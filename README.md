# PAL-NDROM
ürünün palindrom olup olmadığını belirleyen kod
package lessoneleven;

import java.util.Scanner;

public class ApplicationOne {

	public static void main(String[] args) {


		Scanner s = new Scanner(System.in);
		System.out.print("Bir metin giriniz: ");
		String text = s.nextLine();

		System.out.println(text + "'nin tersi: " + reverseText(text));
		System.out.println(text + "'in sesli sayısı: " + vowelNumber(text));
		System.out.println(text + " palindrom mu?: " + isPalindrome(text));

	}

	public static String reverseText(String text) {
		String reverse = "";
		for (int i = 0; i <= text.length() - 1; i++) {
			reverse = text.charAt(i) + reverse;
		}
		return reverse;
	}

	public static int vowelNumber(String text) {
		int sum = 0;
		for (int i = 0; i <= text.length() - 1; i++) {
			switch (text.charAt(i)) {
			case 'a', 'e', 'i', 'o', 'u', 'ö', 'ü':
				sum++;
			}
		}
		return sum;
	}

	public static boolean isPalindrome(String text) {
		return text.equals(reverseText(text)) ? true : false;
	}

}

