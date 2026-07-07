The system consists of six main entities: User, Operator, ChargingStation, Charger,
Reservation, and Review.
Here is the ER diagram for charging station booking system:
User: Can make reservations and leave reviews. Attributes: user_id (PK), username, email,
password.
Operator: Manages charging stations. Attributes: operator_id (PK), name, contact_info.
ChargingStation: Managed by an operator, contains multiple chargers, receives reviews.
Attributes: station_id (PK), name, location, operator_id (FK), total_chargers.
Charger: Belongs to a charging station, can be reserved. Attributes: charger_id (PK), type,
power_output, status, station_id (FK).
Reservation: Connects a user and a charger, tracks booking and real-time availability.
Attributes: reservation_id (PK), booking_time, start_time, end_time, status, user_id (FK),
charger_id (FK).
Review: Connects a user and a charging station. Attributes: review_id (PK), rating, comment,
timestamp, user_id (FK), station_id (FK).
Relationships:
Operators manage many ChargingStations.
Each ChargingStation contains many Chargers.
Users can make many Reservations and leave many Reviews.
Each Reservation links one User to one Charger.
Each Review links one User to one ChargingStation.
