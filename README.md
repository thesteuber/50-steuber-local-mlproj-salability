# Security Salability of New Homeowner (SSNH) with Machine Learning

## Project Description
The SSNH project aims to determine a "Salability" score of a lead for Safe Haven Security (The Company) based on an assortment of data points, and with this score, the company will be able to better prioritize touching leads by market by score.

The SSNH Score will range from 0.00 (hypothetically not sellable) to 1.00 (100% likelihood of making the sale).

## Primary Use Case (PUC)
As the head of the Leads team, I want to take a csv of leads and pump them through the SSNH, providing the SSNH score to each lead. I will then group by market and prioritize leads within the markect by the SSNH score.

## Raw Data Sources
The company recently make large breakthroughs getting their data from their CRMs, HR System, Vendor EDI Sources, and Affiliate partners into a enterprise data core made up by a data lake and a data warehouse.

The data to be used for linnear regression will mainly come from the company's core CRM that contains the contractual data (i.e. whether or not the lead made it to install) and an auxiliary CRM that houses additional data like the value of the property.

Then of course the data to feed the ssnh will come from feature engineering the daily leads intake from Zillow, RedFin, Realtor, and the MLS.

## Description of Metrics
The main metrics for the SSHN project will aim to gauge the success of the project by determing the accuracy of the SSNH score. To achieve this, the metrics needed are a mixture of the following:

<!-- I am unclear on how SSNH will be calculated. Are you expecting the model to calucate this value? If so, are there any metrics needed for the formula? Or is this an existing field in your dataset? -->

<ul>
  <li>Total Unsold Leads</li>
  <li>Total Leads Sold</li>
  <li>Average SSNH Score</li>
  <li>Total Unsold Leads with an SSNH Score = 1.00 </li>
  <li>Total Leads Sold with an SSNH Score = 1.00</li>
  <li>Total Unsold Leads with an SSNH Score >= 0.75 </li>
  <li>Total Leads Sold with an SSNH Score >= 0.75</li>
  <li>Total Unsold Leads with an SSNH Score >= 0.50 </li>
  <li>Total Leads Sold with an SSNH Score >= 0.50</li>
  <li>Total Unsold Leads with an SSNH Score >= 0.25 </li>
  <li>Total Leads Sold with an SSNH Score >= 0.25</li>
  <li>Total Unsold Leads with an SSNH Score = 0.00 </li>
  <li>Total Leads Sold with an SSNH Score = 0.00</li>
</ul>

Trial runs could attempt to prioritize the daily lead pickings by SSNH score descending. The closing rates on the sales could then be compared to the closing rates whenever the SSNH Score is not considered. 

Estimating that every sold lead generates roughly $2,000 for the company, the value of the SSNH would be shown clearly in dollars by taking the hopefully higher closing rate on days during which the SSNH score is considered and determing the average amount of additional sales the company closes by prioritizing the leads with a higher likelihood of selling. 

