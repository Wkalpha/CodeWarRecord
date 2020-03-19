# CodeWar record  
[Question 1.](https://www.codewars.com/kata/52fba66badcd10859f00097e/train/java)  
My solution:
```java
public class Troll {
    public static String disemvowel(String str) {
        // Code away...
        String ans = str.replaceAll("[aeiouAEIOU]","");
        return ans;
    }
}
```
[Question 2.](https://www.codewars.com/kata/578aa45ee9fd15ff4600090d/train/java)  
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
