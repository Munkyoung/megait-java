# tourist


		

```java
	package com.day09.homework;

import javax.swing.JOptionPane;

public class homework01 {
	public static void main(String[] args) {
		int lastidx = 0 ;
		int total = 0 ;
		String vip = "";
	Tourist[] p = new Tourist[5];

	for (int i = 0; i < p.length; i++) {
		p[i] = new Tourist();
	}

	String menu = "1. 목적지 설정 \n 2. 여행객 추가 \n 3. 모든 여행객 정보보기 \n 4. 전체 예산 보기 \n 5. VIP조회 \n 0. 종료";
	while (true) {
		loop: switch (JOptionPane.showInputDialog(menu)) {
		case "1":
			Tourist.destination = JOptionPane.showInputDialog("목적지를 설정 해주세요.");
			break;

		case "2":
			
			p[lastidx]  =  new Tourist();
			p[lastidx].name = JOptionPane.showInputDialog(lastidx +1  + "번 여행객의 이름을 입력하세요..");
			p[lastidx].budget = Integer.parseInt(JOptionPane.showInputDialog("예산을 입력하세요..."));
			lastidx++;
			/*for (int i = 0; i < p.length; i++) {
				p[i].name = JOptionPane.showInputDialog((i + 1) + "번 여행객의 이름을 입력하세요..");
				p[i].budget = Integer.parseInt(JOptionPane.showInputDialog("예산을 입력하세요..."));
			}*/
			break;

		case "3":
			for (Tourist a : p) {
				JOptionPane.showMessageDialog(null, a.getData() );
			}
			break;

		case "4":
			for (int i = 0; i < p.length; i++) {
			total +=p[i].budget;
			}
			JOptionPane.showMessageDialog(null,"총 예산은 : " +  total + "입니다.");
			break;

		case "5":
			int max = p[0].budget;
			for (int i = 0; i < p.length; i++) {
				if (max < p[i].budget) {
					max = p[i].budget;
				}
			}
			for (int i = 0; i < p.length; i++) {
				if (max == p[i].budget) {
					p[i].vip = 1;
					vip = p[i].name;
				}
			}
			JOptionPane.showMessageDialog(null, vip);
			break;

		case "0":
			break;
		default:
			System.out.println("잘못 입력 하셨습니다.");
			break loop;

		}

	}

}
}
```
