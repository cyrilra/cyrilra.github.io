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
## Summary
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
Unfortunately, I am unsure if you could/allowed to fully view the code. 

## Roles and Reflection
My role in this group was to help produce function methods for the hotel management system menu itself. I added the main menu and another side menu for the system while the other group members worked on the Guest class, Room class, and the remaining members continued to work on the main function methods for the HM system. I can say I did my part, but the other group members did more of the heavy lifting for the system. I wish I could have done more, but they were incredibly talented and smart that I don't think my help would have done anything. Regardless, it was a learning experience regardless and I was still able to apply everything I learned in that class for the finals project. A massive thank you to my group members and wouldn't have done well without them!


