# CodeWar record  
[Question 1.](https://www.codewars.com/kata/52fba66badcd10859f00097e/train/java)  
將輸入的英文字串母音取代為空白  
My solution:
```java
public class Troll {
    public static String disemvowel(String str) {
        String ans = str.replaceAll("[aeiouAEIOU]","");
        return ans;
    }
}
```
[Question 2.](https://www.codewars.com/kata/578aa45ee9fd15ff4600090d/train/java)  
將輸入的數值陣列的奇數做小到大排序  
My solution:
```java
public class Kata {
  public static int[] sortArray(int[] array) {
		int x,y = 0;
		for(int i = 0; i<array.length; i++){
			for(int j=i+1; j<array.length; j++){
				if(array[i]>array[j] && (array[i]%2!=0 && array[j]%2!=0)){
					x = array[i];
					y = array[j];
					array[j] = x;
					array[i] = y;
				}
			}
		}
	    return array;
	  }
}
```  

[Question 3.](https://www.codewars.com/kata/55bf01e5a717a0d57e0000ec/train/java)  
將輸入的數值拆開相乘做為新的輸入值，直到輸入的數字位數為1  
My solution:  
```java
class Persist {
  static int count = 0;
  public static int persistence(long l) {
    try{
      int inputLength = Long.toString(l).length();
      int temp2 = 1;
      String inputToString = Long.toString(l);
      if(inputLength>=2){
        int[] temp = new int[inputLength];
        for(int i =0;i<inputLength;i++){
          temp[i] = Character.getNumericValue(inputToString.charAt(i));
        }
        for(int i2=0;i2<temp.length;i2++){
          if(i2<temp.length){
            temp2 *= temp[i2];
          }
        }
        count++;
        return persistence(temp2);
      }else{
        return count;
      }
    }finally{
      count = 0;
    }
    
  }
}
```  
Another answer:  
```java
class Persist {
  public static int persistence(long n) {
    long m = 1, r = n;

    if (r / 10 == 0)
      return 0;

    for (r = n; r != 0; r /= 10)
      m *= r % 10;

    return persistence(m) + 1;
    
  }
}
```  
[Question 4.](https://www.codewars.com/kata/546e2562b03326a88e000020/train/java)  
輸入的數值單獨平方後串聯為字串，輸出要為數值型別
My solution:  
```java
public class SquareDigit {

  public int squareDigits(int n) {
    String re = "";
    String temp = Integer.toString(n);
    int[] a = new int[temp.length()];
    for(int i = 0;i<temp.length();i++){
	a[i] = (int) Math.pow(temp.charAt(i) - '0', 2);
	}
    for(int r:a){
	    	re += r;
}
  return Integer.parseInt(re);
}
}
```  
Another answer:  
```java
public class SquareDigit {

  public int squareDigits(int n) {
    String result = ""; 
    
    while (n != 0) {
      int digit = n % 10 ;
      result = digit*digit + result ;
      n /= 10 ;
    }
    
    return Integer.parseInt(result) ;
  }

}
```  
[Question 5.](https://www.codewars.com/kata/5262119038c0985a5b00029f/train/java)  
判斷輸入的數值是否為質數  
My solution(會超時):
```java
public class Prime {
  public static boolean isPrime(int num) {
	int count = 0;
 	if(num <= 0 || num == 1 || num == 4){
 		return false;
 	}else if(num == 2){
 		return true;
 	}else{
 		for(int i = 2; i <= num; i++){
			if(num%i==0 && num != i ){
			count++;
				if(count>=1){
					return false;
				}
			}
		}
	}
	return(count<=1 ?  true:false);
	}
}
```  
Another solution:  
```java
public class Prime {
  public static boolean isPrime(int num) {
    return num > 1 && java.math.BigInteger.valueOf(num).isProbablePrime(20);
  }
}
```  
[Question 6.](https://www.codewars.com/kata/54b42f9314d9229fd6000d9c/train/java)  
將輸入的字串中，重複的字元替換為)，不重複的字元替換為(，不分大小寫  
```java
public class DuplicateEncoder {
    static String encode(String word){
    word = word.toLowerCase();
    String result = "";
    for(int i =0; i < word.length(); i++){
        char c = word.charAt(i);
	result += word.indexOf(c) == word.lastIndexOf(c) ? "(":")";
    }
    return result;
  }
}
```  

