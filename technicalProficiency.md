---
layout: page
title: Technical proficiency
permalink: /Technical proficiency/
---

#### What is the overall quality of your code like?  
  
# ★ ★ ★ ★ ★
  
I believe that the overall quality if my code is excellent. I am fortunate to have had some prior experience with the technologies used in the project, e.g. HTML, PHP, MySQL, etc.  
I found the coding to be one of the most enjoyable aspects of the project.
  
``` 
    function createEquipment($pdo,$equipment,$incidentID)
    {
        // insert data using prepared statement
        $insertQuery = "INSERT into equipment(type, make, model, partNum, serialNum, yearOfManufacture, description) VALUES (:type, :make, :model, :partNum, :serialNum, :yearOfManufacture, :description)";
        $stmt = $pdo->prepare($insertQuery);
        $stmt->execute($equipment);
        // We will need the last inserted id in the equipment table as a foreign key
        $equipmentID = $pdo->lastInsertId();
        // Because there is a many-to-many relationship between incident and equipment, we need to use a linking table
        createIncidentEquipment($pdo, $incidentID, $equipmentID);
        // We also need the last used equipment ID back in the controller
        return $equipmentID;
    }

    function createIncidentEquipment($pdo, $incidentID, $equipmentID)
    {
        // insert data into the incidentEquipment linking table
        $insertQuery = "INSERT into incidentEquipment(incidentID,equipmentID) VALUES (:incidentID,:equipmentID)";
        $stmt = $pdo->prepare($insertQuery);
        $stmt->bindParam(':incidentID',$incidentID);
        $stmt->bindParam(':equipmentID',$equipmentID);
        $stmt->execute();
    }
```  
  
#### How well did you follow best practices in development?
  
# ★ ★ ★ ★ ★  
  
Where possible, and to the best of my knowledge, I have followed best practices in development.  
    - Code has been well commented  
    - A naming convention was decided on early and adhered to  
    - The code has been kept simple, wherever possible  
    - The code has been made as portable as possible, e.g. using relative file paths instead of absolute  
    - Where practicable we have reused code, e.g. the models that interface between the controllers and the database  
    
#### How well did you use appropriate version control?
  
# ★ ★ ★ ★ ★ 
  
Version control has been a life saver several times throughout the project. The ability to work concurrently on a single file and then merge the changes was a must have for a team working remotely. I still find Git to be confusing at times, but I am much more familiar with it than a few months ago. I was particularly impressed with Visual Studio Code's Git implementation, which allowed you to commit, push, etc. (note the highlighted sections in the below image).  
Finally I need to mention the amazing ability to roll back to an older commit; it really saved me after I broke this portfolio a few nights ago!
  
![Code's Git interface]({{ "/files/img/code_gitjpg" | absolute_url }})  

#### To what extent do you think you contributed an equal portion of the overall project?
  
# ★ ★ ★ ★ ★  
  
I initially felt that I had not had as much time to dedicate to the project as my colleagues; however, after talking to the team I received some very humbling feedback about the quality and nature of my input. In short, they all seemed very happy with the technical skills that I brought to the team. I don't have as many commits as some of the other guys on the team, but on more than one occassion I could be found bouncing from one desk to another; helping troublshoot issues, pair programming, or just guiding someone to discover a solution . . . It was actually really fun, I see why you do it!
  
