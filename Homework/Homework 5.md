## 1. Create an abstract class PayCalculator that has an attribute payRate given in dollars per hour. 
### The class should also have a method computePay(hours) that returns the pay for a given amount of time.

	abstract class PayCalculator{
	  private double payRate;
	  public PayCalculator(double payRate) {
		   this.payRate = payRate;
	}  
    
	public double computePay(int hours) {
	  return payRate*hours; 
    }
    }
   
## 2. Derive a class RegularPay from PayCalculator, as described in the previous exercise. 
### It should have a constructor that has a parameter for the pay rate. It should not override any of the methods. 
## Then derive a class HazardPay from PayCalculator that overrides the computePay method. 
### The new method should return the amount returned by the base class method multiplied by 1.5.

    abstract class PayCalculator{
      private double payRate;
      public PayCalculator(double payRate) {
        this.payRate = payRate;
      }

    public double computePay(int hours) {
      return payRate*hours;




    }


    }


    class RegularPay extends PayCalculator{
      public RegularPay(double payRate) {

      super(payRate);
      }
    }	
      class HazardPay extends RegularPay{
        public HazardPay(double payRate) {

          super(payRate);
        }
        public double computePay(int hours) {

          return super.computePay(hours)*1.5;
        }

      }

        class Main{
          public static void main(String[] args) {
            RegularPay regularPay = new RegularPay(150);
            HazardPay hazardPay = new HazardPay(150);
            System.out.println("Regular payment for 5 hours:" + regularPay.computePay(5));
            System.out.print("Hazard payment for 5 hours:" + hazardPay.computePay(5));

          }
        }




## 3. Create an abstract class DiscountPolicy. 
### It should have a single abstract method computeDiscount that will return the discount for the purchase of a given number of a single item. 
#### The method has two parameters, count and itemCost.

    abstract class DiscountPolicy{
      abstract double computeDiscount(int count, double itemcost);

    }

    class Test extends DiscountPolicy{
      double computeDiscount(int count, double itemcost)

      {
        double discount;
        discount = (itemcost*count*5)/100;

        return discount;
      }
    public static void main(String args[]){
      Test dp = new Test();
      System.out.print(dp.computeDiscount(50, 100));
    }






    }


## 4. Derive a class BulkDiscount from DiscountPolicy, as described in the previous exercise. 
### It should have a constructor that has two parameters, minimum and percent. 
### It should define the method computeDiscount so that if the quantity purchased of an item is more than minimum, the discount is percent percent.

    abstract class DiscountPolicy
    {   
    public abstract double computeDiscount(int count, double itemCost);
    }  

    class BulkDiscount extends DiscountPolicy
    {   
    private double percent;
    private double minimum;

    public BulkDiscount(int minimum, double percent)
    {
    this.minimum = minimum;
    this.percent = percent;
    }

    @Override
    public double computeDiscount(int count, double itemCost)
    {
    if (count >= minimum)
    {
    return (percent/100)*(count*itemCost); //discount is total price * percentage discount
    }

    return 0;
    }
    }
    public class Main {

       public static void main(String[] args) {
           BulkDiscount bd=new BulkDiscount(10,5);
            System.out.println("Bulk Discount :"+bd.computeDiscount(20, 20));

       }

    }
