---
layout: project
type: project
image: img/hms.png
title: "Hotel Management System"
date: 2023
published: true
labels:
  - Team-based
  - C++
summary: "The finals project my group and I created for the ICS 212 class."
---
For the ICS 212 class, instead of a final exam, we did a finals project with a group. The project that we were prompted to do was to create a simple hotel management system using C++. The task itself wasn't necessarily challenging in terms of difficulty, but there was so many smaller tasks contributing to the entire system so the workload was much heavier. The project utilized everything we were taught in ICS 212 and how we approached the project was what was graded. 

Here is a snippet of the code that I added on: 
```cpp
int HMS::menu() {
	int exit = 1;
	cout << "\n######## Hotel Management ########\n" << endl;
	cout << "1. Manage Rooms\n2. Check-In Room\n3. Available Rooms\n4. Search Customer\n5. Check-Out Room\n6. Guest Summary Report\n7. Load Default Hotel\n8. Load Default Guests\n9. Exit\n" << endl;
	
	int x = getInput("Enter Option: ", 1, 9);
	switch (x) {
		case 1:
			manageRooms();
			break;
		case 2:
			checkIn();
			break;
		case 3:
			getAvailableRooms();
			break;
		case 4:
			if (numGuests == 0){
				cout << "No guests checked-in." << endl;
			} else {
				searchGuest();
			}
			break;
		case 5:
			if (numGuests == 0){
				cout << "No guests checked-in." << endl;
			} else {
				checkOut();
			}
			break;
		case 6: 
			guestSummary();
			break;
		case 7:
			loadHotel("default.csv");
			break;
		case 8:
			loadGuests("defaultGuests.csv");
			break;
		case 9:
			quit();
			exit = 0;
			break;
		default:
			cout << "Please follow the instructions carefully." << endl;
			break;
	}
	return exit;
}
```
Unfortunately, I am unsure if you could fully view the code. 
