public class CreditCard{
  
  public boolean verify(String num){             //luhn check:
    int evens = 0, sum, odds = 0;
    for(int i = num.length()-2; i >=0; i-=2){    //go from right to left, take all numbers in even spaces
      int evenPos = Integer.parseInt(num.substring(i,i+1));
      evenPos = evenPos * 2;        //multiply each number in an even spot by 2
      if (evenPos >= 10)            //if it is >10 after multiplication, add the numbers in each spot (12 becomes 1+2 = 3) 
        evenPos = evenPos - 9;      //(so subtract 9 from #s greater than 10)
      evens =+ evenPos;             //take sum of all the new numbers together
    }
    
    for(int j = num.length()-1; j >=0; j-=2){      //from right to left, take all the numbers in odd places
      int oddPos = Integer.parseInt(num.substring(j,j+1));
      odds =+ oddPos;       //add all of the numbers in odd places together
    }
    sum = evens + odds;     //add sum of evens to sum of odds
    if (num.length() < 13 || num.length() > 16)  //checks to make sure the card is a valid length (between 13-16)
      return false;
    else if (sum % 10 == 0)      //credit number is valid if sum modulus 10 = 0
      return true;
    else
      return false;
    
  }
  public int findType(String num){      //starting numbers:
    if (num.length() < 13 || num.length() > 16)     //checks to make sure the card is a valid length (between 13-16)
      return 0;
    else if (Integer.parseInt(num.substring(0,2)) >= 51 && Integer.parseInt(num.substring(0,2)) <= 55)      //it is a mastercard if the first two numbers are between 51-55 
      return 1;
    else if (Integer.parseInt(num.substring(0)) == 4)       //it is a visa card if the first number is 4
      return 2;
    else if (Integer.parseInt(num.substring(0,2)) >= 34 && Integer.parseInt(num.substring(0,2)) <= 37)      //it is an american express card if the first two numbers are between 34-37
      return 3;  
    else if (Integer.parseInt(num.substring(0,4)) == 6011 ) //it is a discover card if the first four digits are 6011
      return 4;
    else if (Integer.parseInt(num.substring(0,3)) >= 300 && Integer.parseInt(num.substring(0,3)) <= 305 || Integer.parseInt(num.substring(0,2)) == 36 || Integer.parseInt(num.substring(0,2)) == 38)  
      return 5;      //it is a carte blanch/diners card if the first two numbers are 36 or 38 or the first three numbers are between 300-305
    else
      return 0;
    
  }
}  //end of class