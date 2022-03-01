# What is JsonPowerDB?
JsonPowerDB is a Real-time, High Performance, Lightweight and Simple to Use, Rest API based Multi-mode DBMS. JsonPowerDB has ready to use API for Json document DB, RDBMS, Key-value DB, GeoSpatial DB and Time Series DB functionality. JPDB supports and advocates for true serverless and pluggable API development. 

# Features of JsonPowerDB 
1) Simple to use
2) Real-time DBMS.
3) Multiple security layers.
4) Schema free - easy to develop and maintain.
5) Server side Native NoSQL - best query performance.
6) In-built support to query on multiple JPDB databases.
7) Multi-mode DBMS - Document DB, Key-Value DB, RDBMS support.
8) JsonPowerDB (JPDB) is Next Generation, Creative and Disruptive Multi-mode DBMS_ with many USPs.
9) Proprietary algorithm for High Performance CRUD operations. Multiple times faster than popular DBMS.
10) Serverless support for faster development - A UI developer can develop complete dynamic application.
11) DBMS with built in web / application server and embedded caching makes the performance lightning fast.
12) Web-services API - Can be used with any programming language that has support for HTTP.
13) Enriched by a pluggable API Framework - A developer can develop a pluggable API and plugin into any of our cloud JPDB instance.
14) Standardisation of API development framework makes the development process easy, more readable, and less error prone.

# Website/ Reference
https://login2explore.com/

# Docs
https://login2explore.com/jpdb/docs.html

# Deshborad Screenshoots
![image](https://user-images.githubusercontent.com/71280861/156116374-20163c71-47d4-44ca-bb8a-b910981f5c9f.png)

![image](https://user-images.githubusercontent.com/71280861/156116411-c72218f0-856e-4750-99fa-0e9fb799cfa5.png)

<img width="960" alt="image" src="https://user-images.githubusercontent.com/71280861/156116486-88096fad-209b-4d72-9552-6565cb11c6ed.png">

# Required Installation
Step 1: Visit to the Chrome Extensions Web Store https://chrome.google.com/webstore/search/talend%20api%20tester?hl=en-US 

Step 2: Add and install the Talend Api Tester 

![image](https://user-images.githubusercontent.com/71280861/156116899-d48a44cd-bf79-4dc2-a099-2bc125d4c2ad.png)

Step 3: Visit to the Chrome Extensions Web Store https://chrome.google.com/webstore/search/Netben%20connector?hl=en-US

Step 4: Add and install the NetBeans Connector 

<img width="958" alt="image" src="https://user-images.githubusercontent.com/71280861/156117159-9dc0d91e-2f3d-4e38-b14a-62fea310ec1d.png">

# Sample JsonPowerDB_Project Explanation

1) In this project I have created a simple "Employee Form" using NetBeans Connector that have three different input fields - Employee ID, Employee Name and Email

<img width="960" alt="image" src="https://user-images.githubusercontent.com/71280861/156119263-542a3c15-654f-4498-9a3d-23cd63506113.png">

2) I have also created some required functions that is required for the funcationality and working of the form such as:

2.1) validateAndGetFormData(): This method/function is used to VALIDATE the data inserted into the form.
  * If there is any empty field or no data is inserted into any of the fields then it will push a "alert" message and change the cursor focus on that field. 
    
    <img width="960" alt="image" src="https://user-images.githubusercontent.com/71280861/156123097-1d3c0233-c700-48a3-8895-bb1d665bb016.png">
   
   * If the input data is correct then the function will create a json object "jsonStrObj" that will contain the input data as a JSON String and return the "jsonStrObj".
     
     <img width="960" alt="image" src="https://user-images.githubusercontent.com/71280861/156123032-c61b3f44-6611-495c-9f8b-59b7774d0b1d.png">

2.2) createPUTRequest(): This method is used to create PUT Json request.
  * Inorder to save the input data to the DB, we need to use "PUT" request to further process the data to the Database.
  * This function required - Connection Token, jsonObj, Database Name and Realtion Name as a parameter to convert it to a proper executable syntax and return the format              as "putRequest"
  ** Refer official Documents for more info about the token, url, etc.
   
2.3) executeCommand(): This method is used to EXECUTE the request.
  * Inorder to execute the "PUT" request to further process the request to the Database.
  * This function required - reqString, DB Base Url, API EndPoint Url as a parameter to create a complete "URL"
  * Now using some predefined library the fuction used to parse the "jsonObj" data and execute it.
  * A execution status will be return whether it is executed successfully or failed and return the "jsonObj". 
        
   <img width="960" alt="image" src="https://user-images.githubusercontent.com/71280861/156123234-423061fc-1513-425e-98ae-c5b888451462.png">
        
 2.4) resetForm(): This method is used to create RESET the form.
  * Inorder to avoid duplicate data insertion we need to rest the form back and reset it to default state.
  * This function will set the values of Employee ID, Employee Name and Email to "" and reset the cursor focus. 
   
   <img width="960" alt="image" src="https://user-images.githubusercontent.com/71280861/156123326-9f90111f-1920-4c51-bf47-06ce846cdddb.png">

        
3) saveEmployee(): This method is used to create SAVE/UPDATE the form data into DB.
   * First we will call the validateAndGetFormData() method to check the input data.
   * Now creating a "Put" request for example: 
     var putReqStr = createPUTRequest("90938846|-3194883564511846?|90945747", jsonStr, "Employee", "index")
   * Now executing the request to update the data into the database. 

4) To Visualize the the update or records follow the following steps. 
  
   1) Visit http://api.login2explore.com:5577/ and loggin to the account
   2) Select the Visualize option in the left side and click on JsonDb
   3) Select the Database and Relation we used at the time of creating "PUT" request 
      
      <img width="959" alt="image" src="https://user-images.githubusercontent.com/71280861/156124081-8119f274-c111-47db-872d-6e829dfc91b5.png"> 
   
   4) Check the records.
      
      <img width="960" alt="image" src="https://user-images.githubusercontent.com/71280861/156124203-fa39fbe7-20a3-49e1-94e8-c9264117697b.png">

