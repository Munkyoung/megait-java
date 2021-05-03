#  배열

```java
package com.day05.homework;

public class homework02 {
	public static void main(String[] args) {

		int[][] num = new int[4][4];
		int count = 0;
		// 2-1
		for (int i = 0; i < num.length; ++i) {
			System.out.println("\n");
			for (int j = 0; j < num[i].length; ++j) {
				count++;
				num[i][j] = count;
				System.out.print("\t" + num[i][j]);
			}
		}

		count = 0;

		for (int i = 0; i < num.length; ++i) {
			System.out.println("\n");
			for (int j = 0; j < num[i].length; ++j) {
				count++;
				num[i][j] = count;
				System.out.print("\t" + num[j][i]);
			}
		}
		count = 0;
		

		for (int i = 0; i < num.length; ++i) {
			System.out.println("\n");
			if (i % 2 != 0) {
				for (int j = num[i].length-1; j >= 0; --j) {
					count++;
					num[i][j] = count;
				}

			} else {
				for (int j = 0; j < num[i].length; ++j) {
					count++;
					num[i][j] = count;
				}
			}

		}
		for (int i = 0; i < num.length; ++i) {
			System.out.println("\n");
			for (int j = 0; j < num[i].length; ++j) {
				System.out.print("\t" + num[i][j]);
			}
		}
		
	}
}
```

