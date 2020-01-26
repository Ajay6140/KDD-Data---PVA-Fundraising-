# KDD-Data---PVA-Fundraising & Target Marketing 



(from http://kdd.ics.uci.edu/databases/kddcup98/epsilon_mirror/cup98doc.txt)

BACKGROUND ------------------------- 

The data set for this year's Cup has been generously provided by the Paralyzed Veterans of America (PVA). PVA is a not-for-profit organization that provides programs and services for US veterans with spinal cord injuries or disease. With an in-house database of over 13 million donors, PVA is also one of the largest direct mail fund raisers in the country. Participants in the '98 CUP will demonstrate the performance of their tool by analyzing the results of one of PVA's recent fund raising appeals. This mailing was sent to a total of 3.5 million PVA donors who were on the PVA database as of June 1997. Everyone included in this mailing had made at least one prior donation to PVA. The mailing included a gift (or "premium") of personalized name &amp; address labels plus an assortment of 10 note cards and envelopes. All of the donors who received this mailing were acquired by PVA through similar premium-oriented appeals such as this. One group that is of particular interest to PVA is "Lapsed" donors. These are individuals who made their last donation to PVA 13 to 24 months ago. They represent an important group to PVA, since the longer someone goes without donating, the less likely they will be to give again. Therefore, recapture of these former donors is a critical aspect of PVA's fund raising efforts. However, PVA has found that there is often an inverse correlation between likelihood to respond and the dollar amount of the gift, so a straight response model (a classification or discrimination task) will most likely net only very low dollar donors. High dollar donors will fall into the lower deciles, which would most likely be suppressed from future mailings. The lost revenue of these suppressed donors would then offset any gains due to the increased response rate of the low dollar donors. Therefore, to improve the cost-effectiveness of future direct marketing efforts, PVA wishes to develop a model that will help them maximize the net revenue (a regression or estimation task) generated from future renewal mailings to Lapsed donors. 

POPULATION ----------

The population for this analysis will be Lapsed PVA donors who received the June '97 renewal mailing (appeal code "97NK"). Therefore, the analysis data set contains a subset of the total universe who received the mailing. The analysis file includes all 191,779 Lapsed donors who received the mailing, with responders to the mailing marked with a flag in the TARGET_B field. The total dollar amount of each responder's gift is in the TARGET_D field. The overall response rate for this direct mail promotion is 5.1%. The package cost (including the mail cost) is $0.68 per piece mailed. 

ANALYSIS TIME FRAME AND REFERENCE DATE -------------------------------------- 

The 97NK mailing was sent out on June 1997. All information included in the file (excluding the giving history date fields) is reflective of behavior prior to 6/97. This date may be used as the reference date in generating the "number of months since" or "time since" or "elapsed time" variables. The participants could also find the reference date information in the filed ADATE_2. This filed contains the dates the 97NK promotion was mailed. 
+--------------------------------------------------------------------+ | 

DATA SOURCES and ORDER &amp; 

TYPE OF THE VARIABLES IN THE DATA SETS 

| +--------------------------------------------------------------------+

The dataset includes: o 24 months of detailed PVA promotion and giving history (covering the   period 12 to 36 months prior to the "97NK" mailing) o A summary of the promotions sent to the donors over the most recent   12 months prior to the "97NK" mailing (by definition, none of these   donors responded to any of these promotions) o Summary variables reflecting each donor's lifetime giving history (e.g., total # of donations prior to "97NK" mailing, total $ amount of the donations, etc.) o Overlay demographics, including a mix of household and area level   data o All other available data from the PVA database (e.g., date of first gift, state, origin source, etc.) The fields are described in greater detail in the data dictionary file &lt;filename: cup98DIC.txt>


# TARGET MARKETING 

# Background

A national veteran’s organization wishes to develop a data mining model to improve the cost-
effectiveness of their direct marketing campaign. The organization, with its in-house database of over 13 million donors, is one of the largest direct mail fundraisers in the United States. According to their recent mailing records, the overall response rate is 5.1%. Out of those who responded (donated), the average donation is $13.00. Each mailing, which includes a gift of personalized address labels and assortments of cards and envelopes, costs $0.68 to produce and send. Using these facts, we take a sample of this dataset to develop a classification model that can effectively capture donors so that the expected net profit is maximized. Weighted sampling is used, under-representing the non-responders so that the sample has a more balanced numbers of donors and non-donors.

# Data

The modeling dataset is in the file pvaDataForModeling_Fall2018.csv. The data has been sampled (from the original PVA training dataset) to carry a higher proportion of donors (TARGET−B = 1) than in the original data. The amount of donation (TARGET−D) is also included but is not used in this assignment. The file contains all 480 attributes.
