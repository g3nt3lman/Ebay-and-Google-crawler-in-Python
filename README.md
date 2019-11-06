# Crawler-Ebay

This project was done, due to improving freelance work. Some employer on Upwork portal wanted to search for EANs of particular products. 
The provided me with products names and initially wanted to look for products barcodes manually. I have created crawler which look for 
those products onb ebay, get EANS from there and than search those just finded barcodes in google.
Contractor approved a list of sites from where the coming EANs were robust. Those sites adresses are listed in pattern file.
If google search results printed out the site that is in that list, than finally ean is approved and mentioned site is added to uotput
file.

Note that not always there is an EAN in wwww, sometimes product is so old that noone sells it anymore. Therefore crawler cant find 
EANS of this products. Sometimes ebay sites of products does not contain EANs and in this particular cases those missing EANs should
be search with other method.

In this project to find sites and product that fit the most given names, I used Levensthein distance to compare found products with the 
given ones. Aquired score from Levensthein function was compared to other witihin a search results, and that with best score was choosen
both on ebay and google search step.
