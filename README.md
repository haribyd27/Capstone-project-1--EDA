# Capstone-project-1--EDA
INTRODUCTION: In this I have attempted to analyse the dataset of hotel bookings. The dataset consists of 119390 records across 32 features and has been given with information regarding bookings of two hotels from July 2015 to August 2017. These two hotels are City Hotel and Resort Hotel. It also explores vast information of these two hotel types such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things, etc. The purpose of this project is to analyse Hotel Bookings data, investigate cancellations, and their underlying patterns and suggest measures that can be implemented to reduce cancellations and secure revenue. The main objective is to explore the given dataset and discover the factors which govern the bookings. The dataset will be analysed and from the conclusions drawn from it will be used to recognize the missteps taken by the manager. With this information, hotels will be equipped to improve their performance.

PROBLEM STATEMENT: Have you ever wondered when the best time of year to book a hotel room is? Or the optimal length of stay in order to get the best daily rate? What if you wanted to predict whether or not a hotel was likely to receive a disproportionately high number of special requests? This hotel booking dataset can help you explore those questions! This data set contains booking information for a city hotel and a resort hotel, and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things. All personally identifying information has been removed from the data. Explore and analyse the data to discover important factors that govern the bookings.
Main Libraries to be used:
    Pandas for data manipulation, aggregation
    Matplotlib and Seaborn for visualisation and behaviour with respect to the target variable. Use at least 5 different visualisations.
    NumPy for computationally efficient operations
    
OBJECTIVE: We are provided with a hotel bookings dataset. Out main objective is performing EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other. I have tried to do a simple analysis of hotel booking data using matplotlib and seaborn libraries.

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

