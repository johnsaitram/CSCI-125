## 1.  Create a class (use your imagination min 4 properties, 4 behavior);
## 2.  Create a default and parameterized constructors;
## 3.  Create objects from the class and test your code; 
    public class PokemonBattleSimulatorV1 {
	
	String name;
	String type;
	Boolean shinyvariant;
	int nationaldexnumber;
	int level;
	
	public void start1() {
		System.out.println(""+name+" I choose you!");
	}
	
	public void start2() {
		System.out.println("Go,"+name+"!");
	}
	public void info1() { 
		System.out.println("[Level "+level+"]  ["+type+"]");
	}

	public PokemonBattleSimulatorV1(Boolean shinyvariant1, String name1, int level1 ,String type1, int nationaldex1) {
		
		/** boolean was used for a if the pokemon was shiny, 
		which in the game is set to a true or false value.
		Plan to have it change color of name to gold if true  **/
		
		name = name1;
		type = type1;
		shinyvariant = shinyvariant1;
		nationaldexnumber= nationaldex1;
		level = level1;
		
	}
	public static void main(String[] args) {
		
		PokemonBattleSimulatorV1 c1 = new PokemonBattleSimulatorV1(true,"Venusaur",50,"Grass-Poison",003);
		PokemonBattleSimulatorV1 c2 = new PokemonBattleSimulatorV1(true,"Charizard",50,"Fire",006);
		PokemonBattleSimulatorV1 c3 = new PokemonBattleSimulatorV1(true,"Blastoise",50,"Water",9);
		PokemonBattleSimulatorV1 c4 = new PokemonBattleSimulatorV1(true,"Pikachu",25,"Electric",025);
		
		//for the .start, the user can choose 1 or 2
		

		c1.start1();
		c1.info1();
		c3.start2();
		c3.info1();
		}



	}
