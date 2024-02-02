 * Used to reduce multiple variables into one
 * uncorrelated
 * follows eigen decomposition 
   * var1=[1,2,...],var1=[1,2,...],var1=[1,2,...]
     * get the center of var and fit a linear line on it
     *  PC1 = -best fit line, PCE next orthogonal and continues....
     * to calcukate sample varience 

                           PC2
                           │
                           │
                           │
                           │
                           │
                           │
                           │
                           │
                           │
                           │
                           │
           *               │
           |E2-----E1------▼
      PC1 ───────────────────────────────────────|
                           -------------- * E1   |E2

 * Since E1 is the best fit for the data, its varience from the center will be the highest
 * Decide PC count from the varience tollerted

 * In simple words splitting data to multiple columns
