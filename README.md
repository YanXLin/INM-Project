# INM-Project

Created by Andrew Cornelio and Yan Lin

1.  Create a network map that help the users find the closest available room on campus from any given location
	* Nodes: Physical locations of rooms/buildings on campus 
	* Edges: Distance between rooms/buildings
	* Description: Run Shortest Path Algorithm to shortest rooms by minimum distance. Select closest available room
2. Generate a class schedule that matches ‘n’ meetings/classes with classes with ‘m’ rooms. Refer to section 5.2 of this pdf: http://pages.cs.wisc.edu/~shuchi/courses/787-F09/scribe-notes/lec5.pdf. 
	* Nodes N1: Available class rooms and meeting times.
		* Each classroom has k, one hour length time slots during which it can be used
		* Each classroom has a certain capacity and can hold at most this many students
		* Classes are in buildings with a school designation (AS or EN)
	
	* Nodes N2: Classses that want to meet
		* Due to professor availability, classes can only meet at certain one hour time slot
		* Classes can have many students registered, and must meet in a room that has sufficient capacity
		* Classes must meet in rooms with the correct school designation (AS or EN)

	* Edges: An edge signifies that a class can meet at a certain room at a certain time, according to the constraints above.
	* Description: The above requirements create a bipartite graph. Since only one class can meet in a certain room at a certain time, the task is to find a matching, namely the matching which maximizes the number classes that will meet.
