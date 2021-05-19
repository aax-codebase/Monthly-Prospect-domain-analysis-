## Similarweb process: (to be run from 8th of month)   

- Go to the Gsheet “aax SimilarWeb Dashboard A La Carte” (https://docs.google.com/spreadsheets/d/1SF2fzB2-BgexrFqx9k4Ud-9HsgN1T_4MPLL0JAJA1Zg/edit#gid=0) and delete the domains in column H.  
- Download Salesforce report “Pipeline linked websites” (https://aax.lightning.force.com/lightning/r/Report/00O5a000005zIuXEAU/edit?queryScope=userFolders) and place these domains in column H.  
- Ensure the start month in column C is month M-1 and the Sales solution is “Lead Enrichment - Full”  
- Press the large “Refresh data” button.  
- Copy this data to the file similarweb_full_save.xlsx labelling the month in question in column B.  
- Once the data is collected copy it to the Similarweb Dashboard creating a new tab for the month in question.  
- Request the top 200 domains from the MNET team and run the same process as with the above domains. This data should be added to the tab “Top 200 domains” with the relevant data from Similarweb being the establishment of the Category for RPM and Ad block forecasting.  
  
## Blockthrough process:  

- Download Salesforce report “Pipeline linked websites” (https://aax.lightning.force.com/lightning/r/Report/00O5a000005zIuXEAU/edit?queryScope=userFolders)
- Save the report as the month/year to which you will be running data against.  
 e.g. In March 2021 the data gathered for similarweb is from February so 2021-02.  
- Run the script cookie_acceptor.py which will create an input list for the languages scrape.  
- Run the script get_languages_from_websites.py. Make sure to accept all cookie messages from each of the relevant pages.  
- Run the script Blockthrough_scrape_input.py which will create a list ready to be iterated over to check for Blockthrough code.  
- Run the script Blockthrough_initial_scrape.py which will iterate over all of the domains searching for Blockthrough code.  
- Add the output columns (Blockthrough detected?, Ad block warning?) from the csv “MMM-Y” to columns AF and AG in the Similarweb Dashboard.  
- Release an email to the team highlighting that the monthly data is available.  
