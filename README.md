# coding-bat-solutions


// can balance array3.....

public boolean canBalance(int[] nums) {
  int tsum=0;int sum=0;int n=0;
  for(int i=0;i<=nums.length-1;i++)
  {
    sum=sum+nums[i];
  }
  tsum=sum/2;
  for(int i=0;i<=nums.length-1;i++)
  {
    n=n+nums[i];
    if(n==tsum && sum-n==tsum  )
    return true;
  }
  return false;
}


//array3...squareup...

public int[] squareUp(int n) {
  int c=0; 
  int[] a=new int[n*n];
  for(int i=0;i<n;i++)
  {
    int num=i+1;
    for(int j=0;j<n-(i+1);j++)
      {
        a[c]=0;c++;
      }
      for(int k=0;k<=i;k++)
      {
        a[c]=num;c++;num--;
      }
  }
  return a;
}
