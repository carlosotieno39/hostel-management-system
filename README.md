# hostel-management-systemHOSTEL MANAGEMENT SYSTEM - C ONLY

=================================

This is a console-based Hostel Management System entirely
in C.

PROJECT FILES
-------------
main.c
hostel.h / hostel.c
student.h / student.c
room.h / room.c
booking.h / booking.c
allocation.h / allocation.c
reports.h / reports.c
auth.h / auth.c
file_manager.h / file_manager.c

DATA FILES
----------
data/hostels.dat
data/rooms.dat
data/students.dat
data/bookings.dat
data/allocations.dat

COMPILE - GCC
-------------
All source files:
    gcc -Wall -Wextra -std=c11 *.c -o hostel_system

Linux/macOS:
    ./hostel_system

Windows:
    hostel_system.exe

DEFAULT LOGIN
-------------
Admin:
    Username: admin

Students:
    Select "Student Registration" from the main menu to create an account.

MAIN FEATURES
-------------
1. Admin login
2. Student registration/login
3. Add hostel
4. Add room
5. View all rooms
6. View vacant rooms
7. Student room booking
8. Admin room allocation
9. Student clearance
10. Current occupants report
11. Reserved rooms report
12. Allocated rooms report
13. Vacant rooms report
14. Persistent file storage
15. Input validation and double-booking prevention

PROJECT FLOW
------------
VACANT -> RESERVED -> OCCUPIED -> VACANT

Student books a vacant room:
    VACANT -> RESERVED

Admin allocates a valid reservation:
    RESERVED -> OCCUPIED

Admin clears the active allocation:
    OCCUPIED -> VACANT

The program prevents:
- Booking a reserved/occupied room
- Allocating a non-reserved room
- Allocating a room to a student who already has an active allocation
- Clearing a student who has no active allocation
- Invalid hostel/room/student IDs