class Solution {
public:
    int minOperations(vector<int>& nums) {
    map<int,bool>mp; // check duplicate elements using map
    for(int i=0;i<nums.size();i++)
    {
        // duplicate element present then make 1e9+7 
        if(mp[nums[i]]==true)
        nums[i]=1e9+7; 
        else
        mp[nums[i]]=true;
    }
    //sort array 
    sort(nums.begin(),nums.end());
    int max_right_len=0;
    for(int i=0;i<nums.size();i++)
    {
        int val=nums[i];
        if(val!=1e9+7)
        {
            int target=val+nums.size()-1;
            int index=upper_bound(nums.begin(),nums.end(),target)-nums.begin();
            index--;
            max_right_len=max(max_right_len,index-i+1);
        }
    }
    return nums.size()-max_right_len;
    }
};
