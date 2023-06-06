"# Week05" 
package week05Assignment;

public interface Logger {
	
	public void log(String log);
	public void error(String error);

}


package week05Assignment;



public class AsteriskLogger implements Logger {
	
	public void log(String log) {
		System.out.println("***" + log + "***");
	}
	public void error (String error) {
		System.out.println("*********" + "*".repeat(error.length()));
		System.out.println("***ERROR: " + error + "***");
		System.out.println("*********" + "*".repeat(error.length()));
		
	}

}


package week05Assignment;

	public class SpacedLogger implements Logger {
		
		
		
		public void log(String log) {
			char [] logChar = log.toCharArray();
			
			for (char a : logChar) {
				System.out.print(a);
			System.out.print(" ");
			}
		}
		public void error(String error) {
			System.out.print("ERROR:" );
			char [] errorChar = error.toCharArray();
			
			for(char b : errorChar) {
				System.out.print(b);
				System.out.print("  ");
			}
		}
    
    
    package week05Assignment;

public class App extends SpacedLogger {

	public static void main(String[] args) {
	
		Logger log = new AsteriskLogger();

		log.log("Hello");
		System.out.println();
		
		log.error("Hello");
		System.out.println();
		
		log.log("Hello");
		System.out.println();
		
		log.error("Hello");
		System.out.println();
		
		
		SpacedLogger secondLog = new SpacedLogger();
		
		secondLog.log("Hello");
		System.out.println();
		
		
		secondLog.error(" Hello");
		System.out.println();
		
		secondLog.log("Hello");
		System.out.println();
	
		
		secondLog.error(" Hello");
		System.out.println();
		
		
		
		
		
		
		
		
		

	}

}

		
		

