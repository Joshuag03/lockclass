# lockclass
Create class Lock
Write the class Lock that could use to create electronic lock objects. Each lock may be in either an open (unlocked) or a closed (locked) state and each is protected by its own integer key which must be used to unlock it. The class should contain the following methods:

public Lock(int key)

Create a lock that initially open

public void close()

Close the lock

public boolean isOpen()

Return true if and if the lock is open

public void open(int key)

Open the lock if and only if the parameter key matches the lock’s own key. If the lock is closed and the keys do not match, count that failed attempt. If the same lock receives three (3) or more failed attempts in a row, print the message “Alarm” (this to be done in main).

Check for correct input (key can only be a 3 digit integer). User input (lock key) is expected. The following main method illustrates how the Lock class should work:

public static void main (String[] args) { System.out.println("Enter key"); int key1 = Integer.parseInt(obj.readLine()); // set to 111 System.out.println("Enter key"); int key2 = Integer.parseInt(obj.readLine()); // set to 222 Lock lock1 = new Lock (key1); Lock lock2 = new Lock (key2); lock1.close(); lock2.close(); System.out.println(lock1.isOpen()); // prints false lock1.open(123); // fails to open lock1.open(456); // fails to open lock2.open(222); // opens lock2 lock1.open(789); // fails - prints “Alarm” lock1.open(111); // opens lock1 } 
