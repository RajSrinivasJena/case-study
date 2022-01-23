# case-study

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

3. Based on the given data we see there is a pattern of compute usage, that is during which part of day resources are over and under utilized. 
   so, my solution to this problem is 'time scheduling of resources'. Here, we will not fix 4000 for every part of the day. Rather, we will divide it into peak and ideal   
   categories.
   For ex - For Midnight peak, we can provision 6000
            For Evening Peak, We can provision 6000 and 10000
            For Idle conditions, we can provision 
   Scheduled reserved instance for predictable workload.
   
   
