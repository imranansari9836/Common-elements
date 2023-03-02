class Solution
{
    ArrayList<Integer> commonElements(int A[], int B[], int C[], int n1, int n2, int n3) 
    {
        ArrayList<Integer> arr=new ArrayList();
        int x=0,y=0,z=0;
        int count=0;
        while(x<A.length && y<B.length && z<C.length)
        {
            if(A[x]==B[y] && B[y]==C[z])
            {
                if(count!=A[x])
                {
             arr.add(A[x]);
             count=A[x];
                }
             x++;
             y++;
             z++;
            }
            else if(A[x]<B[y])
            {
                x++;
            }
            else if(B[y]<C[z])
            {
                y++;
            }
            else
            {
                z++;
            }
        }
        return arr;
    }
}
