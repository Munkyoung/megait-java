````java
package com.day12.homework;

public class Homework01 {
	public static void main(String[] args) {
		long a = System.currentTimeMillis();
		
		for(int i = 1; i<=1000000; i++) {
			System.out.println(i);
		}
		long b = System.currentTimeMillis();
		System.out.println(a);
		System.out.println(b);
		System.out.println(b-a);
	}

}
````
