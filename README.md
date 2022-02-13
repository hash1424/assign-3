# assign-3
7feb
q1)public class example 
{
		public static void main(String[] args) {
		String str = "the sky is blue";
		System.out.println("The original string is: " + str);
		String strWords[] = str.split("\\s");
		String rev = "";
		for(String sw : strWords) {
		StringBuilder sb = new StringBuilder(sw);
		sb.reverse();
		rev += sb.toString() + " ";
		}
		System.out.println("The modified string is: " + rev.trim());
		}
		}
    
    
    q2)public class StringCompreesion {
	    
	    static void compression(char[] a, int n){ 
	        
	        int result = 0;
	        
	        for(int i=0; i<n; i++){ 
	            int count = 1; 
	            while(i<n-1 && a[i] == a[i+1]){ 
	                count++; 
	                i++; 
	            } 
	  
	            if(count==1){
	                result++;
	            }
	            else{
	                result = result + 2;
	            } 
	        } 
	        
	        System.out.println(result);
	    } 
	  
	    public static void main(String[] args){
	        
	        char[] a = {'a', 'a', 'a', 'b', 'b'}; 
	        int n = a.length;
	        
	        compression(a, n); 
	    } 
	}
  
  
  
  q3)
  public class Character   
{  
     public static void main(String[] args) {  
        String str = "hin hashim here";  
        int[] freq = new int[str.length()];  
        char minChar = str.charAt(0), maxChar = str.charAt(0);  
        int i, j, min, max;           
        char string[] = str.toCharArray();  
          
        for(i = 0; i < string.length; i++) {  
            freq[i] = 1;  
            for(j = i+1; j < string.length; j++) {  
                if(string[i] == string[j] && string[i] != ' ' && string[i] != '0') {  
                    freq[i]++;    
                    string[j] = '0';  
                }  
            }  
        }  
           
        min = max = freq[0];  
        for(i = 0; i <freq.length; i++) {  
              
            if(min > freq[i] && freq[i] != '0') {  
                min = freq[i];  
                minChar = string[i];  
            }   
            if(max < freq[i]) {  
                max = freq[i];  
                maxChar = string[i];  
            }  
        }  
          
        System.out.println("Minimum occurring character: " + minChar);  
        System.out.println("Maximum occurring character: " + maxChar);  
    }  
}  

q4)
class Teststringcomparison1{  
 public static void main(String args[]){  
   String s1="Hashim";  
   String s2="HASHIM";  
   String s3=new String("Hashim");  
   String s4="Salman";  
   System.out.println(s1.equals(s2)); 
   System.out.println(s1.equals(s3));  
   System.out.println(s1.equals(s4)); 
 }  
}  
q5)
import java.util.*;
public class permute {

	static void permute(String s , String answer)
	{
		if (s.length() == 0)
		{
			System.out.print(answer + " ");
			return;
		}
		
		for(int i = 0 ;i < s.length(); i++)
		{
			char ch = s.charAt(i);
			String left_substr = s.substring(0, i);
			String right_substr = s.substring(i + 1);
			String rest = left_substr + right_substr;
			permute(rest, answer + ch);
		}
	}
	public static void main(String args[])
	{
		Scanner scan = new Scanner(System.in);
		
		String s;
		String answer="";
		
		System.out.print("Enter the string : ");
		s = scan.next();
		
		System.out.print("\nAll possible strings are : ");
		permute(s, answer);
	}

}
8feb
q1)public class removal   
	{  
	public static void main(String[] args)   
	{   
	String str="Geekster-The%school:+you@code:your-succes$Stories";  
	String resultStr="";  
  
	for (int i=0;i<str.length();i++)  
	{    
	if (str.charAt(i)>64 && str.charAt(i)<=122)  
	{     
	resultStr=resultStr+str.charAt(i);  
	}  
	}  
	System.out.println("String after removing special characters: "+resultStr);  
	}  
	}  
  q2)
  public class InternExample{  
public static void main(String args[]){  
String s1=new String("hello");  
String s2="helllo";  
String s3=s1.intern();
System.out.println(s1==s2);
System.out.println(s2==s3);
}
}
q3)import java.util.Scanner;
public class digitt {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);
        StringBuilder sb = new StringBuilder();
        //append;
        String str= sc.nextLine();
        sb.append("+91- ");
        sb.append(str);
        System.out.println(sb);

	}
}

