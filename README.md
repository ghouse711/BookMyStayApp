# BookMyStayApp

# Use Cases (Short Summary)

***

## **1 Room Inventory Setup & Management**

**Data Structures:**

*   `HashMap<String, Integer>` → room type → available count
*   `HashMap<String, Double>` → room type → price per night

**Key Features:**

*   Initialize room types (Single/Double/Suite)
*   Update counts and pricing
*   Real-time availability

**Why:** Fast O(1) lookups, centralized inventory.

***

## **2 Room Search & Availability Check**

**Data Structures:**

*   Same HashMaps (read-only access)

**Key Features:**

*   Display available rooms
*   Show pricing/amenities
*   Prevent searching unavailable rooms

**Why:** Ensures accurate availability without modifying inventory.

***

## **3 Booking Request (First-Come-First-Served)**

**Data Structure:**

*   `Queue<Reservation>` (LinkedList)

**Key Features:**

*   FIFO booking fairness
*   Handles peak traffic
*   Avoids race conditions

**Why:** Ensures fair, ordered booking processing.

***

## **4 Reservation Confirmation & Room Allocation**

**Data Structures:**

*   `Set<String>` → booked room IDs
*   `HashMap<String, Set<String>>` → room type → assigned rooms

**Key Features:**

*   Generate unique room IDs
*   Prevent duplicate allocation
*   Update inventory atomically

**Why:** Guarantees zero double-booking.

***

## **5 Add-On Service Selection**

**Data Structure:**

*   `Map<String, List<Service>>` → reservation ID → services

**Key Features:**

*   Attach multiple services (breakfast/spa/pickup)
*   Track additional charges

**Why:** Clean one-to-many reservation → services mapping.

***

## **6 Booking History & Reporting**

**Data Structure:**

*   `List<Reservation>`

**Key Features:**

*   Store all confirmed bookings
*   Support reports & cancellations
*   Historical audit trail

**Why:** Easy retrieval and customer support.


