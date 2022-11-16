## AMAZON SENTIMENT ANALYSIS

1. The project begins in the scraped_reviews folder for webscraping reviews for;
    - &nbsp;[mouse](https://www.amazon.com/%E3%80%90Upgrade%E3%80%91-Wireless-Rechargeable-Portable-Adjustable/product-reviews/B088NDL2G1/ref=cm_cr_getr_d_paging_btm_prev_4?ie=UTF8&reviewerType=all_reviews&sortBy=recent&pageNumber=1)
    - &nbsp;[keyboard](https://www.amazon.com/Klim-KLIM-Chroma-Wireless-USA/product-reviews/B07FLKYRFB/ref=cm_cr_arp_d_viewopt_srt?ie=UTF8&reviewerType=all_reviews&sortBy=recent&pageNumber=1)
    - &nbsp;[speaker](https://www.amazon.com/JBL-Portable-Waterproof-Wireless-Bluetooth/product-reviews/B07HKN3K31/ref=cm_cr_arp_d_viewopt_srt?ie=UTF8&reviewerType=all_reviews&sortBy=recent&pageNumber=1)
    - &nbsp;[headset](https://www.amazon.com/BENGOO-G9000-Controller-Cancelling-Headphones/product-reviews/B01H6GUCCQ/ref=cm_cr_arp_d_viewopt_srt?ie=UTF8&reviewerType=all_reviews&sortBy=recent&pageNumber=1)

2. The scraped data is saved in one database named amazon_sentiment with respective tables namely; led_wireless_mouse, keyboard, speaker, headset. The data is then accessed and exported to the data_analysis folder for data analysis.

3. Within the data analysis folder, pre-processing, EDA and Clustering analysis were carried out for modeling purposes within the model folder. 
    - Two approaches will be taken into account using a cleaned dataset without spelling correctiion and one with spelling correction and see which result performs better (cleaned_reviews & correct_spelling_reviews). 
    - Moreover, the WordCloud images can be seen in the img folder.

4. The model folder has two approches ml_algo and deep_learning for results comparison (yet to be done). 