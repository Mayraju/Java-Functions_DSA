## how to sort the matrix in Java

1. In the matrix, we sort the values based on the index value, as it treats everything as a single array

let matrix = [[2,1],[9,19],[3,14]]  --> i want to sort the matrix based on the arr[I][0] the sorting will look like this

**Arrays. sort( matrix, new Comparator<int[]>(){
     public int compare(int[] a,int[] b){
           return Integer.compare(a[0],b[0]);
     }
})**


## How to count How many times a key occurred in the array.

Example:  int[] arr = [1,1,2,2,3,3]

in the above array, 1 appeared 2 times, 2 appeared 2 times, 3 appeared 2 times

How do you count the above numbers?

we have two ways
1. counting sort
2. HashMap

## 1. Counting sort


     create the array, "with no of elements in the array + maximum element + 1"
     Example: n = 1000000, maximum element in the array = Math.pow(10,9) 
     for the above example, we get errors like below
     in some cases stack overflow or heap size is not sufficient for large input values, in that case, we go for hashmap.
     ### Note: please check constraints before using the counting sort.

    


## 2. HashMap

       hm.put(arr[i],hm.getOrDefault(arr[i],0)+1);



