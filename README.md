# Travell-Agency-Prediction



The data is from one of the world’s largest online travel agency (OTA) which powers search results for millions of travel shoppers every day
In this competitive market matching users to hotel inventory is very important since users easily jump from website to website.
As such, having the best ranking of hotels (“sort”) for specific users with the best integration of price competitiveness gives an OTA the best chance of winning the sale.

The dataset includes shopping and purchase data as well as information on price competitiveness.
The data are organized around a set of “search result impressions”, or the ordered list of hotels that the user sees after they search for a hotel on the agency's website.
In addition to impressions from the existing algorithm, the data contain impressions where the hotels were randomly sorted, to avoid the position bias of the existing algorithm.
The user response is provided as a click on a hotel or/and a purchase of a hotel room.

Appended to impressions are the following:

1) Hotel characteristics
2) Location attractiveness of hotels
3) User’s aggregate purchase history
4) Competitive OTA information




Column Name	Data Type	Description
search_id	Integer	The ID of the search
timestamp	Date/time	Date and time of the search
site_id	Integer	ID of the website point of sale (i.e..com, .co.uk, .co.jp, ..)
user_country_id	Integer	The ID of the country the customer is located
user_hist_stars	Float	The mean star rating of hotels the customer has previously purchased; null signifies there is no purchase history on the customer
user_hist_paid	Float	The mean price per night (in US$) of the hotels the customer has previously purchased; null signifies there is no purchase history on the customer
listing_country_id	Integer	The ID of the country the hotel is located in
listing_id	Integer	The ID of the hotel
listing_stars	Integer	The star rating of the hotel, from 1 to 5, in increments of 1.  A 0 indicates the property has no stars, the star rating is not known or cannot be publicized.
listing_review_score	Float	The mean customer review score for the hotel on a scale out of 5, rounded to 0.5 increments. A 0 means there have been no reviews, null that the information is not available.
is_brand	Integer	+1 if the hotel is part of a major hotel chain; 0 if it is an independent hotel
location_score1	Float	A (first) score outlining the desirability of a hotel’s location
location_score2	Float	A (second) score outlining the desirability of the hotel’s location
log_historical_price	Float	The logarithm of the mean price of the hotel over the last trading period. A 0 will occur if the hotel was not sold in that period.
listing_position	Integer	Hotel position on the search results page. This is only provided for the training data, but not the test data.
price_usd	Float	Displayed price of the hotel for the given search.  Note that different countries have different conventions regarding displaying taxes and fees and the value may be per night or for the whole stay
has_promotion	Integer	+1 if the hotel had a sale price promotion specifically displayed
booking_value	Float	Total value of the transaction.  This can differ from the price_usd due to taxes, fees, conventions on multiple day bookings and purchase of a room type other than the one shown in the search
destination_id	Integer	ID of the destination where the hotel search was performed
length_of_stay	Integer	Number of nights stay that was searched
booking_window	Integer	Number of days in the future the hotel stay started from the search date
num_adults	Integer	The number of adults specified in the hotel room
num_kids	Integer	The number of (extra occupancy) children specified in the hotel room
num_rooms	Integer	Number of hotel rooms specified in the search
stay_on_saturday	Boolean	+1 if the stay includes a Saturday night, starts from Thursday with a length of stay is less than or equal to 4 nights (i.e. weekend); otherwise 0
log_click_proportion	Float	The log of the probability a hotel will be clicked on in Internet searches (hence the values are negative)  A null signifies there are no data (i.e. hotel did not register in any searches)
distance_to_dest	Float	Physical distance between the hotel and the customer at the time of search. A null means the distance could not be calculated.
random_sort	Boolean	+1 when the displayed sort was random, 0 when the normal sort order was displayed
competitor1_rate	Integer	+1 if agency has a lower price than competitor 1 for the hotel; 0 if the same; -1 if the agency's price is higher than competitor 1; null signifies there is no competitive data
competitor1_has_availability	Integer	+1 if competitor 1 does not have availability in the hotel; 0 if both agency and competitor 1 have availability; null signifies there is no competitive data
competitor1_price_percent_diff	Float	The absolute percentage difference (if one exists) between the agency and competitor 1’s price (agency’s price the denominator); null signifies there is no competitive data
competitor2_rate	Integer	(same, for competitor 2 through 8)
competitor2_has_availability	Integer	
competitor2_price_percent_diff	Float	
competitor3_rate	Integer	
competitor3_has_availability	Integer	
competitor3_price_percent_diff	Float	
competitor4_rate	Integer	
competitor4_has_availability	Integer	
competitor4_price_percent_diff	Float	
competitor5_rate	Integer	
competitor5_has_availability	Integer	
competitor5_price_percent_diff	Float	
competitor6_rate	Integer	
competitor6_has_availability	Integer	
competitor6_price_percent_diff	Float	
competitor7_rate	Integer	
competitor7_has_availability	Integer	
competitor7_price_percent_diff	Float	
competitor8_rate	Integer	
competitor8_has_availability	Integer	
competitor8_price_percent_diff	Float	
clicked	Boolean	if the listing is clicked 1, else 0
booked	Boolean	if the listing is booked 1, else 0
