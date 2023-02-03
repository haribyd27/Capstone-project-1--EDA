# Capstone-project-1--EDA
INTRODUCTION: In this I have attempted to analyse the dataset of hotel bookings. The dataset consists of 119390 records across 32 features and has been given with information regarding bookings of two hotels from July 2015 to August 2017. These two hotels are City Hotel and Resort Hotel. It also explores vast information of these two hotel types such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things, etc. When running a successful and demanding hospitality business, most of the owners like a hotel that is running at its full capacity and bringing in large revenue. Most of the time hotel booking cancellations can be hurtful to business owners, although sometimes there are genuine reasons for guests to do so. These last-minute cancellations can result in lost revenue unless some measures are undertaken to mitigate the loss. The purpose of this project is to analyse Hotel Bookings data, investigate cancellations, and their underlying patterns and suggest measures that can be implemented to reduce cancellations and secure revenue. The main objective is to explore the given dataset and discover the factors which govern the bookings. The dataset will be analysed and from the conclusions drawn from it will be used to recognize the missteps taken by the manager. With this information, hotels will be equipped to improve their performance.

PROBLEM STATEMENT: Have you ever wondered when the best time of year to book a hotel room is? Or the optimal length of stay in order to get the best daily rate? What if you wanted to predict whether or not a hotel was likely to receive a disproportionately high number of special requests? This hotel booking dataset can help you explore those questions! This data set contains booking information for a city hotel and a resort hotel, and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things. All personally identifying information has been removed from the data. Explore and analyse the data to discover important factors that govern the bookings.

  Main Libraries to be used:
    Pandas for data manipulation, aggregation
    Matplotlib and Seaborn for visualisation and behaviour with respect to the target variable. Use at least 5 different visualisations.
    NumPy for computationally efficient operations
    
OBJECTIVE: We are provided with a hotel bookings dataset. Out main objective is performing EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other. I have tried to do a simple analysis of hotel booking data using matplotlib and seaborn libraries.

VARIBLE DESCRIPTION:
hotel: Name of hotel ( City or Resort)
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
