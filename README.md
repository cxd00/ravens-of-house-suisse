# ravens-of-house-suisse

Our project, Project Osoleth, required us to create a web application that extracted specific information on a requested security from a client; intensive design planning was necessary to create a functioning application.  We began by realizing that we needed to integrate three separate programs to work seamlessly for a smooth user experience: a front end client facing programming, a back end Java program to extract data, and a framework to connect the two. Next, we used a front end JavaScript code to display a message for the user to input a message on what information they desired. This input was read as a JSON and formatted accordingly to the Bloomberg API. 

The ISIN was the extracted as a message from the JSON with regular expressions and the message was exposed with the restful API for display purposes. An AJAX query was then sent to the backend code with the ISIN and the backend Java code then sent out the specific information associated with the ISIN. The actual Backend code involved a lot of key decisions regarding data structures, as it stored all the values of the ISIN in a hash map by reading all the data from an excel sheet. The hash map essentially stored all ISIN’s as keys, mapping them to an object we created called ISINValues, which holds every value of the ISIN. The hash map allowed for O(1) searching for any ISIN key so clients could get their information quickly and efficiently. 

Due to the time restraints of the challenge, we were not able to use open source NLP libraries to interpret inquiries from the IB chats; interpreting these inquires would have been a challenging and engaging experience we would have been sure to gain a lot from.


