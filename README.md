This notebook includes my work on the data preparation and data clustering of the Brazilian E-Commerce Public Dataset by Olist version 6 dataset.

Objective: Used various clustering techniques to group Brazilian online customers based on thier similarities
Used K-means and GMM clustering algorithms using the the Brazilian E-Commerce Public Dataset by Olist version 6 dataset to find cusomter groups with similar characteristics.




<p align="center">
<img width="460" height="300" src='https://user-images.githubusercontent.com/26442702/144537000-e09ee378-5cab-41a1-8d21-5e5051c5ea19.png')>
</p>
<p align="center">
Inertia Vs cluters
</p> 

<p align="center">
------------------------------------------------------------------------------------------------------------------------------------------
</p>
<p align="center">
<img width="460" height="300" src='https://user-images.githubusercontent.com/26442702/144537036-4d17288a-33f5-47fb-9202-a819865ee01b.png')>
</p>
<p align="center">
SilhouetteVisualizer
</p> 

<p align="center">
------------------------------------------------------------------------------------------------------------------------------------------
</p>
<p align="center">
<img width="460" height="500" src='https://user-images.githubusercontent.com/26442702/144537064-f6f6825e-c9db-473b-b90a-432da9eab5d3.png')>
</p>
<p align="center">
The Most Different Features Between Customer Groups
</p> 

<p align="center">
------------------------------------------------------------------------------------------------------------------------------------------
</p>
<p align="center">
<img width="550" height="600" src='https://user-images.githubusercontent.com/26442702/144537070-d0e9cef3-c179-4c19-b499-23e657e2d166.png')>
</p>
<p align="center">
Customers Location Across Brazil
</p> 


**In summary:**
- Two clustering methods, K-means and GMM have been implemented on the customer level data and the result has always indicated that there are two customer groups and no more
- The two methods agreed on the facts that the two groups are:
    - a happy group, that paid less per order and got lighter products and are more satisfied (gauged by their review score) while the unhappy group paid more money and received heavier and bigger products and are less satisfied.
- K-means results seemed to be more reliable due the way he difference in various features between clusters could be interpreted
- the summary of Kmeans is:
    - the first customer group (cluster 0) paid less (150 on average), got their smaller orders (2 Kg on average) faster (10 days on average), have seen more products photos (twice  much the other group) and gave good review scores (~4.8 on average)
    - the second customer group (cluster 1) paid more (175 on average), got their bigger orders (2.25 Kg on average) slower (17 days on average), have seen less products photos and gave bad review scores (~2 on average)
    
    
| Customer group | payment | order physical size | shipping | product photos | review score |
| --- | --- | --- | --- | --- | --- |
| 0 | low | small and light | fast | many | high score (happy customers) | 
| 1 | high | big and heavy | slow | not many | low score (unhappy customers) | 

- The main visible difference between the means and median analysis can be seen on the average order photos quantity `product_photos_qty`. The median analysis clearly show that the happy customers have seen almost twice photos as much on their orders than they unhappy customers. This is an interesting finding and can only confirm that they unhappy customers (the second group) may have been disappointed not only by their expensive orders to arrive late, but also but the fact that they do not match their expectations
- The customer location was found not have any significant implication on the cluster assignment
