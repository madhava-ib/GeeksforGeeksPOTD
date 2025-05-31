class Solution {
  public:
    // Function to count the number of elements less than or equal to x
    int countSmallerEqual(const vector<vector<int>>& matrix, int x) {
        int n = matrix.size();
        int count = 0;
        int row = 0;
        int col = n - 1;

        // Traverse from the top-right corner
        while (row < n && col >= 0) {
            if (matrix[row][col] <= x) {
                // If current element is less than or equal to x,
                // all elements in this row up to the current column are <= x
                count += (col + 1);
                row++;
            } else {
                // Move left in the matrix
                col--;
            }
        }

        return count;
    }

    int kthSmallest(vector<vector<int>>& matrix, int k) {
        int n = matrix.size();
        int low = matrix[0][0];
        int high = matrix[n - 1][n - 1];
        int ans = 0;

        while (low <= high) {
            int mid = low + (high - low) / 2;

            // Count elements less than or equal to mid
            int count = countSmallerEqual(matrix, mid);

            if (count < k) {
                // If there are less than k elements <= mid, the kth smallest is larger
                low = mid + 1;
            } else {
                // Otherwise, mid might be the answer, but we need to check for smaller
                // values
                ans = mid;
                high = mid - 1;
            }
        }

        return ans;
    }
};
