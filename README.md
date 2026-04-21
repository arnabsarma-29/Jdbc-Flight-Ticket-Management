# Flight Ticket Booking System (JDBC Project)

A Java-based console application that simulates a flight ticket booking system using JDBC and PostgreSQL. It handles passenger details, flight details, and payment processing using transaction management.

---

## Features

- Add passenger details
- Add flight details
- Process payment
- Transaction management using JDBC
- Ticket generation based on payment status
- Rollback support if payment fails

---

## Tech Stack

- Language: Java
- Database: PostgreSQL
- Connectivity: JDBC
- Concepts Used:
  - Transaction Management
  - Savepoint & Rollback
  - PreparedStatement
  - DAO Pattern

---

## Project Structure

```
com.jspider_jdbc_project.flight_ticket/

    model/
        Passenger.java
        Flight.java
        Payment.java

    dao/
        Dao.java

    database/
        Db_Connection.java
```

---

## How It Works

- Passenger details are inserted first
- A savepoint is created after passenger insertion
- Flight details are added separately
- Payment is processed last
- If payment is successful:
  - Transaction is committed
  - Ticket is generated
- If payment fails:
  - System rolls back to passenger savepoint
  - Ticket is not generated

---

## Database Configuration

```
URL: jdbc:postgresql://localhost:5432/jdbc_ticket
Username: postgres
Password: 123
```

---

## Core Logic Flow

1. Insert Passenger
2. Create Savepoint
3. Insert Flight Details
4. Insert Payment Details
5. Check Payment Status
6. Commit or Rollback Transaction

---

## Key Concepts Used

- JDBC (Java Database Connectivity)
- Transaction Management
- Savepoint handling
- Commit & Rollback
- DAO pattern
- Exception handling

---

## How to Run

1. Clone the project
```
git clone https://github.com/your-username/flight-ticket-system.git
```

2. Import into IDE (Eclipse / IntelliJ)

3. Setup PostgreSQL database:
   - Create database: jdbc_ticket
   - Update credentials in Db_Connection.java

4. Run main application (if available)

---

## Author

https://github.com/arnabsarma-29
