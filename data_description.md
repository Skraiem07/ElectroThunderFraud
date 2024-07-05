## __Variable definitions__

### Client:

- Client_id: Unique id for client
- District: District where the client is
- Client_catg: Category client belongs to
- Region: Area where the client is
- Creation_date: Date client joined
- Target: fraud:1 , not fraud: 0

### Invoice data:

- Client_id: Unique id for the client
- Invoice_date: Date of the invoice
- Tarif_type: Type of tax
- Counter_number:
- Counter_statue: takes up to 5 values such as working fine, not working, on hold statue, ect
- Counter_code:
- Reading_remarque: notes that the STEG agent takes during his visit to the client (e.g: If the counter shows something wrong, the agent gives a bad score)
- Counter_coefficient: An additional coefficient to be added when standard consumption is exceeded
- Consommation_level_1: Consumption_level_1
- Consommation_level_2: Consumption_level_2
- Consommation_level_3: Consumption_level_3
- Consommation_level_4: Consumption_level_4
- Old_index: Old index
- New_index: New index
- Months_number: Month number  It might represent a specific billing cycle. For instance, a billing period that occurs every four months.
- Counter_type: Type of counter


## goal:
Using the client’s billing history, the aim of the challenge is to detect and recognize clients involved in fraudulent activities.

## target variable
target :  
- fraud:1 
- not fraud: 0

## evaluation metric 
AUC

--------------

##Reduction in Financial Losses**:

#Goal*: Decrease annual financial losses due to fraud by 80%.
#Impact**: Potential savings of up to 160 million Tunisian Dinars annually.
##Enhanced Revenue**:

#Goal**: Increase overall revenue by 10%.
#Impact**: Ensure accurate billing and improved financial performance.
Improved Fraud Detection Accuracy:

Goal: Achieve a fraud detection accuracy rate of 95%.
Impact: Minimize false positives and negatives, leading to more effective fraud prevention.
Operational Efficiency:

Goal: Automate 90% of the fraud detection process.
Impact: Reduce manual workload, enhance productivity, and allocate resources to strategic tasks.
Customer Trust and Satisfaction:

Goal: Increase customer satisfaction ratings by 15%.
Impact: Fair billing practices and reduced erroneous accusations will build trust and improve customer relationships.



---------------------------------------------------
- we already changed the date types to dtypes "creation_date" and "invoice date"
- the "months_number" values goes fr0m 0 to 13558 which is not correct : 
the month number has no logic for it 
- how to  interstand  if a client who has two counters is frauding , is the fraude based on the counterid or client id 

----------------
Counter statue takes up to 5 values such as working fine, not working, on hold statue..., ect. Reading remarque is notes that the STEG agent takes during his visit to the client (e.g: If the counter shows something wrong, the agent gives a bad score). And the counter coefficient is an additionnal coefficient to be added when standard consumpution is exceeded
------------------
consommation_level_1 to 4: Consumption levels, likely representing different tiers or categories of consumption.