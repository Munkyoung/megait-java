# Unit

```java
package com.day11.homework;

public class Unit {
	String name;
	int hp;
	int att;
	boolean alive = true;

	public void attack(Unit enemy) {

	}

}

class Sniper extends Unit {// 자식 클래스

	Sniper() {
		System.out.println("Sniper");
		name = "저격수";
		hp = 400;
		att = 100;
	}

	public void attack(Unit enemy) {
		int rand1 = (int) (Math.random() * 10);
		if (rand1 == 0) {
			enemy.hp = 0;
			
		} else {
			enemy.hp -= 100;
		} // else

	}

}

class Tank extends Unit {
	Tank() {
		System.out.println("Tank");
		name = "탱크";
		hp = 4000;
		att = 50;
	}

	public void attack(Unit enemy) {
		int rand1 = (int) (Math.random() * 10);
		if (rand1 <= 2) {
			enemy.hp -= (int) (enemy.hp / 0.3);
			
		} else {
			enemy.hp -= 50;
		} // else
	}

}
```
