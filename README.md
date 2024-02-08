# Hotel Management System Database Project

## Overview

A hotel operates through various interconnected departments such as front office, booking and reservation, inventory management, quality control, security, housekeeping, and more. This database project aims to streamline the management of these operations by efficiently storing and managing hotel-related information.

## Functionality

- **Hotel Chains and Hotels**: Hotels can belong to hotel chains. Each hotel has multiple rooms and floors, and rooms can vary in type, price, and description.
- **Guest Management**: Tracks guest information including name, address, and city.
- **Booking Management**: Manages bookings based on dates, booking type, and room count.
- **Room Management**: Designates room types with standard rates, descriptions, and smoking allowances.
- **Rate Management**: Provides room rate periods for seasonal discounts.
- **Queries**: Supports various queries such as guest count per month, available rooms for a given date, hotel count per chain, booking count per customer per year, rooms booked per hotel per date, unique countries with hotels, available rooms in a hotel, hotels with URLs, and room rates for specific periods.

## Database Design

### Tables Breakdown

1. **Hotel_Chain**
   - Attributes: Chain_ID (Primary Key), Chain_Name

2. **Hotel**
   - Attributes: Hotel_ID (Primary Key), Chain_ID (Foreign Key), Hotel_Name, Hotel_URL, Star_Rating, Image_URL, Room_Capacity, Floor_Count, Address_ID (Foreign Key)

3. **Address**
   - Attributes: Address_ID (Primary Key), Street_Address, City, State, Country, Postal_Code

4. **Room_Type**
   - Attributes: Type_ID (Primary Key), Type_Name, Standard_Rate, Description, Smoking_Allowed

5. **Booking**
   - Attributes: Booking_ID (Primary Key), Guest_ID (Foreign Key), Room_ID (Foreign Key), Check_In_Date, Check_Out_Date, Booking_Type

6. **Guest**
   - Attributes: Guest_ID (Primary Key), Name, Address_ID (Foreign Key)

7. **Room**
   - Attributes: Room_ID (Primary Key), Hotel_ID (Foreign Key), Type_ID (Foreign Key), Room_Number

8. **Room_Rate_Period**
   - Attributes: Rate_Period_ID (Primary Key), Start_Date, End_Date, Rate

### Relationships

- Hotel_Chain (1) to Hotel (Many)
- Hotel (1) to Address (1)
- Hotel (1) to Room (Many)
- Hotel (1) to Room_Type (Many)
- Booking (Many) to Guest (1)
- Booking (Many) to Room (1)
- Guest (1) to Address (1)
- Room (1) to Room_Type (1)

## Additional Requirements

- Work in groups of 2 or 3 and track individual contributions.
- Each team member must submit a breakdown for at least 2 tables in the database.
- Normalize the database to 3rd normal form.
- Create an EER Model of the database structure.
- Include primary and foreign keys where appropriate.

## Conclusion

This Hotel Management System Database Project aims to provide an efficient and organized solution for managing hotel operations. With its comprehensive design and normalized structure, it enables seamless tracking and retrieval of hotel-related information, contributing to enhanced efficiency and customer satisfaction.

