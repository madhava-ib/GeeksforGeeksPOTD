class Solution {
  public:
    bool pythagoreanTriplet(vector<int>& arr) {
        int n = arr.size();
        int maxEle = 0;
        for (int ele : arr)
            maxEle = max(maxEle, ele);
        vector<bool> vis(maxEle + 1, 0);
        for (int ele : arr)
            vis[ele] = true;
        for (int a = 1; a <= maxEle; a++) {
            if (vis[a] == false)
                continue;
            for (int b = 1; b <= maxEle; b++) {
                if (vis[b] == false)
                    continue;
                int c = sqrt(a * a + b * b);
                if ((c * c) != (a * a + b * b) || c > maxEle)
                    continue;
                if (vis[c] == true) {
                    return true;
                }
            }
        }
        return false;
    }
};
