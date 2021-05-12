# Student

```java
package com.day10.homework;


public class Student {
	private String name;
	private int kor;
	private int eng;
	private int math;
	private String gpa;
	private int grade;
	private double average;
public String getName() {

	return name;
}

public void setName(String name) {
	if (name.length() <= 10) {// 10자 이하
		this.name = name;
	}
}

public int getKor() {
	return kor;
}

public void setKor(int kor) {
	if (kor > 0 && kor < 100) {
		this.kor = kor;
	}
}

public int getEng() {
	return eng;
}

public void setEng(int eng) {
	if (eng > 0 && eng < 100) {
		this.eng = eng;
	}
}

public int getMath() {
	return math;
}

public void setMath(int math) {
	if (math > 0 && math < 100) {
		this.math = math;
	}
}

public String getGpa() {
	return gpa;
}

private void setGpa() {
	if (average > 90) {
		gpa = "A";
	} else if (average > 80) {
		gpa = "B";
	} else if (average > 70) {
		gpa = "C";
	} else if (average > 60) {
		gpa = "D";
	} else {
		gpa = "F";
	}
}

public int getGrade() {
	return grade;
}

public void setGrade(int grade) {
	if (grade >= 1 && grade <= 4) {
		this.grade = grade;
	}
}

public double setAverage() {
	average = (kor + eng + math) / 3.0;
	return average;
}

Student() {
	setAverage();
	setGpa();
}

Student(String name) {
	this.name = name;
	setAverage();
	setGpa();
}

Student(String name, int kor, int eng, int math) {
	setName(name);
	setKor(kor);
	setEng(eng);
	setMath(math);
	setAverage();
	setGpa();
	
}

String getInfo() {
	return "이름 : " + name 
			+ "\n 국어 점수 : " + kor 
			+ "\n영어 점수 : " + eng 
			+ "\n수학 점수 : " +math
			+ "\n평균 : " + average 
			+ "\n등급 " + gpa
			+ "\n학년" + grade;
}
}
```

