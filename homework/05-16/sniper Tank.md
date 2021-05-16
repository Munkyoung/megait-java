# tank sniper

```java
package com.day11.homework;

public class Homework01 {
public static void main(String[] args) {
		
		Unit p1 = new Unit();
		Unit p2 = new Unit();
		int rand1 = (int)(Math.random()*2);
		int rand2 = (int)(Math.random()*2);
		
		switch (rand1) {
		case 0 : 
			p1 = new Sniper();
		case 1 : 
			p1 = new Tank();
		}
		switch (rand2) {
		case 0 : 
			p2 = new Sniper();
		case 1 : 
			p2 = new Tank();
		}
		
		while (p1.alive && p2.alive) {
			p1.attack(p2);
			p2.attack(p1);
			if (p1.hp <= 0 ) {
				p1.alive = false;
				System.out.println("p2 가 이겼습니다");
			}
			if (p2.hp <= 0) {
				p2.alive = false;
				System.out.println("p1 가 이겼습니다");
			}
		}
		
		
	}

}
```
