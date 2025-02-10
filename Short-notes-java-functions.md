## how to sort the matrix in Java

1. In the matrix, we sort the values based on the index value, as it treats everything as a single array

let matrix = [[2,1],[9,19],[3,14]]  --> i want to sort the matrix based on the arr[I][0] the sorting will look like this
```java
Arrays. sort( matrix, new Comparator<int[]>(){
     public int compare(int[] a,int[] b){
           return Integer.compare(a[0],b[0]);
     }
})
```


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
     #Note: please check constraints before using the counting sort.

## 2. HashMap
  ```java
       HashMap<Integer,Integer> hm = new HashMap<Integer,Integer>();
       hm.put(arr[i],hm.getOrDefault(arr[i],0)+1);
 ```


## How to fill default values in multi-dimensional Arrays, like 2-d, and 3-d in Java

  1. 2-D array declaration and filling default values
       suppose a 2-D array of rows 2 columns 2 of integer datatype in java
       int rows=2,columns=2;
       #declaration of 2-D array.
       ```java
       int[][] array = new int[rows][columns];
       ```
       #filling the default values in it.
       ```java
         for(int[] row: array){
              Arrays.fill(row,-1);
         }
       ```
   2. 3-D array declaration and filling default values
      int m=2,n=2,p=3;
      #declaration of a 3-D array
      ```java
       int[][][] array = new int[m][n][p];
      ```
      #filling the default values in it.
      ```java
         for(int i=0;i<array.length;i++){
           for(int j=0;j<array[i].length;j++){
               Arrays.fill(array[i][j],-1);
            }
        }
      ```
       
 ## How to compare the Strings in Java
     in java we can't compare the strings by "==" operator, we need to use the function to compare the two strings.

     1. equals  --> // Case sensitive comparison accounts for case of letters	
     2. equalsIgnoreCase --> Case insensitive comparison through equalsIgnoreCase

   ```java
       String str1 = "Some text";
        String str2 = "Some Text";
        System.out.println(str1.equals(str2)); --> false
        System.out.println(str1.equalsIgnoreCase(str2)); --> true
```

## How to convert String to char array vice versa
1. to convert String to char array
```java
     char[] array = str.toCharArray();
```
   2. how to convert the char array to Strin
 ```java
      1.String str1 = new String(charArray);
      2. String str2 = String.valueOf(charArray);
```

## String Builder
1. How to initialize the String Builder
```java
   StringBuilder stringBuilder = new StringBuilder();
```
2. How to add characters to String builder
```java
stringBuilder.append(character)
```
3. How to reverse the String using the String Builder
      1. if it is already a StringBuilder object
          ```java
              stringBuilder st1 = stringBuilder.reverse()
          ```
     2. if it is not a StringBuilder Object.we need to convert that String into StringBuilder then use reverse function
        ```java
              StringBuilder str2 = new StringBuilder(string);
               str2 = str2.reverse()
        ```
4. How to delete character in a String Builder Object
   ```java
        stringBuilder.deleteCharAt(index)
   ```
5. how to given character is a digit
```java
     Character.isDigit(character);
```
       
       

      



