class Solution {
  public:
    int countPairs(vector<vector<int>> &mat1, vector<vector<int>> &mat2, int x) {
        // Indices for pointing current element in mat1 and mat2
        int r1 = 0, c1 = 0;
        int r2 = mat2.size() - 1, c2 = mat2[0].size() - 1;

        int count = 0;

        // While there are elements in both matrices
        while (r1 < mat1.size() && r2 >= 0) {
            int val = mat1[r1][c1] + mat2[r2][c2];

            if (val == x) {
                count++;

                // Move mat1 column `c1` to right
                // and mat2 column `c2` to left
                c1++;
                c2--;
            } else if (val < x) {
                c1++; // Move mat1 column `c1` to the right
            } else {
                c2--; // Move mat2 column `c2` to the left
            }

            // If `c1` crosses the right boundary of mat1
            if (c1 == mat1[0].size()) {
                c1 = 0; // Reset column index
                r1++;   // Move to the next row in mat1
            }

            // If `c2` crosses the left boundary of mat2
            if (c2 == -1) {
                c2 = mat2[0].size() - 1; // Reset column index
                r2--;                    // Move to the previous row in mat2
            }
        }

        return count;
    }
};
