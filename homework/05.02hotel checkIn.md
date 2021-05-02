# 호텔 체크인

```java
package com.day04.homework;

import javax.swing.JOptionPane;

public class homework05 {
	public static void main(String[] args) {
		String tmp = JOptionPane.showInputDialog("방 개수를 입력 하세요");

		int[] num = new int[Integer.parseInt(tmp)];

		String menu = "1. 체크인 \n" + "2. 체크아웃 \n" + "3. 현황 보기 \n" + "0. 종료하기";
		// 방 개수 입력 받기

		while (true) {

			String select = JOptionPane.showInputDialog(menu);

			if ("1".equals(select)) {
				JOptionPane.showMessageDialog(null, "체크인을 합니다.");
				while (true) {

					String roomnum = JOptionPane.showInputDialog("체크인할 방 호수를 입력 하세요 \n ");
					int count = Integer.parseInt(roomnum) - 1;
					if (count < 0 || count >= num.length) {
						JOptionPane.showMessageDialog(null, "잘못 입력 하셨습니다.");
						continue;

					}

					if (num[count] == 1) {
						JOptionPane.showMessageDialog(null, "입실중인 방은 체크인 하실수 없습니다");
					} else {
						JOptionPane.showMessageDialog(null, "입실 완료");
						num[count] = 1;
						break;
					} // 엘스

				} // 1번 무한 반복
			} else if ("2".equals(select)) {

				JOptionPane.showMessageDialog(null, "체크아웃을 합니다.");
				while (true) {

					String roomnum = JOptionPane.showInputDialog("체크아웃할 방 호수를 입력 하세요 \n ");
					int count = Integer.parseInt(roomnum) - 1;
					if (count < 0 || count >= num.length) {
						JOptionPane.showMessageDialog(null, "잘못 입력 하셨습니다.");
						continue;

					}

					if (num[count] == 0) {
						JOptionPane.showMessageDialog(null, "비어있는 방입니다");
					} else {
						JOptionPane.showMessageDialog(null, "퇴실 완료");
						num[count] = 0;
						break;
					} // 엘스

				} // 1번 무한 반복
			} else if ("3".equals(select)) {
				JOptionPane.showMessageDialog(null, "현황 보기를 합니다.");
				String a = "";
				for (int i = 0; i < num.length; i++) {
					a += i + 1 + "번 방 = " + (num[i] == 0 ? "빈방\n" : "입실중\n");
				}

				JOptionPane.showMessageDialog(null, a);

			} else if ("0".equals(select)) {
				JOptionPane.showMessageDialog(null, "프로그램을 종료합니다.");
				break;
			} else {

				JOptionPane.showMessageDialog(null, "잘못 입력 하셨습니다.");
				continue;

			}

		}
	}
}
```
