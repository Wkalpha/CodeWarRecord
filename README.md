# CodeWar record  
Question 1.  

Trolls are attacking your comment section!  
A common way to deal with this situation is to remove all of the vowels from the trolls' comments, neutralizing the threat.  
Your task is to write a function that takes a string and return a new string with all vowels removed.  
For example, the string "This website is for losers LOL!" would become "Ths wbst s fr lsrs LL!".  
Note: for this kata y isn't considered a vowel. 

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
```
