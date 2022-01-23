# case-study
<pre>
1. From the data it is clear that there is uneven use of resources during a day.
   The following can be inferred from the data:
    
    There are 3 cycles of Peak load, wherein peak load in evening is the highest.
    
   -Compute resources starts getting peak load from the evening .i.e. from 4 PM and stays till 6:30 PM approximately.
   -The average load during this Peak being 8323 and the max load being 13760.
   
   -Next Peak load is observed at midnight 12 am and lasts for approx 5 mins.
   -The average load during this peak being 4707 and the max load being 6072.
   
   -Peak load at morning is observed at 9:30 am for a shorter period of time.
   -The max and average load in the case is 5989.
   
   At all other instances, we have underusage of resources.
  
   
2. From my observation, the missing timestamps infer 'ideal resource usage'. That is, during this time resources usage was approximately near to 4000. The listed timestamp shows abnomalies in resource usage either underusage/overusage.

<br/>

3. The current sum of total realtime load and sum of total alloted resources stands at 83178 & 88000 respectively.
   It is evident that resources are underutilized with 4000 provisioning. If we go on increasing the resources by 100, 200, 300..etc we will widen the total gap. Not only this, we will also widen the gap where resources are underutilized in 4000 provisioning. For ex - In 11:52:56 , Computation capacity being used is 5 whereas provisioned load is 4000. So, Increasing the load for this timeframe will widen the gap even more.


   Based on the given data we see there is a pattern of compute usage, that is we have a predictable workload. 
   so, my solution to this problem is 'time scheduling of resources'.
   Here, we will not fix 4000 for every part of the day. Rather, we will divide it into segments.
            
   Midnight Segment: Current Provisioning: 4000 
                     Revised Provisioning: 4707 (Avg of segment)* 
                    
   Evening Segment: Current Provisioning: 4000 
                    Revised Provisioning: 8323 (Avg of segment)
                    
   Morning Segment: Current Provisioning: 4000 
                    Revised Provisioning: 4374 (Avg of segment)                   
                    
   Similarly, for underused segments the provisioning can be lowered based on its average.
   * Assuming the Peak Load remains in the same range everyday
   
   For Ex - In 1st Row:
   Initial Provisioning: 4000
   Revised Provisioning: 4707
   Assuming price for reserved Instance (X) is Re 1.
   On Demand Cost based on IP: (6207-4000) * Rs 2 = Rs 4144 
   On Demand Cost based on RP: (6207-4707) * Rs 2 = Rs 2730
   
   We can also take the Max value as the Revised provisioning value for a segment, but we don't know the exact value.
   
   This method of scheduling Reserved Instances based on predictable workload is possible and is 20-30% cheaper than On demand Instances.
   
   </pre>
   
                    
   
   
   
