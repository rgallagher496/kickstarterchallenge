Analysis of Theater Kickstarter Campaigns
Prepared by Robert Gallagher


Overview

The purpose of this project is to first look at how start month of a Kickstarter campaign impacted the success rate for theater projects.
Second is to look at how goal size impacted the play subcategory of theater campaign success rates.  

Analysis and Challenges

Contained below is a summary of results from the analysis done in [kickstarterchallenge](Kickstarter_Challenge.xlsx)

	Outcomes based on launch date

	The following image is a line graph of counts of theater campaigns grouped by if the campaign was successful, failed, or canceled organized by 
	starting month pulled from data across multiple years.  To see the supporting pivot table look in the "TheaterOutcomesBy Launch Date" tab of the
	excel file linked above.

	![kickstarterchallenge](/Theater_Outcomes_vs_Launch.png)


	Outcomes based on goal size

	The following image is a line graph of the percent of successful, failed, and canceled campaigns of the theater subcategory of plays grouped by size of
	the campaign goal.  To see the supporting pivot table look in the "Outcomes Based on Goals" tab of the excel file linked above.
	
	![kickstaterchallenge](/Outcomes_vs_Goals.png)

	Challenges

	To count results by size category I first wrote an extremely long countifs function.  This was error prone so to simplify this function I created a new
	column in the "Kickstarter" tab of the attached excel file above called Goal Category.  I then wrote the following formula
	 =IF(D2<1000,"Less than 1000",IF(D2>=50000,"Greater than 50000",IF(D2<5000,"1000 to 4999",TRUNC(D2/5000)*5000&" to "&(TRUNC(D2/5000)+1)*5000-1))).
	This formula generates the categories needed in the "Outcomes Based on Goals" tab of the spreadsheet.  Then I was able to significantly shorten the countifs formula.
	Keep in mind this formula would need to be adjusted if categories are changed in the future. 

Conclusions

	Conclusions about outcomes based on launch date

	The time period with the most successful campaign launches were ones launched in May.  And given that the distance between the failed and successful line is also
	greatest in May this isn't just because there are more campaigns in May.  June also appears to have a higher success rate than the rest of the year.
	While July also has more successful campaigns than average the distance between failed and successful lines is much closer to the rest of the year.  I think it
	would make sense to also look at a percentage of successful campaigns per each month.  If you look at both number of campaigns started per month and the success rate
	we could make a better decision about what time frame would be best to start a new fund raising effort in.

	Conclusions about outcomes based on

	For the most part this says the smaller campaigns are more successful than the larger campaigns.  The exception appears to be for the 35000 to 39999 and 45000 to 49999 categories.
	But when you look at the total number of campaigns in these two categories you see that our sample size is small.  I don't think we have enough data points in these
	categories to really draw any conclusions about these two categories.  Overall, it looks like campaigns of less than $5000 dollars are the most successful.

	Other considerations

	I think it would be interesting to add our size categories to our goal start date analysis and see if there is any correlation between start time and campaign size.  I
	also think looking at the overall success rate by total length of the campaign would be useful.  Based on the data it looks like Kickstarter is mostly used for smaller
	donation goals so another if a larger budget is needed then another funding source should probably be used.
