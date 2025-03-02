
# Objective
The overall objective for this project is to write a code that can scrape the NICE website committee documents to extract the software used for the economic model development for each guidance piece. This would then be used to determine the number and % of non-Excel models in submissions, and determine if there are trends by date or disease/submission type.

# Steps
1. All NICE published evidence is in https://www.nice.org.uk/guidance/published. The table needs to be expanded to 'show all'. All information from this table needs to be scraped and stored.
2. For each of the 'Reference numbers', a new address needs to be made following the pattern https://www.nice.org.uk/guidance/REFNUMBER/evidence (e.g. https://www.nice.org.uk/guidance/ta1043/evidence for the first one). On this page there will be several links to pdfs. All availabile pdf links all need to be identified.
   - If it is possible, it would also be good to know the size of each of the pdfs that are being linked to, and the date
3. A selection criteria can then be made to pick the correct link. Firstly it would select for 'committee papers' in the title of the pdf/address. Then it would select by most recent (or filter further for 'final', and ensure that the selected pdf is of the expected size (>2MB) to pick the pdf that is most likely ot have the information we need
4. The company evidence submission template can then be used to our advantage. The code could then open the pdf link and find 'B.3.2 Economic analysis' - if this does not exist then it would return a 'not found' or have the option to select the next likely pdf. The text between the headings 'B.3.2 Economic analysis' and 'B.3.2.1. Patient population' can be extracted and then processed to search for terms such as 'Microsoft Excel',  ' R ' or 'TreeAge. The number of hits can be reported, and from there there can be a manual check of flagged submissions which did not contain 'Microsoft Excel' to see what refinement may be needed to the code

# Proof of concept
## I would appreciate help with any of these items, either by giving me an example or telling me a useful package/function
1. Extract the full table from https://www.nice.org.uk/guidance/published
2. Extract the links to pdfs available on https://www.nice.org.uk/guidance/ta1043/evidence page
3. (optional) Extract the date and size of the pdfs on https://www.nice.org.uk/guidance/ta1043/evidence page
4. Open https://www.nice.org.uk/guidance/ta1044/evidence/draft-guidance-consultation-committee-papers-pdf-15249475981 and extract the text between 'B.3.2 Economic analysis' and 'B.3.2.1. Patient population'

## Thanks team

