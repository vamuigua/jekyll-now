---
layout: post
title: Encapsulation:Getter and Setter Methods
---
**Encapsulation**<br>
-This is simply the hiding of information or data from other objects within the same class.<br>
-Information is hidden from other objects in the same class using the keyword *'private'*<br>

            Example:

            private int Phone = 18
            private string name = "Victor"

-The integer *18* and string *"Victor"* are hidden from other objects within the same class thus they are not in public view to be shared among the objects within the class.<br>            
-To enable information to be obtained or fetched from the object with its 'private' characteristics, the getter an setter methods, are used.<br>

**Getter**<br>
-The keyword *'get'* is used to fetch or extract a 'private' variable in an object:<br>

            Example:
            Public class Party{
              private int Phonenumber;

            Public int getPhonenumber(){     //getter method
              return Phone no;
            }  
            }

**Setter**<br>
-The keyword *'set'* is used to display the variable that is fetched when the *'get'* keyword is used:<br>

            Example:            
            Public void setPhonenumber(int x){     //setter method
              this.Phonenumber = x;
            }

-The final output looks as follows:<br>

            Public class Party{
              private int Phonenumber;

            Public int getPhonenumber(){     //getter method
              return Phone no;
            }  
            }

            Public void setPhonenumber(int x){     //setter method
              this.Phonenumber = x;
            }
