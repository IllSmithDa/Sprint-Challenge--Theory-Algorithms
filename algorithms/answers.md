1. 
    a. This seems to be a standard while loop with a initialized to 0. A while loops simply just 
    iterates until the end of loop is reached. Therefore the run time in Big O should simply be 
    O(n)

    b. While this does add an additional step of finding the length, it is merely a constant which 
    isn't not taken into account in run time especially in Big O. Therefore, the run time should still 
    be O(n).

    c. This functinons contains three for loops with the two inner for loop's run time being O(n). Thw two inner loops is guarnteed to run through the entire iteration. However, the outer for loop The total run time in Big O is more toward log n because it only runs half of iteration that the two inner loops are running assuming that n here is the length of the array. Therefore the Big O is 
    O(n^2 log n). 

    d. The Outer loop is logarithmic as it only iterates through half the data making it O(log n). The inner loop is a standard iteration through the array making it O(n). By combining the two, we are able to get a run time of O(n log n).

    e. There are a total for 4 for loops and non of them seem to be logarithmic as each loop seems to iterate through most if not all the data set. Therefore, the appropriate run time appears to be
    O(n^4). At this point, the algorithm reaches close to or reaches to exponential run time. 

    f. This seems to be a mere recursive iteration until the base case bunnies = 0 is reached. An algorithm like this will usually have a run time of O(n) regardless of the constant '2' in the return 
    statement. Therefore, the run time in Big O is O(n). 

    g.  This is a search algorithm that seems to have a average of O(n) as its runtime. While it is possible that in a best case scenario the first item matches giving it a o(1) runtime, on average it will probably take longer than that. It does iterate through entirely in the worse case scenario and doesn't seem to have means of divide and conquer which would have gave it a O(log n) runtime. Therefore, the runtime that seems to match the algorithm best is O(n).

    2. 

    a. Given an array a of n numbers, design a linear running time algorithm to find the maximum value of a[j] - a[i], where j ≥ i.
    
    a[j], a[i] n = number of elements in the array or a.length -1; where j >=i; search iteratively

    let highestVal = 0;
    for (let i = 0; i <= n; i++) {
        let j = i + 1;
        if(arr[j] - arr[i] > highestVal) {
            highestVal = arr[j] - arrr[i];
        }
    }
    return highestVal;


    b. Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg is broken if it is thrown off floor f or higher, and unbroken otherwise. Devise a strategy to determine the value of f such that the number of dropped eggs is minimized.
        
        // O(n) runtime version of egg drop
        let n = buildingArr.length; 
        
        //increment floor levels until the floor f is met where the eggs dropped is breaking 
        for (let i = 0; i < n; i++) {
            if (buildingArr[i] == f) {
                // floor where egg is broken 
                return buildingArr[i];
            }
        }   
    You can also use a divid and conquer strategy such as a binary search tree to find the floor faster with a runtime of o(log n) by dividing array into left array and right array by the midpoint or dividing buildArr by 2 and and if f is greater than the midpoint, iterate through the right or greater array. If f is less than midpoint, iterate though left array or less array until f match is found. 
    

    3.
    a. Since the less quicksort is neverg going to be used as the pivot is always chosent to be first element which means that x will always be greater than pivot assuming array is sorted. The finding of pivot itself is O(1) as you are always finding the first element. The rest is merely appending every value to greater quicksort and it seems to simply iterate without dividing anything when first elemnt is the pivot evn though it is technically divide and conquer. The recursive function itself is also iterating which makes this two O(n) which makes it a quadratice algorithm with a total run time of 
    O(n^2). 

    b. Now that both quicksort are running, The divide and conquer method seems to actually work which could make one of the processes a log n. However, one problem with this idea is that the amount of work is still the same as the for each still seems to iterate through the entire array and just appends differently to the lesser array rather than the entire array to the greater array. It still iterates the entire array which still leaves the run time at O(n^2).