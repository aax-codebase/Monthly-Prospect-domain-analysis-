# Monthly-website-data-update
A combination of scripts to keep the website objects updated in Salesforce.

## Outline:  
  
The repository contains a series of scripts to be used to keep the linked website objects in Salesforce updated.

## Process:  
  
### Webscraping process:  

1)  
As close to the first of the month as possible download the report "TO_BE_CREATED" with the list of linked website objects created in the last month.  
These websites need to be scanned for the language of the website so that they can be effectively categorised. Save the file as "websites_input_1.csv".
  
2)  
Run the script get_languages_from_websites.py which will add a column to the file with the given language.

3)  
Run the script "CREATE_LIGHT_SCRIPT.py" iterating over the new websites and allowing cookies.  

4)  
Run the script "blockthrough_initial_scrape.py" on the full Salesforce website download list. This iterates through the full website list establishing    
firstly the relevant data with the adblocker enabled and secondly with it disabled.  

### Similarweb process:  







### Combination process:  


1)  
Run the combination script "TO_BE_CREATED.py" combining the data from the Ad-block scrape, the non-Ad-block scrape and the Similarweb API calls into one file  
that is ready to be uploaded to salesforce "TO_BE_CREATED.csv"
