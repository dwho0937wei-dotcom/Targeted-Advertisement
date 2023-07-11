1. My Project Organization

This practical application assignment 5.1 is organized as its initial state but with 'All-5-Investigations-Combined_Daniel-Ho' Jupyter Notebook showing my complete investigation/conclusion/recommended-action for all 5 coupons (Bar, <20 Restaurant, 20-50 Restaurant, Coffee House, Carry Out & Take Away).

I personally thought the specified notebook may be too long for the grader to grade properly so I decided to create a folder called 'Separate-Investigations' which separates the notebook into five shorter ones, each investigating a distinct coupon. That way, the grader can review each of my coupon investigation one at a time instead of going through all five at once. 
The Intro (Context, Overview, Data, Deliverables), Data Description, and the Problems that were initially there along with my work will appear in all five as they provide the grader context and also involves my work of data cleaning which is essential before the investigation.

However, if you as the grader want to review the complete project in one notebook, then you can just simply review 
'All-5-Investigations-Combined_Daniel-Ho' and forget about the folder 'Separate-Investigations'.


2. Summary Findings

Now onto summarizing what I have found after investigating each coupon.

    2.1 Bar Coupon
        Following the given instructions, the pie chart showed that 41.2% of all users who received the bar coupon accepted the coupon.               
        Some pie charts have shown that most users who either:
            monthly visit bars more than 3 times,
            monthly visit bars at least once and are over 25 years old,
                             ^               and are less than 30 years old
                             ^               and have no kids as passenger and don't work for Food, Fishing, & Forestry,
         or                  ^                           ^                 and are not widowed,
        have accepted the coupon.
         
        Other pie charts have shown that most users who either:
            monthly visit bars at most 3 times,
            monthly visit bars less than 1 or aged over 25,
         or monthly visit cheap (<20) restaurants at least 4 times and have an income of less than $50k
        have rejected the coupon.
        
        This led me to hypothesize that users aged 25-30 who visited the bar at least once while having no kids as passenger, never getting widowed, and not working for Farming, Fishing, & Forestry are the most likely people to accept the bar coupon.
        
    2.2 Cheap (<$20) Restaurant Coupon
        A pie chart showed that 70.9% of all users who received the cheap restaurant coupon accepted the coupon.
        Comparing this pie chart to another two pie charts that query the users in visiting the cheap restaurant at least once and then more than 3 times, I saw that the acceptance rate slightly increase to 71.7% and then 73% respectively.
        When querying users to only monthly visit the restaurant less than 1 or never visit at all, the acceptance rate decreases to 67.2%.
        Thus, I figured that those who visit the cheap restaurants more are more likely to accept the coupon for these restaurants.
        
        For further exploration, I decided to create my own set of 6 conditions, each with a pie chart that represents the acceptance rate of coupons from users that meet the condition and another pie chart that shows the acceptance rate of users who don't meet it.
        Note that I build my conditions based on my previous findings of previous conditions.
        I find the following:
            users who monthly visit cheap restaurants at least once but monthly visit expensive restaurants less than 1:
                meet condition: 70.1% accept the coupon
                    don't meet: 71.7% accept the coupon
                    
            users who monthly visit at least once on both cheap and expensive restaurants
                meet condition: 74.3% accept
                    don't meet: 69.3% accept
                    
            users who monthly visit a cheap and expensive restaurants at least once and has an income less than $50k:
                meet condition: 75.8% accept
                    don't meet: 70.1% accept
                    
            users who monthly visit a cheap and expensive restaurants at least once and has an income less than $25k:
                meet condition: 70.5% accept
                    don't meet: 70.9% accept
            
            users who monthly visit a cheap and expensive restaurants at least once and has an income more than $50k:
                meet condition: 73.2% accept
                    don't meet: 70.4% accept
                    
            users who monthly visit a cheap and expensive restaurants at least once and has an income between $37.5-62.5k:
                meet condition: 78.3% accept
                    dont' meet: 70.1% accept
                    
        With the last condition showing the highest increase in acceptance rate for those who meet the condition, 
        I hypothesize that users with an income between $37.5-62.5k that monthly visit both cheap and expensive restaurants more than once will more likely accept the cheap restaurant coupon.   
    
    2.3 Expensive ($20-50) Restaurant Coupon
        A pie chart showed that 44.6% of users who received the expensive ($20-50) restaurant coupons accepted the coupon.
        My intuition is that expensive restaurants are usually fancy so I thought they would provide the best meal time for romantic couples. 
        When querying users who currently have their married partner with them as passenger, the pie chart showed that 62.5% accepted the coupon, higher than 44.6%.
        For users who have their unmarried partner with them as passenger, the pie chart showed 59% accepted the coupon, lower but still higher than 44.6%
        When building a barplot that captured the proportion of users who accept the coupon or not while having a partner as their passenger in five distinct marital status,
        I realized that those who were widowed were the only one who were less likely to accept the coupon while others would more likely do so.
        I also confirmed that counting all users that don't have a partner as their passenger, I have 42.7% accepting the coupon, lower than 44.6% even if just slightly.
        
        Therefore, I hypothesize that users with a partner as their passenger will more likely accept the expensive restaurant coupon unless the user is widowed.
    
    2.4 Coffee House Coupon
        A pie chart showed that 49.6% of users who received the coffee house coupon accepted the coupon.
        I would intuitively see coffee as a morning beverage that gives people energy when drank.
        Therefore, I used a barplot to measure the proportion of users who accepted the coupon or not based on the time they are driving.
        Users who drive at 10AM and 2PM are more likely to accept the coupon. 
        I was surprised that users driving at 7AM are less likely to accept it.
        Ignoring the 2PM since the 10AM had a higher likelihood, I wanted to see if the reason that the 10AM users are keen to get the coffee house coupon is because they are old but I found out that it is most likely not the case since most 10AM users receiving the coffee house coupon were aged 21.
        Focusing my attention to users' monthly visit to the coffee house, I used a heatmap of CoffeeHouse (Monthly Visit) vs. Y (Acceptance) to find that for users who have monthly visited the coffee house at least once have a higher density in its Y=1 area than its Y=0 area. The users who monthly visited the coffee house 1-3 times have a significantly higher density with 0.17 on its Y=1 area and only 0.094 on its Y=0 area.
        I then confirm this likelihood by creating a pie chart based on users who drive at 10AM and monthly visit the coffee house at least once and I receive a whopping 81.1% of users accepting the coupon.
        Comparing to all other users, the pie chart shows a decrease of accepting the coupon to 45.9% compared to 49.6% of the first pie chart.
        
        In conclusion for this coupon, I hypothesize that users who drive at 10AM and monthly visited the coffee house at least once are very keen on accepting the coffee house coupon.
    
    2.5 Carry Out & Take Away Coupon
        The pie chart showed that 73.8% of users who received the Carry out & Take away coupon accept the coupon.
        Considering this is a coupon about picking up food, I thought it would have been convenient for the users to pick up the food as they are going towards their destination. 
        However, the pie chart of only users that can pick up food while going to the same direction as their destination showed that only 70.6% accepted the coupon while the pie chart of only users who need to go to the opposite direction from the destination to pick up the food showed that 75.4% accepted the coupon. 
        Why is there a higher proportion of users willing to go to the opposite direction to use the coupon than ones going to the same direction? 
        I thought it was unintuitive to think users like to go to the opposite direction of their destination rather than the same direction so I figured that perhaps users just happen to be very near their pick-up food location that it didn't matter.
        Sure enough, I later found out that all users who receive this coupon are only 5 minutes away of driving to pick up their food according to column 'toCoupon_GEQ5min' all being '1'.
        The 5 minute drive may be the important factor of why many users accepted the coupon to begin with.
        Using heatmap Y (Acceptance) vs. destination, I surprisingly found out that the Y=1 and destination='No Urgent Place destination' has the highest density 0.31,
        and as for the heatmap Y (Acceptance) vs. CarryAway (Monthly Visit), it has a very high density on area Y=1, CarryAway=1~3 with proportion 0.27 and area Y=1, CarryAway=4~8 with proportion 0.26, both way higher than its Y=0 area (0.095 and 0.085 respectively). Area Y=1, CarryAway=gt8 is a lot lower with proportion 0.098 but still higher than its Y=0 area with proportion 0.032.
        
        Therefore, in conclusion, I hypothesize that as long as users are within 5 minutes away of driving from using their to-go coupon, they will likely accept it. They will even more likely do so if they are not going anywhere urgent and they have monthly picked up food at least once.
      
      