q4)private static String VowelAndConsonants(String str) {
        str=str.toLowerCase();
        int vowel=0,consonant=0;
        for(int i=0;i<str.length();i++) {
            if (str.charAt(i) >= 'a' && str.charAt(i) <= 'z') {
                if(str.charAt(i)=='a'||str.charAt(i)=='e'||str.charAt(i)=='i'||str.charAt(i)=='o'||str.charAt(i)=='u') {
                    vowel++;
                }
                consonant++;
            }
        }
        return new String(vowel+":"+(consonant-vowel));
	}
}


9feb

import java.util.Scanner;

public class AddArray {

	public static void main(String[] args) {
		// TODO Auto-generated method 
		int n;  
		Scanner sc=new Scanner(System.in);  
		System.out.print("Enter the number of elements you want to store: ");  
		 
		n=sc.nextInt();  
		
		int[] array = new int[10];  
		System.out.println("Enter the elements of the array: ");  
		for(int i=0; i<n; i++)  
		{  
		 
		array[i]=sc.nextInt();  
		}  

		 int sum = 0;  
	  
	        for (int i = 0; i < array.length; i++) {  
	           sum = sum + array[i];  
	        }  
	        System.out.println("Sum of all the elements of an array: " + sum);
	        sc.close();
	}

}
q2)

import java.util.Scanner;

public class MiddleElement {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		int n;  
		Scanner sc=new Scanner(System.in);  
		System.out.print("Enter the number of elements you want to store: ");  
		 
		n=sc.nextInt();  
		
		int[] array = new int[10];  
		System.out.println("Enter the elements of the array: ");  
		for(int i=0; i<n; i++)  
		{  
		 
		array[i]=sc.nextInt();  
		}  
		int m=0;
		if(n%2==1)
		{
			m=array[(n+1)/2-1];
		}
		else
		{
			m=(array[n/2-1]+array[n/2])/2;
		}
		
	       System.out.println("Middle element is :"+m);
	       sc.close();
	}

}
q3)

import java.util.Scanner;

public class PositiveNumber {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int n;  
		Scanner sc=new Scanner(System.in);  
		System.out.print("Enter the number of elements you want to store: ");  
		 
		n=sc.nextInt();  
		
		int[] array = new int[10];  
		System.out.println("Enter the elements of the array: ");  
		for(int i=0; i<n; i++)  
		{  
		 
		array[i]=sc.nextInt();  
		}  
		int j = 0;
		while(j < array.length) 
		{
			if(array[j] >= 0) {
				System.out.print( array[j]);
			}
			j++;
		}
		
	       
	       sc.close();

	}

}
10feb)
q1)public class ReverseArray {  
    public static void main(String[] args) {   
        int [] arr = new int [] {1, 2, 3, 4, 5};  
        System.out.println("Og array: ");  
        for (int i = 0; i < arr.length; i++) {  
            System.out.print(arr[i] + " ");  
        }  
        System.out.println();  
        System.out.println("Array in reverse order: ");    
        for (int i = arr.length-1; i >= 0; i--) {  
            System.out.print(arr[i] + " ");  
        }  
    }  
} 

q2)

import java.util.Arrays;
public class Sort {
 
    public static void main(String[] args)
    {
       
        int[] arr = { 13, 7, 8, 45, 21, 9, 110, 102 };
  
       
        Arrays.sort(arr);
        System.out.println("Modified arr[] = %s", Arrays.toString(arr));
                       
    }
    q3)/q4
    class firstlast
{
public static void main(String args[])
{
int a[]=new int[5];
a={1,2,3,4,5};
int size=a.length;
System.out.println("First element of an array is"+a[0]);
System.out.println("Last element of an array is "+a[size-1]);
}
}






