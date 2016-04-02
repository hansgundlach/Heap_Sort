package GithubNewHeapSort;

import java.util.Arrays;

public class Heap_Sort {
	//to learn more about algorithmns I am making a heap sort program.
	//I think the programs I have plus this is good.
	
	public static void main(String args[]){
		//this is the array that is going to be sorted
		int[] start = new int[]{-1,3,5,2,9,7,5,18,3,25,1};
	maxHeaping(start,start.length);
	System.out.println(Arrays.toString(start));
	heapSort(start, start.length);
	System.out.println(Arrays.toString(start));
		
	}
	
	
	//combines all the methods to finally sort 
	public static void heapSort(int[] unord , int count ){
		 int last = unord.length  - 1 ;
		maxHeaping(unord,unord.length);
		while (last > 0 ){
		
		//swaps begining and last elements
		int end = unord[last];
		unord[last] = unord[0];
		unord[0] = end;
				
		last--;
		siftDown(unord, 0, last);
		
		}
		
		}
	// I understand that count is not so good however other alternatives include using temporary arrays
	//and then find a subarray
	//maxHeap will build in ascending order
	public static void maxHeaping(int[] unheap, int number){
		int start =  (number-2)/2;
		while(start >=0 ){
			
			siftDown(unheap, start,number-1);
			start = start-1;
			
		}
		
	}
	
	//this maxheapify is wrong
	//ask if it is good fashion to have the size in there
	public static void maxHeapify(int[] input,int i){
		//count used to be input.length
		int lasted = i;
		
		//is my code a little less efficient 
			//checks the left node and switches if bigger
			if(2*i+1<input.length && input[i]<input[2*i+1] ){
			//   int stable = input[i];
				//input[i] = input[2*i+1];
				//input[2*i+1] =  stable;
				lasted = 2*i+1;
				
				
				
				
			//checks right node and switches if bigger 
			}if(2*i + 2<input.length && input[i]<input[2*i + 2]){
				//int nextStable = input[i];
				//input[i] = input[2*i + 2];
				//input[2*i+ 2]= nextStable;
				lasted = 2*i+2;
				
			}if(lasted != i){
				int stable = input[i];
				input[i] = input[lasted];
				input[lasted] = stable;
				//this is heading down the heap
				maxHeapify(input, lasted);
			}
		
		//return input;
	}
	
	
	
	public static void maxHeap(int[] start){
		//I think i>0 check if it could be just bigger than 1
	
	for(int i = start.length/2;i>0;i--){
	maxHeapify(start,i);
	
	
	}
	}
	
	
	
public static void siftDown(int[] sift , int start, int end){
	  //more efficent then calling maxHeap again
		int root = start;
		//I think this is +2 but it vould be +1 
		//the equal to n case is casuing a erro 
		while(root * 2 + 1 <= end){
			int child = root*2 + 1;
			int swap = root;
			//if parent is less then child 
			if(sift[swap]<sift[child]){
				swap = child;
			}if(child+1 <= end && sift[swap] < sift[child+1]){
				swap = child+1;
			}if(swap == root){
				return ;
			}else{
				//swapping root and swap elements
				int nroot = sift[root];
				sift[root] = sift[swap];
				sift[swap] = nroot;
				root = swap;
			}
			
			
		}
		}

}
