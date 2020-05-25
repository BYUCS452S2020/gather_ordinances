# Project Schema

* users (id, username, password, first_name, last_name, email, created, updated)
  * Primary Key id

> **Explanation:** We will need to keep track of a user's log in information.   
> **Entity Represented:** The user who is signed in.  
> **Relation to Other Tables:** Users can have saved preferences (preferences) and can reserve ordinances for family members (reserved_persons). Other tables have a foreign key reference to the users table.  
> **Evidence of Normalization:** 3NF all columns have atomic values, only has one column for the primary key and no candidate keys, all columns are functionally dependent on primary key (single user cannot have multiple usernames and passwords, etc.)  
> **Explanation of Column Names:** We wanted to know when the user
was created (created) as well as when it was last updated (updated) 
for security reasons. We need the email (email) to notify the user 
of any changes made to their username (username) and/or their
password (password) in case it wasn't made by them. We want the 
user's first and last names (first_name, last_name) for a friendlier
and more personal experience with the site. We are using an internal 
key (id) to represent a user. 

* reserved_persons (family_search_id, first_name, last_name, gender, updated) 
  * Primary Key family_search_id

> **Explanation:** These are the deceased family search persons that a user has reserved ordinances for     
> **Entity Represented:** Deceased individuals on family search     
> **Relation to Other Tables:**  These persons can be reserved by users. Many to many relationship, linking table links users to reserved_persons.    
> **Evidence of Normalization:** 3NF all columns have atomic values, only has one column for the primary key and no candidate keys, all columns are functionally dependent on primary key (reserved persons cannot have multiple genders or names)   
> **Explanation of Column Names:** We are retrieving each person from family search and because the family search ids are guaranteed to be unique, that is an external primary key (family_search_id). We only need to store each person's first and last names (first_name, last_name) and gender (gender) for the statistics we are going to offer. The updated column is a timestamp used to keep track of when this data is updated.  

* preferences (id, name, description)
  * Primary Key id

> **Explanation:** This is a series of preferences a user can store in regards to how they want their ordinances reserved   
> **Entity Represented:** Preferences available for limitations on what ordinances that the script reserves.  
> **Relation to Other Tables:**  Many to many relationship, linking table links preferences to users. Users can have multiple sets of preferences.  
> **Evidence of Normalization:**  3NF all columns have atomic values, only has one column for the primary key and no candidate keys, all columns are functionally dependent on primary key (preferences cannot have multiple names or descriptions etc)  
> **Explanation of Column Names:** Preferences can have a name, and a short description that will show when the preference name is hovered over by the user. ID is an internal key guranteed to be unique, used in the linking table to connect a user to a specific preference.
