# Algorithms

### Knapsack 0/1
 - [x] Knapsack  (bruteforce & recursion)
 - [x] Knapsack (dp)
 - [ ] Knapsack printing
 - [x] Fractional knapsack

 [Knapsack gfg](https://www.geeksforgeeks.org/0-1-knapsack-problem-dp-10/)

##### Use-cases
- Helps businesses decide which projects to fund within a budge, maximizing profit without overspending
- In logistics to optimize the loading of goods into trucks & plans, ensuring most valuable or highest prioritized items are included without exceeding weight limits

``` java
// Brute-force and recursion -  1

class Solution {
    static int maxOf(int a, int b){
        return a > b ? a : b;
    }
    static int doit(int index, int capacity, int currWt, int currVal, int val[], int wt[]){
        if(currWt  > capacity)
            return 0;
        
        if(index >= wt.length)
            return currVal;
  
        
        int dd1 = doit(index+1, capacity, currWt + wt[index], currVal + val[index], val, wt);
        int dd2 = doit(index+1, capacity, currWt, currVal, val, wt);
        return maxOf(dd1, dd2);
        
    }
    static int knapSack(int capacity, int val[], int wt[]) {
        return doit(0, capacity, 0, 0, val, wt);
    }
}

```

```java 

//  Brute force & recursion - 2

class GfG {

    static int knapSack(int W, int wt[], int val[], int n)
    {
        // Base Case
        if (n == 0 || W == 0)
            return 0;

        // If weight of the nth item is  more than Knapsack capacity W then this item cannot be included in the optimal solution
        if (wt[n - 1] > W)
            return knapSack(W, wt, val, n - 1);

        // Return the maximum of two cases:
        // (1) nth item included
        // (2) not included
        else
            return Math.max(knapSack(W, wt, val, n - 1), 
             val[n - 1] + knapSack(W - wt[n-1], wt, val, n-1));
    }

    // Driver code
    public static void main(String args[])
    {
        int profit[] = new int[] { 60, 100, 120 };
        int weight[] = new int[] { 10, 20, 30 };
        int W = 50;
        int n = profit.length;
        System.out.println(knapSack(W, weight, profit, n));
    }
}

```

```java
//Knapsack dp - top down approach

import java.io.*;

class GFG {

    // Returns the value of maximum profit
    static int knapSackRec(int W, int wt[], int val[],
                           int n, int[][] dp)
    {

        // Base condition
        if (n == 0 || W == 0)
            return 0;

        if (dp[n][W] != -1)
            return dp[n][W];

        if (wt[n - 1] > W)

            // Store the value of function call
            // stack in table before return
            return dp[n][W]
                = knapSackRec(W, wt, val, n - 1, dp);

        else

            // Return value of table after storing
            return dp[n][W]
                = Math.max((val[n - 1]
                       + knapSackRec(W - wt[n - 1], wt, val,
                                     n - 1, dp)),
                      knapSackRec(W, wt, val, n - 1, dp));
    }

    static int knapSack(int W, int wt[], int val[], int N)
    {

        // Declare the table dynamically
        int dp[][] = new int[N + 1][W + 1];

        // Loop to initially filled the
        // table with -1
        for (int i = 0; i < N + 1; i++)
            for (int j = 0; j < W + 1; j++)
                dp[i][j] = -1;

        return knapSackRec(W, wt, val, N, dp);
    }

    // Driver Code
    public static void main(String[] args)
    {
        int profit[] = { 60, 100, 120 };
        int weight[] = { 10, 20, 30 };

        int W = 50;
        int N = profit.length;

        System.out.println(knapSack(W, weight, profit, N));
    }
}

```

[code link gfg](https://www.geeksforgeeks.org/problems/0-1-knapsack-problem0945/1?itm_source=geeksforgeeks&itm_medium=article&itm_campaign=practice_card)


### More usecases

- **Resource Allocation**: Assign limited resources (time, budget, or manpower) to maximize efficiency or impact (e.g., project selection, cloud computing).
- **Budget Management**: Optimize the distribution of funds across competing priorities, like marketing campaigns or personal investments.
- **Logistics and Supply Chain**: Maximize cargo value within weight or volume constraints (e.g., truck or plane cargo loading).
- **Portfolio Optimization**: Select financial assets (stocks, bonds) to maximize returns or minimize risk within a budget.
- **Task Scheduling**: Assign tasks to resources (time, workers) for maximum productivity, given constraints.
- **Data Storage**: Allocate limited storage space to store the most valuable or frequently accessed data.
- **Manufacturing Optimization**: Determine the product mix to maximize profit with resource constraints (materials, labor, time).
- **Healthcare Resource Allocation**: Optimize the use of medical resources (staff, equipment) for the best patient outcomes.
- **E-commerce Inventory Management**: Stock the most profitable items given storage capacity or select items for promotions.
- **Renewable Energy Storage**: Store surplus energy in batteries to maximize usage efficiency under capacity limits.
