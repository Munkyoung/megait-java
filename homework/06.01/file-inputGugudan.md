# FileinputStream구구단

```java
public class Homewokr03 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("원하는 단을 입력하세요...");
		String ans = sc.next();
		try {
			FileInputStream fin = new FileInputStream("구구단" + ans + "단.txt");
			String s;
			Scanner fsc = new Scanner(fin);
			while (fsc.hasNext()) {
				s = fsc.nextLine();
				System.out.println(s);
			}

			sc.close();
			fin.close();
		} catch (Exception e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}

	}

}
```
