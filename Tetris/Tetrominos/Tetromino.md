```java
public class Tetromino extends JPanel{
	
	private static final Color[] COLOR = { 
			new Color(2,218,218),		 // I 블럭 의 색상
			new Color(218,68,230), 	 	 // T 블럭 의 색상
			new Color(255, 166, 0), 	 // L 블럭 의 색상
			new Color(0,85,255),   		 // J 블럭 의 색상
			new Color(218,218,2),  		 // ㅁ 블럭 의 색상	
			new Color(239,71,71),		 // z 블럭 의 색상
			new Color(2,218,2)			 // s 블럭 의 색상
	};
	
	int x;
	int y;
	int type;
	int wid;
	int hei;
	
	void Down () {
		y--;
	}
	void Left () {
		x--;
	}
	void Right () {
		x++;
	}
	public int getX	() {
		return x;
	}
	public int getY	() {
		return y;
	}
	
	
}
```
