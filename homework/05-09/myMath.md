myMath

```java
package com.day08.homework;

import java.util.Scanner;

import javax.swing.JOptionPane;

public class homework01 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		myMath func = new myMath();
		
while (true) {
		String a = JOptionPane.showInputDialog("1. 총합 구해보기" + "\n" + "2. 구구단 보기 " + "\n" + "3.종료");
		if (a.equals("1")) {
			String n1 = JOptionPane.showInputDialog("정수 하나를 입력 하세요.");
			
			int n = Integer.parseInt(n1);

			JOptionPane.showMessageDialog(null, func.getTotal(n));

			continue;
		} else if (a.equals("2")) {
			String n1 =JOptionPane.showInputDialog("정수 하나를 입력 하세요.");
			
			int n = Integer.parseInt(n1);

			JOptionPane.showMessageDialog(null, func.getGugudan(n));
			continue;

		} else if (a.equals("3")) {
			break;
		}

	}
}
}
```

