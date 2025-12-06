Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1]

public class TwoSum {
    public int[] twoSum(int[] nums,int target)
    {
        int i,j;
        int[] result=new int[2];
        for(i=0;i<nums.length;i++)
        {
            for(j=i+1;j<nums.length;j++)
            {
                if(nums[i]+nums[j]== target)
                {
                    result[0]=i;
                    result[1]=j;
                    break;
                }

            }
        }
        return result;
    }
    public static void main(String[] args)
    {
        int[] nums={2,7,11,15};
        int target=9;
        TwoSum ts=new TwoSum();
        int[] res=ts.twoSum(nums,target);
        System.out.println("["+res[0]+","+res[1]+"]");
    }
}
