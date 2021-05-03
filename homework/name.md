# 배열 문제

## 가능한 이름 조합

```java
package com.day09.quiz;

public class quiz02 {
	public static void main(String[] args) {
		String [] fname = {"김","이","박","최","한"};
		String [] name = {"피카츄","라이츄","파이리","꼬부기","버터풀","야도란","피죤투"};
		
		for (int i = 0; i < fname.length; i++) {
			
			
			for (int j=0; j< name.length; j++) {
			//	System.out.println("조합가능한 이름 : " + fname[i] + name[j]);
				
			}// 작은 for
			
			
		}// 큰 for
		
		for(int i = 0; i < 10; ++i) {
			
		int rand1 = (int)(Math.random()*fname.length);
		
		int rand2 = (int)(Math.random()*name.length);
		
		System.out.println("=====가능한 " + (i+1) + " 번째 이름======");
		System.out.println(fname[rand1] + name[rand2]);
		}
	
}

}
```
