class Solution {
  public:
    int uniquePaths(vector<vector<int>> &grid) {
        int r = grid.size(), c = grid[0].size();

        // Initialize DP array with zeros
        vector<int> dp(c, 0);

        // Set the starting cell if there's no obstacle
        dp[0] = (grid[0][0] == 0) ? 1 : 0;

        // Fill the DP array for each row
        for (int i = 0; i < r; i++) {
            for (int j = 0; j < c; j++) {

                // If there's an obstacle, set dp[j] to 0
                if (grid[i][j] == 1) {
                    dp[j] = 0;
                } else if (j > 0) {

                    // Add the value from the left cell
                    dp[j] = (dp[j] + dp[j - 1]);
                }
            }
        }

        // Return paths count for the bottom-right cell
        return dp[c - 1];
    }
};