DATA VISUALIZATION: The Data analysis is performed to answer the following questions.
1.	What is the portion of each hotel type (i.e. City hotel. Resort hotel)
  ![CHART 1](https://user-images.githubusercontent.com/124367258/216624363-1eacb9c6-4909-4de1-9fac-fd78a7e1d94e.JPG)
It seems city hotel has larger portion compared to resort hotel which is almost double in portion. The reason could be that the resort hotel would be expensive     compared to city hotel. Most of the business stratagies should focus more on city hotel compared to resort hotel.

2. What is the percentage of cancellations and non-cancellations of each hotel types.
	![CHART 2](https://user-images.githubusercontent.com/124367258/216622097-78fa86f3-967f-4dc7-8e99-1ac387e56026.JPG)
  After seeing the data, we can say that the cancelled vs non-cancelled bookings ratios are different for the different types of hotels. For the City Hotel, 58.28% of the bookings were non-cancelled vs 41.72% of the bookings that were cancelled, forming a majority. In contrast, for the Resort Hotel, 72.24% of the bookings were non-cancelled whereas 27.76% of the bookings were cancelled.Hence proper business tactis should be implemented to find the reasons for cancellations and countermeasures should be taken to reduce cancellations.
  
3.	What is the total arrival trend of adults, children and babies from 2015-2017-time period.
![CHART3](https://user-images.githubusercontent.com/124367258/216622804-e6548f74-33ab-445f-a9c5-305a8182d90b.JPG)
The total number of arraivals of adults, with children, and with babies is higher for year 2016. The people travelling with babies preferred resort hotel than city hotel.In order to increase the same people more focus and improvements may be made that could increase revenue. There is large difference in total arrivals of adults between city hotel and resort hotel.

4.	What is number of cancellations and non-cancellations for each deposit type (i.e No deposit. Non-refundable, and Refundable) for all hotel types.
![4 1](https://user-images.githubusercontent.com/124367258/216623030-9926ead8-682b-481b-81c0-2c3f8a7fdf20.JPG)
![4 2](https://user-images.githubusercontent.com/124367258/216623067-e8a462a5-ee86-4a2f-9285-e208527c88e4.JPG)
When we see at the graphs of bookings for both canceled and non-canceled for each deposit type. we see that the bookings with no deposit taken form the majority. There is a large difference between no deposit bookings and the other types. The bookings with non refund deposit type has more cancellations than non-cancellations.The non-refund deposit types are most likely to be cancelled than other deposit types. The above graphs helps to identify most likely cancelled desposit types which has no singinificance on business.

5.	What is count of monthly arrivals, weekly arrivals and daily arrivals for all months for both the hotel types.
![5m](https://user-images.githubusercontent.com/124367258/216623620-2129a0f3-884f-47d5-9171-4f4539706d79.JPG)
![5w](https://user-images.githubusercontent.com/124367258/216623710-48c942b6-50a9-45e8-a5ad-7f53f2a865ee.JPG)
![5d](https://user-images.githubusercontent.com/124367258/216623757-b748eecf-a282-437a-a423-5286c9285247.JPG)
There is increase in demand of hotel bookings during middle of year for city hotel. But for the resort hotel its only during July and August, where rain season is about to end and winter season is about to start. The same trends can also bee seen from the weekly arrivals also. For the daily arrivals for all months, it is roller coster like trend.

6.	What is the count of group of people staying on weekdays nights and weekends nights.
![6n](https://user-images.githubusercontent.com/124367258/216624559-ebd5e8c9-31d9-4936-a6bd-6c6fdfeb2e25.JPG)
![6day](https://user-images.githubusercontent.com/124367258/216624603-748f98c2-c5dd-4468-b2a9-6f68c00aab21.JPG)
![6changes](https://user-images.githubusercontent.com/124367258/216624684-d6097d34-23a9-49e6-92e8-a4258b4c267f.JPG)
From trend in the above graph, It can been seen that majority of stays are on weekends. The revenue of hotels can be incresed by encouraging weekend visitors to stay longer by sending them a promo code shortly after they have booked their rooms to let them know about your great deal. You can give them a small discount if they decide to extend their stay into the week as weekday customers is alreday less compared to weekend.

7.	What is the count of reserved and assigned room types of both the hotels. And also the count of booking changes for all room types of both the hotels.
![6a](https://user-images.githubusercontent.com/124367258/216625092-d7c5851c-e852-40fc-98f9-f652f28aa2bf.JPG)
![6assig](https://user-images.githubusercontent.com/124367258/216625167-59a0ad59-db2c-45cd-971c-e6e4bd0c1286.JPG)
![6changes](https://user-images.githubusercontent.com/124367258/216625211-309c700b-9db2-48a2-bdf4-8e0497d56329.JPG)
Most of the customers booked A type room followed by D type and E type. The remaining room types have less bookings comparatively. Most of the customers booked got their reserved rooms only for all the room types and less customers have got different room type form their booked type.The same can also be analysed from booking changes trend which shares the similar information.

8.What is count of customer’s types, market types, and distributions types. What is the count of cancellations and non-cancellations of all the market types (i.e. Direct, corporate, online TA, offline TA/TO, complementary, groups, and Aviation) for both the hotels.
![7customers](https://user-images.githubusercontent.com/124367258/216625403-a1f2ac84-5183-4438-81ea-7fdfa15bab12.JPG)
![7market](https://user-images.githubusercontent.com/124367258/216625437-db50abe3-87bd-4d72-adaa-91187306e20c.JPG)
![7distri](https://user-images.githubusercontent.com/124367258/216625465-afa19392-0eec-4485-9597-9b7d73ec9b8b.JPG)
![7city](https://user-images.githubusercontent.com/124367258/216625499-4cd87346-d0d0-4238-b4c1-8605f8f5cb2a.JPG)
![7resort](https://user-images.githubusercontent.com/124367258/216625519-83853942-7c59-4166-b4fe-62c769917aa7.JPG)
Majority types of customers are transient type, followed by transient-party. The contract types and group types are comparatively less. Hence, With the ease of booking directly from the website, most people tend to skip the middleman to ensure quick response from their booking.

Majority of the distribution channels and market segments involve travel agencies (online or offline).We can target our marketing area to be on these travel agencies website and work with them since majority of the visitors tend to reach out to them.

The cancellations are more comapred to non-cancellations for groups type for city hotel type, for the resort hotel type the cancellations are slightly less compared to non cancellations. But major cancellaions are coming from the groups type.

9.	What is correlation of variables among each other.
![9](https://user-images.githubusercontent.com/124367258/216625710-c08fd97b-4334-499e-86e4-dc09e92f8413.JPG)
A mild negetive correlation of 54% is found between arrival date year and arrival date month. A correlation of 49% is found between number of stays on weekdays and weekends. Rest all variables have significantly low correlation among each other.

10.	What is the overall dirtibution of lead time. And also the individual distribution for both hotels.
![10overall](https://user-images.githubusercontent.com/124367258/216625971-a97daf28-f9b1-4734-b30b-14c92cf45f4a.JPG)
![10 individual](https://user-images.githubusercontent.com/124367258/216626006-a14e3b2c-d087-4480-825c-61d754d6e3df.JPG)
Most of the distribution of lead time is in the range of 0-100 for both the hotel types.The lead time is not the major reason fo the cancellations.

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


















  
	


