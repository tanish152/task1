📊 Hotel Bookings Exploratory Data Analysis (EDA)
📁 Project Overview
This project performs Exploratory Data Analysis (EDA) on a hotel bookings dataset that includes information about bookings in two types of hotels — City Hotel and Resort Hotel. The goal is to uncover insights and general trends that influence hotel bookings and understand how different features interact.

📌 Dataset Description
The dataset contains 119,390 rows and 32 columns. Each row represents a hotel booking record. The data includes both categorical and numerical variables related to customer behavior, booking preferences, and hotel attributes.

🏨 Key Features
hotel: Type of hotel (City Hotel or Resort Hotel)

is_canceled: Booking cancellation status (0 = No, 1 = Yes)

lead_time: Number of days between booking and arrival

arrival_date_year, arrival_date_month, arrival_date_week_number, arrival_date_day_of_month: Arrival information

stays_in_weekend_nights, stays_in_week_nights: Duration of stay

adults, children, babies: Guests information

meal: Meal type

country: Country of origin of the customer

market_segment, distribution_channel: Booking channels

is_repeated_guest: Repeated customer status

previous_cancellations, previous_bookings_not_canceled: Booking history

reserved_room_type, assigned_room_type: Room types

deposit_type: Type of deposit made

agent, company: Booking agents and companies

days_in_waiting_list, customer_type, adr: Booking metrics

required_car_parking_spaces, total_of_special_requests: Additional services

reservation_status, reservation_status_date: Booking status

🧹 Data Cleaning and Feature Engineering
✅ Steps Performed
Removing Duplicates

All duplicate rows were identified and removed.

Handling Missing Values

agent and company: Replaced missing values with 0

country: Replaced missing values with 'others'

children: Replaced missing values with the column mean

Data Type Conversion

Converted children, agent, and company to integers

Converted reservation_status_date to datetime

Outlier Removal

One extreme outlier in adr (average daily rate) was removed

Feature Engineering

total_stay = stays_in_weekend_nights + stays_in_week_nights

total_people = adults + children + babies

📈 Exploratory Data Analysis (EDA)
Q1: Which room type is in most demand and which room type generates the highest ADR?
Most Demanded Room: Room Type 'A' was the most frequently reserved.

Highest ADR: Room Type 'H' had the highest average daily rate.

Q2: Which countries do most customers come from?
The top contributing country is Portugal, followed by United Kingdom, France, Spain, and Germany.

Most international customers are from Europe.

Q3: What is the percentage of bookings for each hotel type?
City Hotel accounts for approximately 66% of the bookings.

Resort Hotel accounts for approximately 34% of the bookings.

📉 Challenges Faced
Duplicate Data

A large number of duplicate records were found and had to be dropped.

Incorrect Data Types

Several columns required manual conversion to appropriate types.

Missing Values

Multiple columns had missing values, especially agent, company, and children.

Visualization Decisions

Choosing the right plots and techniques for insightful analysis required iterative experimentation.

🛠️ Tools & Technologies Used
Python

Pandas, NumPy – Data manipulation

Matplotlib, Seaborn, Plotly – Visualization

Jupyter Notebook – Interactive analysis

📌 Key Takeaways
City hotels receive more bookings than resort hotels.

Most customers are from European countries.

Room type 'A' is most booked, but room type 'H' is the most expensive.

Repeated guests make up a small but significant portion of total bookings.

ADR varies greatly depending on hotel type, room type, and customer segment.

