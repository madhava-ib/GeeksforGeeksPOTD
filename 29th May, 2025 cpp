class Solution {
  public:
    void sumOfRootToLeaf(Node* root, int sum, int len, int& maxLen, int& maxSum) {

        // Base case: if the current node is null
        if (!root) {

            // Checking if the current path has a longer length
            // and update maxLen and maxSum accordingly
            if (len > maxLen) {
                maxLen = len;
                maxSum = sum;
            }
            // If the lengths are equal, check if the current sum is
            // greater and update maxSum if necessary
            else if (len == maxLen && sum > maxSum) {
                maxSum = sum;
            }
            return;
        }

        // Recursively calculating the sum of
        // the left and right subtrees
        sumOfRootToLeaf(root->left, sum + root->data, len + 1, maxLen, maxSum);
        sumOfRootToLeaf(root->right, sum + root->data, len + 1, maxLen, maxSum);
    }

    // Function to calculate the sum of the longest root to leaf path
    int sumOfLongRootToLeafPath(Node* root) {
        // Base case: if the tree is empty
        if (!root)
            return 0;

        // Initializing the variables to store the maximum length and sum
        int maxSum = INT_MIN, maxLen = 0;

        // Calling the utility function
        sumOfRootToLeaf(root, 0, 0, maxLen, maxSum);

        // Returning the maximum sum
        return maxSum;
    }
};
