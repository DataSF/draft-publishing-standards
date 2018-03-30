# Appendices

## Appendix A. Rationale for Recommended Standard

In the absence of a citywide standard, we relied on the following to inform a citywide recommended standard:

* The results of the Department of Public Health’s research that resulted in department wide race and ethnicity guidelines released in 2011
* The large scale, random assignment testing conducted by the US Census in 2010 and 2015 to compare alternative question formats \([see overview of research](https://www.census.gov/about/our-research/race-ethnicity.html)\)

### Combined or separate questions

A standard for race and ethnicity must address a key design choice: should race and ethnicity be asked as separate \(one question for ethnicity, i.e. Hispanic or Latino, and another for race\) or combined questions?

Repeated testing by the Census showed that a combined question format yielded data of the highest quality. This is consistent with DPH’s recommendation to use a combined question format.

Below is an excerpt from the US Census 2015 National Content Test \(NCT\):

> “The 2015 NCT research demonstrates that a question format that combines race and ethnicity into one question results in more accurate reporting and dramatically lower item nonresponse compared to the two separate questions on Hispanic origin and on race. In addition, with a new combined question design approach which employed multiple detailed checkboxes to help collect the reporting of detailed groups, the NCT research successfully demonstrated how an innovative approach could collect data for myriad groups across our nation’s diverse population. By combining the race and Hispanic origin questions into 84 one question on race/ethnicity, the research has shown that Hispanics can better find themselves among the race and ethnicity categories.” \(Census, 2015\)

In addition, responses to combined question format can be mapped to any external reporting requirements that are structured using separate questions.

As a result, the recommended standard for San Francisco combines race and ethnicity into a single question using terminology and language tested in the 2015 National Content Test. To address data mapping concerns, the standard also provides guidance and tools for external reporting and data mapping.

### Inclusion of a new category, MENA

The Census tests also explored including a category for Middle Eastern North African \(MENA\), a group that historically is included in the “white” category. The results concluded that the Census should include MENA:

> “The NCT research findings show that the use of a distinct MENA category elicits higher quality data; and people who identify as MENA use the MENA category when it is available, whereas they have trouble identifying as only MENA when no category is available.” \(Census, 2015\)

As a result, the recommended standard includes a category for MENA using terminology and language tested in the 2015 National Content Test. The standard also provides guidance and tools for external reporting and data mapping.

### Census decision to not make changes for 2020

Despite the results of testing related to the topics above, the Census is not making changes for the 2020 Census. This decision is controversial \([this article provides some background on the decision](https://www.npr.org/2018/01/26/580865378/census-request-suggests-no-race-ethnicity-data-changes-in-2020-experts-say)\). Despite this decision, we are moving forward with the recommended standard because:

* San Francisco data collection does not operate under the same climate as federal decision making
* The combined question format and inclusion of MENA has generated better response rates and better quality data in repeated testing
* Our one example of a local standard \(DPH's race/ethnicity\) uses combined as a result of their extensive process of analysis and community engagement
* The existing federal standard already provides for a method for collecting using both combined and separate formats
* External comparisons can be mapped and most reporting already requires mapping the census data to obtain accurate comparisons for Hispanic, Alone

### Multiple Selection must be allowed

A study from the Census ranked California as 2nd highest state for those selecting two or more races in the 2010 census. The census has historically captured race/ethnicity information via options that allowed the respondent to select more than one. Likewise the 1997 OMB Race & Ethnicity standard calls for the use of multiple selection. 

Any modern data system is capable of capturing multiple selections. For older systems limited to single select, it is possible to capture the equivalent information via two or more instances of a single select question. 

### Detailed Race/Ethnicity subgroups left to discretion of departments

This standard should not be interpreted as discouraging or limiting the collection of detailed race/ethnicity information. For certain purposes it is desirable to collect more detailed race/ethnicity sub-group information. Different departments and offices will have different sub-groups that are relevant to their work or may be needed for internal or external reporting \(ex. detailed asian ethnicities\). 

Similar to the Department of Public Health’s 2011 race and ethnicity guidelines, collection of detailed race/ethnicity information is permitted as long as the values can be rolled up into one the the 7 values in this standard.

## Appendix B. Mapping and Transformations Rule Background

The San Francisco Recommended Standard provides rules for mapping and transforming the standard to external or historical data collection methodologies. Below we provide background on the Largest Group other than White rule.

Most state and federal reporting systems request data ‘as is’ via electronic transfer and will handle aggregation \(and the associated decisions\) themselves. The reasoning behind this mirrors the reasoning for this standard; it provides the reporting agency with the most detailed data available as well as ensuring a consistent aggregation method across the various state and local jurisdictions.

**Challenge: how to map multi-select to a single value.** In cases where the department has to perform the aggregation several challenges appear when aggregating from multi-select racial/ethnicity categories to often a single race/ethnicity value. For example if a respondent selected White and Black, or Asian and Hispanic as their races, which option do you report?

**Federal working group identified multiple methods.** Considerable thought and testing went into such questions during the shift to allowing multiple race selections in the 1997 OMB Race Ethnicity Standard. In 2000 the OMB Tabulation Working Group released guidance on best practices for transforming multi-race data to single race reporting standards. They presented options that ranged in complexity with each containing pros and cons.

**Deterministic whole assignment methods should be used. **The federal working group identified two main approaches:

* Deterministic Whole Assignment methods which are fixed rules for assigning race/ethnicity values
* Probabilistic and Fractional Assignment methods which rely on statistical estimation

The probabilistic and fractional assignment methods are much more complex to implement and to explain, particularly on a local scale. Given a review of the options and in consultation with experts, we recommend using Deterministic Whole Assignment methods. We identified three options suited to the purposes of the this standard. The three Deterministic Whole Assignment methodologies for when there are 2 or more races selected are:

* Smallest Group. The smallest of the 2 races in the general population is the one reported.
* Largest Group other than White. The largest of the 2 races in the general population is the one reported unless that race is white.
* Largest Group. The largest of the 2 races in the general population is the one reported.

The table below provides examples to illustrate the methods using the makeup of the population in San Francisco. Given the unique demographics of San Francisco, the preferred option is ‘Largest Group other than White’ to ensure adequate representation by non-white groups.

| **Race and ethnicity 1** | **Race and ethnicity 2** | **Smallest group** | **Largest group other than White** | **Largest group** |
| :--- | :--- | :--- | :--- | :--- |
| White | American Indian or Alaska Native | American Indian or Alaska Native | American Indian or Alaska Native | White |
| White | Asian | Asian | Asian | White |
| White | Black or African American | Black or African American | Black or African American | White |
| White | Hispanic, Latino, or Spanish | Hispanic, Latino, or Spanish | Hispanic, Latino, or Spanish | White |
| White | Middle Eastern or Northern African | Middle Eastern or Northern African | Middle Eastern or Northern African | White |
| White | Native Hawaiian or Other Pacific Islander | Native Hawaiian or Other Pacific Islander | Native Hawaiian or Other Pacific Islander | White |
| Asian | American Indian or Alaska Native | American Indian or Alaska Native | Asian | Asian |
| Asian | Black or African American | Black or African American | Asian | Asian |
| Asian | Hispanic, Latino, or Spanish | Hispanic, Latino, or Spanish | Asian | Asian |
| Asian | Middle Eastern or Northern African | Middle Eastern or Northern African | Asian | Asian |
| Asian | Native Hawaiian or Other Pacific Islander | Native Hawaiian or Other Pacific Islander | Asian | Asian |
| Asian | White | Asian | Asian | White |





