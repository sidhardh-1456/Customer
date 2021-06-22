# Customer
public boolean redeemPoint(String customerId, String amount)
{ 

if(customerId!=null && !customerId.isEmpty() && amount!=null && !amount.isEmpty()) {
			Double toRedeem = Double.valueOf(amount); 
			double currentPoints = myService.getPoints(customerId); 
			double newPoints = currentPoints - toRedeem; 
			myService.save(customerId,newPoints); 
			log.info("Points redeemed for customer {}",customerId); 
			return true; 

		}
		return false; 
    
    
    
    package test;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class bsort {

				
		public static void sortStrings (String[] arr, int n) {
			
			String temp;
			
			for (int j = 0; j < n; j++) {
				for (int i = j + 1; i < n; i++) {
					if (arr[j].compareTo(arr[i]) > 0) {
						temp = arr[j];
						arr[j] = arr[i];
						arr[i] = temp;
					}
				}
			}
 		}
		
		public static void main(String[] args) {
			
			
			String arr1[]= {"a","c","d","f","g"};
	    	String arr2[]= {"e","b","h"};
	         List<String> list = new ArrayList<String>();
	        list.addAll(Arrays.asList(arr1));
	        list.addAll(Arrays.asList(arr2));
	        String arr[] = list.toArray(new String[list.size()]);
			int n = arr.length;
			sortStrings(arr, n);
			System.out.println("Final array : "+Arrays.toString(arr));
			
	}
}

