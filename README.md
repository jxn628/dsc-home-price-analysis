# Home Price Analysis for King County WA

# Summary
I was tasked with analyzing home prices in King County to determine where the market for home renovations exists. Spefically, I was to determine which renovation types have the biggest increase in home value so that those services can be the focus of their marketing campaign.

I used the data provided and after cleaning and pre-processing, was able to develop a model which showed the effect that various features had on the price of homes.

My recommendation is that Trailblazer Renovations Inc. focus on features that add to the size of existing homes (ie Additions). These additions should be additional shared areas such as bathrooms,  as extra bedrooms begin to have a negative correlation with home value. I also recommend that the additions be on existing floors of the house, as additional floors also begin to have a negative correlation.

I also recommend that these additions be done with the highest quality materials and to the highest standard as the Grade of the home is also a strong contributor to home value. The more unique and custom the features of the addtion are, the more that it will add value to the home.

As for marketing, my model determined that the location of houses played a major role in their value. Therefore, Trailblazer Inc. should focus on the zip codes with the highest coefficients from the final model. I provided a ranked list for them to use for this purpose. 

# The Business Problem
Trailblazer Renovations is a home contractor that specializes in home additions and renovations. They are based in Northern California, but have been getting requests from homeowners in Washington State. They are interested in expanding their business, but want to gauge the situation before diving in.

They have already decided to focus their efforts on King County Washington as it contains a large population of people (including metropolitan Seattle) and could be a good opportunity for growth for them.

I have been tasked with analyzing home prices in King County to determine where the market for home renovations lies so that Trailblazer can meet that need. Part of this analysis is to determine which renovation types have the biggest increase in home value so that those services can be the focus of their marketing campaign.

While they plan on marketing to all of King County, they want to know if there are any particular areas that they should focus a greater portion of their energy in marketing to.

# The Data
I have the king county dataset which gives information on home values in King County. Here is what is contained in the raw data:

- id - unique identified for a house
- date - house was sold
- price - is prediction target
- bedrooms - of Bedrooms/House
- bathrooms - of bathrooms/bedrooms
- sqft_livings - footage of the home
- sqft_lots - footage of the lot
- floors - floors (levels) in house
- waterfront - House which has a view to a waterfront
- view - Has been viewed
- condition - How good the condition is ( Overall )
- grade - overall grade given to the housing unit, based on King County grading system
- sqft_above - square footage of house apart from basement
- sqft_basement - square footage of the basement
- yr_built - Built Year
- yr_renovated - Year when house was renovated
- zipcode - zip
- lat - Latitude coordinate
- long - Longitude coordinate
- sqft_living15 - The square footage of interior housing living space for the nearest 15 neighbors
- sqft_lot15 - The square footage of the land lots of the nearest 15 neighbors

# Questions I Wanted to Answer
1. What features have the biggest effect on home price?
2. Are these features able to be changed/renovated, or are they fixed?
3. What are the best features that Trailblazer should market to potential clients?
4. Who should Trailblazer target their marketing campaign toward?
5. Are there any features that I do not recommend pursuing? 

# The Answers I found
### Features that have the biggest effect on home price
1. Size of House (excluding Basement).
2. Grade
3. Location (Zip Code) 
4. Size of Basement
5. Waterfront Location
6. Size of Lot
7. Number of Bathrooms

### Features that CAN be changed (even if difficult):
1. Size of House
2. Grade
3. Basement Size -- I assume that this would be difficult, but not impossible.
4. Additional Bathrooms

### Features that I don't recommend pursuing:
1. Extra Bedrooms
2. Extra Floors

These features have a negative coefficient in regards to home price. If the client **needs** these features, then that is fine. But the scope of my analysis was to find the features that maximized home value and these two features do not meet that metric.

<u> Who should Trailblazer target their marketing campaign toward? </u>
- There is a very signifcant correlation between location and home price, so marketing should be targetting Customers in Zip Codes that had high coefficients in my model.



# Recommendations:

### Recommendation 1:

![Home Price by Home Size](https://github.com/jxn628/dsc-phase-2-project/blob/main/images/home_price_by_home_size.png)

Trailblazer Renovations should focus on home additions. <b>Increasing the square footage of the home has the greatest effect on the value of the house.</b> This is advice that can be given to any homeowner whereever they live in King County. 
- The increased square footage should be used for common areas as additional bedrooms have a negative corellation with price. 
- Extra floors should also be avoided, as floors have a negative corellation with price.
- The exception to this is in the basement. Theoretically, if you are able to increase the space in your basement (perhaps converting mechanical closets/storage into common space), there is value to be added there.
    - I know that it is possible to even add a basement to a house that didn't initially have one, but I also know that it's signficantly more expensive to do that.
    
### Recommendation 2:
 Trailblazer Renovations Inc. should use targeted marketing to homeowners in certain zip codes within King County. **There is a high coefficient on many zip codes, especially in the Seattle municipal area.**

Assuming that the cost for labor and materials is the same no matter what zip code the house is located in, the same work with the same materials brings greater value in certain zip codes.

Use the following list as a ranking of where to prioritize marketing efforts.
 
### Recommendation 3:

![Home Price by Grade](https://github.com/jxn628/dsc-phase-2-project/blob/main/images/home_price_by_grade.png)

 The second most signicant corellation for Home Price is Building Grade. I recommend that all renovations and additions done by TrailBlazer be done to the highest level of quality in terms of both materials and workmanship. If the renovations can cause the house to increase in grade, it will improbe the value of the house.

Most houses fall in the 7-8 grade. (71% of the records in the dataset). This is considered "Average" to "Just Above Average". Level 9 cites "better architectural design with extra interior and exterior design and quality."

The more unique and custom the features of the addtion are, the more that it will add value to the home.
