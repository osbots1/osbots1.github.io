---
layout: page
title: Professional proficiency
permalink: /Professional proficiency/
---

#### How often do you attend scheduled group meetings/scrums?  
  
# ★ ★ ★ ★ ½
  
I certainly tried my best to attend all scheduled meetings/scrums; however, I was unable to attend some of the in-class meetings due to work commitments. On the rare occasions when I was unable to attend, I would notify the group via Slack in advance. I would also try to make myself available via Slack during the meetings.  
As a group, we also had meetings after-hours, during weekends and during the Polytech holidays. These additional meetings were normally planned so that those off us with full and part time work commitments were able to attend without issue. 
  
![Team scrum]({{ "/files/img/scrum.jpg" | absolute_url }})  
  
#### How well did you communicate with others in your group or subgroup?  
  
# ★ ★ ★ ★ ★  
  
I feel that our team's communication level is one of our strengths. Most of our remote communication happens on Slack (see below).  
When we were face to face, we quite often had constructive debates about the direction we should be taking the project, the technologies involved and the ways in which we should employ those technologies. The conversations were not only constructive, but educational and enjoyable!
  
![Team communication]({{ "/files/img/coms1.jpg" | absolute_url }}) 
  

![Team communication]({{ "/files/img/coms1.jpg" | absolute_url }}) 
  
#### How well did you document your work throughout the project?  
  
# ★ ★ ★ ★ 
  
Yeah, about that . . .  
I feel that my documentation via Slack and in my coding, was excellent, but I was a bit remiss when it came to recording my work history as I went. There were two main reasons why I failed to document my work effectively:  
    1.  I am inherently lazy ;) 
    2.  I missed the first class and I was not aware that it was a requirement until quite late in the semester.
Below is a code snippet with documentation, so the team could understand what I was up to.  

``` 
       // Contact Details
            // Clean the contact input from the $_POST array
            $firstName = clean_input($_POST['firstName']);
            $lastName =  clean_input($_POST['lastName']);
            $phoneFixed =  clean_input($_POST['phoneFixed']);
            $phoneMobile =  clean_input($_POST['phoneMobile']);
            $email =  clean_input($_POST['email']);
            // Create an a person array
            $person = array('firstName' => $firstName, 'lastName' => $lastName, 'phoneFixed' => $phoneFixed, 'phoneMobile' => $phoneMobile, 'email' => $email); 
            // Call the createPerson() method. This will return the id of the new person item for use as a foreign key.
            $contactID = createPerson($pdo,$person);
```  

#### How well did you respond to problems or changing requirements?  
  
# ★ ★ ★ ★ ★  
  
I feel I coped well with changing requirements, of which there were many! The client's forms were quite varied in their structure, resulting in many alterations to the initial database design. After the database design was completed, the client surprised us with a new form for a Small Unmanned Vehicle. This form's fields were quite different from the others. I suggested that we ask the client if he would like us to "normalise" his form. This made the process for the team simpler, while still achieving a great result for the customer.  
  
