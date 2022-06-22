## Threads
A thread is a program unit that runs independently of other parts of the program.

## Race conditions
## Synchronizing object access
The lock object is used to control threads that want to manipulate shared resource.
```java
public class BankAccount {
	private Lock balanceChangeLock;
	. . .
	public BankAccount() {
		balanceChangeLock = new ReentrantLock();
		. . .
	}
}
```
```java
balanceChangeLock.lock();
try {
	Manipulate the shared resource.
} finally {
	balanceChangeLock.unlock();
}
```

## Deadlocks
It can happen when one thread acquires a lock, waits for another thread to finish, but the one thread it's waiting for is in need of the lock the first thread acquired.
This is easily fixable by a **condition object**. Condition objects allow a thread to temporarily release a lock, then regain the lock at a later time.
```java
public class BankAccount {

	private Lock balanceChangeLock;
	private Condition sufficientFundsCondition;
	. . .
	public BankAccount() {
		balanceChangeLock = new ReentrantLock();
		sufficientFundsCondition = balanceChangeLock.newCondition();
		. . .
	}
}
```
As long as there are no sufficient funds, call the *await* method on the condition object. Doing this, the current thread will be in a blocked state.
```java
public void withdraw(double amount) {

	balanceChangeLock.lock();

	try {
		while (balance < amount) {
			sufficientFundsCondition.await();
		}
		. . .
	} finally {
		balanceChangeLock.unlock();
	}
}
```
To unblock the thread, another thread must call the *signalAll* method on the **same** condition object. With that, all threads will be unblocked and then they'll compete for the lock.
```java
public void deposit(double amount) {

	balanceChangeLock.lock();

	try {
		. . .
		sufficientFundsCondition.signalAll();
	} finally {
		balanceChangeLock.unlock();
	}
}
```