# 국가등록

```java
package com.day14.homework;

import java.util.ArrayList;
import java.util.List;

import javax.swing.JOptionPane;

class Nation {
	String nation;
	String capital;
	String population;

	Nation(String nation, String capital, String population) {
		this.nation = nation;
		this.capital = capital;
		this.population = population;

	}

	public String toString() {
		return "국가 이름 : " + nation + "수도 이름 : " + capital + "인구수 : " + population;

	}
}

public class Homework01 {
	public static void main(String[] args) {

		String menu;
		String select;

		menu = "1.국가 추가\r\n" + "2. 모든 국가 보기\r\n" + "3. 번호로 검색\r\n" + "4. 이름으로 검색\r\n" + "0. 종료";
		List<Nation> list1 = new ArrayList<Nation>();
		
		loop: while (true) {
			select = JOptionPane.showInputDialog(menu);
			switch (select) {
			case "1":

				String n1 = JOptionPane.showInputDialog("추가할 국가명을 입력하세요...");
				String n2 = JOptionPane.showInputDialog("추가할 국가의 수도 입력하세요...");
				String n3 = JOptionPane.showInputDialog("추가할 국가의 인구수를 입력하세요...");
				list1.add(new Nation(n1, n2, n3));
				
				break ;
			case "2":
				if (list1.isEmpty()) {
					JOptionPane.showMessageDialog(null, "등록된 국가가 없습니다.");
					break;
				}
				/*
				 * for (int i = 0; i < list1.size(); i++) {
				 * JOptionPane.showMessageDialog(null, (i + 1) + "번 국가" + list1.get(i) + "\n");
				}
				 */
				JOptionPane.showMessageDialog(null, list1);
					

				break;
			case "3":
				int num = Integer.parseInt(JOptionPane.showInputDialog("검색할 국가의 번호를 입력하세요"));
				if (num <0 || num >list1.size()) {
					JOptionPane.showMessageDialog(null, "잘못입력하셨습니다.");
					break;
				}
				JOptionPane.showMessageDialog(null, list1.get(num));

				break;
			case "4":
				String name = JOptionPane.showInputDialog("검색할 국가명을 입력하세요");
				for (int i = 0; i < list1.size(); i++) {
					if (name.equals(list1.get(i).nation)) {
						JOptionPane.showMessageDialog(null, list1.get(i));
					}
				}

				break;
			case "0":

				break loop;

			default:
				System.out.println("잘못 입력 하셨습니다.");
				break;
			}
		}

	}

}
```

