# 로그인 

```java
package com.day13.homework;

import java.util.Scanner;

public class Homework01 {
	public static void main(String[] args) {
		// String pwPattern
		// ="^(?=.*[A-Za-z])(?=.*\d)(?=.*[~!@#$%^&*()+|=])[A-Za-z\d~!@#$%^&*()+|=]{8,16}$";
		String a = "";
		String pw = "1";
		String checkPw = "2";
		Scanner sc = new Scanner(System.in);
		
		while (true) {
			System.out.println("이메일을 입력하세요...");
			idCheck email = new idCheck(sc.next());
			if ("x".equals(email.idc())) {
				System.out.println("email을 잘못 입력 하셨습니다...");
				continue;
			} else {
				System.out.println(email	);
				a = email.toString();
				break;
			}
		}
		
		while (true) {
			System.out.println("비밀번호를 입력하세요...");
			pw = sc.next();
			System.out.println("한번더 입력해 주세요...");
			checkPw = sc.next();
			 if (pw.equals(checkPw)) {
				break;
			} 
			 else {
				System.out.println("잘못 입력 하셨습니다. 다시입력하세요");
				continue;
			}
		}

		String[] sArr = a.split("@");
		System.out.println("email : " + a);
		System.out.println("id : " + sArr[0].toString());
		System.out.println("password : " + pw);
	}

}
```

