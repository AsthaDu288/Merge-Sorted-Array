# Merge-Sorted-Array
#Two sorted integer arrays nums1 and nums2, merge nums2 into nums1 as one sorted array.
class Solution {
    public void merge(int[] nums1, int m, int[] nums2, int n) {
        
        int i=0;int j=0;int k=0;
        int nums1Len = m;
        int nums2Len = n;
        int[] ar = new int[nums1Len+nums2Len];
       while(i<nums1Len && j<nums2Len){
                   if(nums1[i]<nums2[j]){
                       ar[k++]=nums1[i++];
                   }
                   else{
                       ar[k++]=nums2[j++];
                      
                   }
       }
        while(i<nums1Len)
            ar[k++]=nums1[i++];
           
        
        while(j<nums2Len)
               ar[k++]=nums2[j++];
                      
           System.arraycopy(ar,0,nums1,0,nums1.length);
              
       }
           
        
        
    }
      
 
    