3. My Jupyter Notebooks
    To navigate to my notebook containing all 5 coupon investigation, click the following link:
        https://github.com/dwho0937wei-dotcom/Module5_Project/blob/main/All-5-Investigations-Combined_Daniel-Ho.ipynb 
    
    If you want to review my distinct coupon investigation in separate notebooks, then are my five separate ones:
        Bar Coupon:
            https://github.com/dwho0937wei-dotcom/Module5_Project/blob/main/Separate-Investigations/1st-Investigation_Bar-Coupons_Daniel-Ho.ipynb
        
        Cheap (<$20) Restaurant Coupon:
            https://github.com/dwho0937wei-dotcom/Module5_Project/blob/main/Separate-Investigations/2nd-Investigation_Cheap-Restaurant-Coupons_Daniel-Ho.ipynb
        
        Expensive ($20-50) Restaurant Coupon:
            https://github.com/dwho0937wei-dotcom/Module5_Project/blob/main/Separate-Investigations/3rd-Investigation_Expensive-Restaurant-Coupons_Daniel-Ho.ipynb
        
        Coffee House Coupon:
            https://github.com/dwho0937wei-dotcom/Module5_Project/blob/main/Separate-Investigations/4th-Investigation_Coffee-House-Coupons_Daniel-Ho.ipynb
        
        Carry out & Take away Coupon:
            https://github.com/dwho0937wei-dotcom/Module5_Project/blob/main/Separate-Investigations/5th-Investigation_Carry-Out-And-Take-Away-Coupons_Daniel-Ho.ipynb
