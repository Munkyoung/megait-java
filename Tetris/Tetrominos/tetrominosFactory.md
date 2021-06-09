```java
public class TetrominosFactory {
	
	public static Tetromino create () {
		
		switch ((int)(Math.random()*7+1)) {
		case 1:
			return new OTetromino();
			
		case 2:
			return new JTetromino();
		
		case 3:
			return new ITetromino();
			
		case 4:
			return new STetromino();
			
		case 5:
			return new ZTetromino();
			
		case 6:
			return new ITetromino();
				
		case 7:
			return new TTetromino();
			
		default:
			return new TTetromino();
			
		}
		
		
		
	}
	

}
```
