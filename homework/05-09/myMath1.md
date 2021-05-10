```java
package com.day08.homework;

public class myMath {
	int sum = 0;
	int getTotal(int n){
		for(int i=0;i<n;i++) {
			sum += n-i;
		}
return sum;
	
}
String getGugudan(int n) {
	String g = "";
	for(int i = 1; i <=9; i ++) {
	g  +=	n  +"  *  "+ i + " = "+ n*i + "\n";
	}
	return g;
}
}
```
