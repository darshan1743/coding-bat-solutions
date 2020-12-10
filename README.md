# coding-bat-solutions


// can balance array3.....

public boolean canBalance(int[] nums)
{
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

public int[] squareUp(int n)
{
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

//coprime

class coprime
{  
	public static int co(int a,int b)
	
  {
	int c=0;
	for(int i=2;i<=a && i<=b;i++)
	{
	if(a%i==0 && b%i==0)
	c++;
	}
	return c;
  }
  

      public static int  check(int[] a)
	
	{
		int c=0;
   
     for(int i=0;i<a.length;i++)
     {
     for(int j=i;j<a.length;j++)
      {
     	if(co(a[i],a[j])==0)
     		c++;
      }
	 }
	 return c;
    }
    
	public static void main(String[] args)
        {
    	int[] array={4,20,8,9};
        System.out.println(check(array));
	}
}



//nth occurance of a number


class occu
{
    public static int search(int val,int a,int[] ar)
	{
	int c=0;
       for(int i=0;i<ar.length;i++)
      {
      	if(ar[i]==val)
      	{
          c++;
      	}
      	if(c==a)
      	return i;
      }
      return 0;
	}
	public static void main(String[] args)
	 {
	 	int[] arr={1,4,6,7,6,3,6};
		System.out.println(search(6,2,arr));
	}
}


