# Computer-Programming-2_Activities_Izza-Espayos-Hamor

class MainCountingDuplicateCharacters{  
  public static void main(String args[]){  
     String string1 = "Happy Birthday";  
        int count;  
          
        char string[] = string1.toCharArray();  
          
        System.out.println("Duplicate characters in a given string: ");   
        for(int o = 0; o <string.length; o++) {  
            count = 1;  
            for(int c = o+1; c <string.length; c++) {  
                if(string[o] == string[c] && string[c] != ' ') {  
                    count++;    
                    string[c] = '0';  
                }  
            }   
            if(count > 1 && string[o] != '0')  
                System.out.println(string[o]);  
        }  
    }  
}  


class MainFindingTheFirstNonrepeatedCharacter{  

 public static void main(String args[]){  
     
        String inputStr ="happiness";

        for(char i :inputStr.toCharArray()){
        if ( inputStr.indexOf(i) == inputStr.lastIndexOf(i)) {
            System.out.println("First non-repeated character is: "+i);
            break;
        }
    }
}
}

+ javac -cp . Main.java
+ java -cp . Main
First non-repeated character is: h



class MainCheckingWhetherAStringContainsOnlyDigit{  
  public static void main(String args[]){ 
 
    String str = "2783946";
    boolean result = str.matches("[0-9]+");
    System.out.println("String : " + str);
    System.out.println("Does string contain only Digits? : " + result);
  }
}

+ javac -cp . Main.java
+ java -cp . Main
String : 2783946
Does string contain only Digits? : true


class MainRemovingWhiteSpaceFromAString{  
  public static void main(String args[]){ 
 
      String Str = new String("Break the norms");
      System.out.print("Return Value :" );
      System.out.println(Str.replaceAll(" ", ""));
   }
}

+ javac -cp . Main.java
+ java -cp . Main
Return Value :Breakthenorms




import java.util.Arrays;
class MainCheckingwhetherTwoStringsAreAnagram {
  public static void main(String[] args) {

    String str1 = "night";
    String str2 = "thing";
    
    str1 = str1.toLowerCase();
    str2 = str2.toLowerCase();

    if(str1.length() == str2.length()) {

      char[] charArray1 = str1.toCharArray();
      char[] charArray2 = str2.toCharArray();

      Arrays.sort(charArray1);
      Arrays.sort(charArray2);
      boolean result = Arrays.equals(charArray1, charArray2);

      if(result) {
        System.out.println(str1 + " and " + str2 + " are anagram.");
      }
      else {
        System.out.println(str1 + " and " + str2 + " are not anagram.");
      }
    }
    else {
      System.out.println(str1 + " and " + str2 + " are not anagram.");
    }
  }
}

+ javac -cp . Main.java
+ java -cp . Main
night and thing are anagram.






