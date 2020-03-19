# CodeWar record  
[Question 1.](https://www.codewars.com/kata/52fba66badcd10859f00097e/train/java)  
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
