# del-mid
class Solution
{
    public:
    //Function to delete middle element of a stack.
    void deleteMid(stack<int>&s, int sizeOfStack)
    {
        // code here.. 
            int mid=ceil((sizeOfStack+1)/2);
            int count=sizeOfStack+1;
            helper(s,count,mid);
    }
    void helper(stack<int>&s,int &count,const int &mid)
    {
        count --;
        if(count==mid)
        {
            s.pop();
            return ;
            
        }
        int temp=s.top();
        s.pop();
        helper(s,count,mid);
        s.push(temp);
    }
};
