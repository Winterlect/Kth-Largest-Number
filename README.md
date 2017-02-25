# Kth-Largest-Number
Just a code depicting the Kth largest number in a series of numbaaaahs


import java.io.PrintWriter;
import java.util.Scanner;

public class main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		System.out.println("T'Sup (;-;) (-_-)");
		
		Scanner in = new Scanner(System.in);	
		PrintWriter out = new PrintWriter(System.out);
		
		String N;
		N = in.nextLine();
		
		int k = Integer.parseInt(N);
		
		String[] nums = in.nextLine().split(" ");
		
		int[] arr = new int [nums.length];
		
		for(int i = 0; i < nums.length; i++){
			
			arr[i] = Integer.parseInt(nums[i]);
			
		}
		
		sort(arr);
		
		out.println(arr[k-1]);
		
		out.close();
		
		
	}
	
	public static void swap(int[] arr, int aLoc, int bLoc){
		
		int tmp = arr[aLoc];
		
		arr[aLoc] = arr[bLoc];
		
		arr[bLoc] = tmp;
		
		
	}
	
	public static void sort(int[] arr){
		
		for(int i = 0; i < arr.length; i++){
			
			int maxLoc = i;
			
			for(int search = i + 1; search <arr.length; search++){
				
				if(arr[maxLoc] < arr[search]){
					
					maxLoc = search;
					
				}
			}
			
			swap(arr,maxLoc,i);
			
			
			
		}
		
	}

}
