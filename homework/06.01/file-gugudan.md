# Filewriter 구구단 만들기

```java
public class Homework02 {
	public static void main(String[] args) {
		String gugu = "";

		try {

			for (int i = 2; i <= 9; i++) {
				FileWriter fw = new FileWriter("구구단" + i + "단.txt");
				for (int j = 1; j <= 9; j++) {
					gugu = i + " x " + j + " = " + i * j + "\n";
					fw.write(gugu);
				}
				fw.close();
			}

		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
	}

}

```
