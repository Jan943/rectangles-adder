# RectanglesAdderApp
Simple app in SpringBoot with Vaadin library

The goal was to create an application in Spring Boot that will have a JPA entity class called Rectangle.
The class should have fields: id, height, width.
Using the Vaadin library, a UI was created that allows adding new rectangles to the database.
Access to the database is visible at the endpoint: localhost: 8090 / figureDB.
After restarting the application, the data in the database is deleted (default Hibernate setting in application.properties)
An endpoint has also been created, thanks to which, after passing a figure name (for a rectangle and a triangle) and side lengths, it returns the perimeter of a given figure, e.g. figure = rectangle & a = 10 & b = 20 returns 20.
4 sets of data for rectangles were placed in the configuration file. These 4 rectangles were loaded into the program (at the time of start - a trick was used and instead of creating an endpoint, an annotation @EventListener was added, i.e. aspect programming was used) and then placed in the database.
There is also a text field in the other GUI which, depending on the given value, displays rectangles from the database (using the repository) - large and small, e.g. small, where the circumference does not exceed 20j.
