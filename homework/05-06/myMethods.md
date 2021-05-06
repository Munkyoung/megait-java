# mymethods

	package com.day07.homework;
	
	public class myMethods {
	double get_average(int kor, int math, int eng) {
	
		double average = (kor + math + eng) / 3.0;
		return average;
	}
	
	String print_stars(int num) {
		String stars = "";
		for (int i = 0; i <= num; i++) {
			stars += "*";
		}
		return stars;
	}
	
	String greet(String name, int age) {
		String hi;
	
		if (age > 20) {
			hi = name + "님 안녕하세요?";
		} else {
			hi = name + "(아)야 안녕?";
		}
		return hi;
	
	}
	
	int calc(int n1, int n2, String c) {
		int result;
		switch (c) {
		case "+":
			result = n1 + n2;
			break;
		case "-":
			result = n1 - n2;
			break;
		case "*":
			result = n1 * n2;
			break;
		case "/":
			result = n1 / n2;
			break;
		case "%":
			result = n1 % n2;
			break;
		default:
			result = 0;
		}
		return result;
	}
	}

