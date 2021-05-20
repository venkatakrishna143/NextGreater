# NextGreater

class Solution:
    def nextGreaterElement(self, nums1: List[int], nums2: List[int]) -> List[int]:
        
        dict_1={}
        
        stack=[]
        
        for i in nums2[::-1]:
            
            while stack and stack[-1]<=i:
                stack.pop()
                
            if len(stack)==0:
                dict_1[i]=-1
            else:
                dict_1[i]=stack[-1]
                
            stack.append(i)
            
        res=[]
        for i in nums1:
            res.append(dict_1[i])
            
        return re
