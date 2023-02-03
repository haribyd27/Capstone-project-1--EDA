NOTBOOKLINK: https://colab.research.google.com/drive/1Io06DQKydlLAcxiOYKSRYBI_nSYvh965#scrollTo=F6v_1wHtG2nS

# Capstone-project-1--EDA
INTRODUCTION: In this I have attempted to analyse the dataset of hotel bookings. The dataset consists of 119390 records across 32 features and has been given with information regarding bookings of two hotels from July 2015 to August 2017. These two hotels are City Hotel and Resort Hotel. It also explores vast information of these two hotel types such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things, etc. The purpose of this project is to analyse Hotel Bookings data, investigate cancellations, and their underlying patterns and suggest measures that can be implemented to reduce cancellations and secure revenue. The main objective is to explore the given dataset and discover the factors which govern the bookings. The dataset will be analysed and from the conclusions drawn from it will be used to recognize the missteps taken by the manager. With this information, hotels will be equipped to improve their performance.

PROBLEM STATEMENT: Have you ever wondered when the best time of year to book a hotel room is? Or the optimal length of stay in order to get the best daily rate? What if you wanted to predict whether or not a hotel was likely to receive a disproportionately high number of special requests? This hotel booking dataset can help you explore those questions! This data set contains booking information for a city hotel and a resort hotel, and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things. All personally identifying information has been removed from the data. Explore and analyse the data to discover important factors that govern the bookings.
Main Libraries to be used:
    Pandas for data manipulation, aggregation
    Matplotlib and Seaborn for visualisation and behaviour with respect to the target variable. Use at least 5 different visualisations.
    NumPy for computationally efficient operations
    
OBJECTIVE: We are provided with a hotel bookings dataset. Out main objective is performing EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other. I have tried to do a simple analysis of hotel booking data using matplotlib and seaborn libraries.

DATA VISUALIZATION: The Data analysis is performed to answer the following questions.
1.	What is the portion of each hotel type (i.e. City hotel. Resort hotel)
2.	What is the percentage of cancellations and non-cancellations of each hotel types.
3.	What is the total arrival trend of adults, children and babies from 2015-2017-time period.
4.	What is number of cancellations and non-cancellations for each deposit type (i.e No deposit. Non-refundable, and Refundable) for all hotel types.
5.	What is count of monthly arrivals, weekly arrivals and daily arrivals for all months for both the hotel types.
6.	What is the count of group of people staying on weekdays nights and weekends nights.
7.	What is the count of reserved and assigned room types of both the hotels. And also the count of booking changes for all room types of both the hotels.
8.	What is count of customer’s types, market types, and distributions types. What is the count of cancellations and non-cancellations of all the market types (i.e. Direct, corporate, online TA, offline TA/TO, complementary, groups, and Aviation) for both the hotels.
9.	What is correlation of variables among each other.
10.	What is the overall dirtibution of lead time. And also the individual distribution for both hotels.

Approach:
1. Understanding the business task.
2. Import relevant libraries and define useful functions.
3. Reading data from files given.
4. Data inspection.
5. Data cleaning.
6. Exploratory data analysis, to find which factors affect the bookings and how they affect it.
8.Conclusions drawn from analysis.

TOOLS USED: Main Libraries to be used:
    Pandas for data manipulation, aggregation
    Matplotlib and Seaborn for visualisation and behaviour with respect to the target variable. 
    NumPy for computationally efficient operations

VARIBLE DESCRIPTION:

- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.

DATASET UNDERSTANDING:There are large number of NaN values in company and agent. They have very much less impact on the analysis and hence those 2 columns are removed. The reason for not removing rows with NaN value is because we have to remove 112593 rows out of 119390 rows which means we are removing around 90% data. So removing columns will be a better idea since those 2 attributes (agents and companies) are unimportant. 488 rows with NAN values out of 119390 is negligible hence these can be removed.For each hotel type, the total nuber of bookings, the percentage of cancellations and non cancellations are found for the analysis.


CONCLUSIONS:
The following conclusions were drawn from analysis:
1.	City hotel seems to be more preferred among travellers than resort hotel.
2.	Both hotels have significantly higher booking cancellation rates. The cancellations were more for the city hotel type than resort hotel.
3.	The arrival rate of adults, children and babies was higher in the year 2016.
4.	The majority of bookings are done for no deposit for both hotels. (rather than partial or full). If we just look at non-cancelled bookings data, we can conclude that if people were to cancel more, the majority of the cancellations would be the ones with no deposit collected. The bookings made through non-refundable deposit type are most likely to be cancelled.
5.	July- August are the most busier and profitable months for both the hotels.
6.	Couples are the most common guests for hotels, hence hotels can plan services according to couples needs to increase the revenue.
7.	Room Type A is the most preferred room type among travellers. Most of the travellers got their assigned room type only. The booking changes are less, hence the changes in booking is not the reason for the cancellations.
8.	Majority of the distribution channels and market segments involve travel agencies (online or offline). We can target our marketing area to be on these travel agencies website and work with them since majority of the visitors tend to reach out to them.
9.	Most variables are least correlated among themselves
10.	Lead time does not affect cancellation of bookings.


















  
	


