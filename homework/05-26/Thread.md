# 쓰레드

```java
class Thread1 extends Thread {
	boolean run = true;

	public void run() {
		while (run) {
			System.out.println("룰루랄라~~");
			try {
				Thread.sleep(3000);
			} catch (InterruptedException e) {
				e.printStackTrace();
			}
		}
	}

	void terminate() {
		run = false;
	}

}

class Thread2 extends Thread {
	ArrayList<Integer> asd = new ArrayList<Integer>();
	int i = 0;
	boolean run = true;

	public void run() {
		while (run) {
			System.out.println(i + "초");
			try {
				Thread.sleep(1000);
			} catch (InterruptedException e) {

				e.printStackTrace();
			}
			i++;

		}
	}

	void getRecords() {
		asd.add(i);
	}

	void printRecords() {
		System.out.println(asd);
	}

	void terminate2() {
		run = false;
	}
}

public class Test01 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int answer;
		int quiz = 0;
		Thread1 th1 = new Thread1();
		Thread2 th2 = new Thread2();
		th1.start();
		th2.start();
	

		

		while (quiz <= 5) {
			int rand1 = (int) (Math.random() * 9 + 1);
			int rand2 = (int) (Math.random() * 9 + 1);
			System.out.println(rand1 + "X" + rand2 + " = ?");
			answer = sc.nextInt();
			if (answer == rand1 * rand2) {
				System.out.println("정답입니다.");
				quiz++;
				th2.getRecords();
			} else {
				System.out.println("오답입니다.");
				continue;
			}
		}
		th1.terminate();
		th2.terminate2();
		th2.printRecords();

	}

}
```

