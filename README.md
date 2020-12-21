# ServiceOntario-wait-times
ServiceOntario releases their wait times and updates it quarterly. I analyzed one of their [datasets](https://data.ontario.ca/dataset/serviceontario-wait-times-and-call-volumes-contact-centres) which shows wait times and call volumes for contact centres. This dataset contains entries in terms of business queries, calls handled, average wait time, year and month. The data spans from 2016 to 2020 at the moment. To analyze the dataset I utilized [Power BI](https://powerbi.microsoft.com/en-us/) which is a business analytics tool that allows to create interactive visualizations.  

Unfortunately, the dashboard may become unavailable since Power BI requires an organizational account. I have attached both Power BI and a pdf version of the report in my [Github.](https://github.com/omarirfa/ServiceOntario-wait-times) which you can check out.


### Objectives
*   Devise a method to establish month and year relationship with the Power BI date format.
*   Create a model to show how ServiceOntario has catered to different business through out the years in terms of wait time and calls handled.
*   Produce insights on how average wait times varied for various businesses.


### Method
The excel file was loaded in and transformed using Power Query. First thing to do was to remove whitespaces, trim the data and change the data type for each column to their specific data types such as text, whole number etc. An issue that I addressed in Power Query was to make a date and month order column. Power BI organizes months in ascending order which makes the visualizations look odd. There are several ways to fix this but I decided to use this way, I made a new column using the calendar function and changed its data type to date. Then made a second column called monthorder which I then to set to as wholenumber. This column chronologically assigned numerical values to their respective months i.e. January == 1, February == 2 etc. Finally, to implement these changes we just had to sort the columns in our report tab by monthorder. Another way of doing this is by just using the calendar function in Power Query to create a column and assigning the calendar as a relationship to the month.

### Improvements
*   Can make predictions using Azures machine learning integration which is provided in Power Query.
*   Further plots could be made using R or Python scripts.
*   More relationships can be made with other applicable datasets from the ServiceOntario website.


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   
  
