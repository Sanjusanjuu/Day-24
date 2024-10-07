#include <iostream>
#include <vector>
using namespace std;

int f(vector<int>& nums) {
    int maxCount = 0;
    int currentCount = 0;
    for (int num : nums) {
        if (num == 1) {
            currentCount++;
            maxCount = max(maxCount, currentCount);
        } else {
            currentCount = 0;
        }
    } 
    return maxCount;
}

int main() {
    int n;
    cin >> n;
    vector<int> arr(n);
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }
    int res = f(arr);
    cout << "The maximum number of consecutive ones is: " << res << endl;
    return 0;
}
