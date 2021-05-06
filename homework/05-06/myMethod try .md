package com.day07.homework;

public class homework01 {
	public static void main(String[] args) {

		myMethods mym = new myMethods();

		double ave = mym.get_average(80, 90, 70);
		System.out.println(ave);

		String stars = mym.print_stars(6);
		System.out.println(stars);

		String hi = mym.greet("홍길동", 25);
		System.out.println(hi);

		int calc = mym.calc(5, 5, "+");
		System.out.println(calc);

	}
}
