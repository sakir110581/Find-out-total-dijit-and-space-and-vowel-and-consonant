# Find-out-total-dijit-and-space-and-vowel-and-consonant-by-JAVA
 
package finddigit;

import java.util.Scanner;

public class finddigit {
	
	private static Scanner scan;

	public static void main(String[] args) {
		System.out.print("\n\nEnter your full paragraph::::::");
		
		scan = new Scanner(System.in);
		String paragraph = scan.nextLine();
		int length = paragraph.length();
		
		char paragraphc[] = paragraph.toCharArray();
		String vowel="aeiouAEIOU";
		char vowelc[] = vowel.toCharArray();
		
		int vowelcount=0,ccount=0,i,j;
		for(i=0;i<length;i++) {
			for(j=0;j<10;j++) {
				if(paragraphc[i]==vowelc[j]) {				
					vowelcount++;
				}
			}
			
			
		}
		String latter="BCDFGHJKLMNPQRSTVWXYZbcdfghjklmnpqrstvwxyz";
		char latterc[] = latter.toCharArray();
		
		for(i=0;i<length;i++) {
			for(j=0;j<42;j++) {
				if(paragraphc[i]==latterc[j]) {				
					ccount++;
				}
			}
			
			
		}
		int space =length;
		space =space - vowelcount;
		space =space -ccount;
		
		System.out.println("Total dejit is:"+length+"\ntotal vowel is:"+vowelcount+"\nAll consonant is::"+ccount+"\nTotal space is::"+space);
		

	}

}
