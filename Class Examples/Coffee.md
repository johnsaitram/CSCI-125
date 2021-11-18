# Coffee example:
### This is the example that the professor went over during lecture 4;

    package lecture4;
    //change package name to your own package
    public class Coffee {

    String name;
    String color;
    String roastLevel;
    int intensity;
    int tempature;

    public void brew() {
	    System.out.println("Coffee for "+name+" is getting ready");
    }

    //public Coffee() {
    //	name = "Azhar";
    //	color = "Medium Dark";
    //	tempature = 200;
    //	
    //}

    public Coffee(String name1, int temp) {
	  name = name1;
	  tempature = temp;
	
    }
    public static void main(String[] args) {
	
	  Coffee c1 = new Coffee("Aaron",50);
	  //c1.name ="john";
	  Coffee c2 = new Coffee("Rishi",100);
	  //c2.name="aaron";
	
	c1.brew();
	c2.brew();
	}


    }
