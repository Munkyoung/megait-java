# 2차원 배열 문제 

## 몬스터

```java
package com.day05.homework;

import java.util.Scanner;

public class homework01 {
	public static void main(String[] args) {

		Scanner sc = new Scanner(System.in);

		int[][] map = new int[10][10];
		int monster = 0;

		// (int)(Math.random()*10+1) 1~10 사이 숫자

		// 몬스터

		for (int i = 0; i < 30; i++) {
			int a = (int) (Math.random() * 10);
			int b = (int) (Math.random() * 10);
			map[a][b] = 1;
		}
		//플레이어 위치
		System.out.println("행을 입력하세요 : ");
		int p1 = sc.nextInt();
		System.out.println("열을 입력하세요 : ");
		int p2 = sc.nextInt();
		map[p1][p2] = 2;

		for (int i = 0; i < 10; i++) {
			for (int j = 0; j < 10; ++j) {
				System.out.print("\t" + map[i][j]);
			}
			System.out.println("\n");
		}
		System.out.println("공격 범위를 입력 하세요.");
		int range = sc.nextInt();
		for (int i = p1 - range; i <= p1 + range; i++) {
			for (int j = p2 - range; j <= p2 + range; j++) {

				if (map[i][j] == 1) {
					monster += 1;
				}
			}
		}
		System.out.println("공격 가능한 적의 수는 : " + monster + " 마리 입니다.");
	}
}
```

