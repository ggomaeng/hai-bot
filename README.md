#Hai_BOT

Hai is designed to dynamically connect people. It analyzes what the user is requesting for, and it reaches out to match with someone who can fulfill the request.

##Data Structure
received chat JSON example:

```bash 
        {
            "object":"page",
            "entry":[
                {
                    "messaging":[
                        {
                            "message":{
                                "text":"does this work?",
                                "seq":20,
                                "mid":"mid.1466015596912:7348aba4de4cfddf91"
                            },
                            "timestamp":1466015596919,
                            "sender":{
                                "id":"885721401551027"
                            },
                            "recipient":{
                                "id":"260317677677806"
                            }
                        }
                    ],
                    "time":1466015596947,
                    "id":"260317677677806"
                }
            ]
        }
```

##Example:
1. One user requests for someone
    - i.e) "Hai, I'm looking for someone who's willing to sublet next semester."
    - Hai uses named entity recognition to analyze the request
    - person: 'anyone', keyword: 'sublet', place: 'new york'
2. If there is already a user looking for a sublet in our DB, it sends a message to both users to connect them.
    - If not, save the user under that keyword.

Hai: "Hello "$name," what are you looking for today? Here are some commands you can ask:
- "Hai, I'm looking for someone who can teach me Algebra 2"
- "Hai, I'm looking for soneone who can share a ride to BWI tomorrow at 5:30pm"
- "-help"

User: "Hai, I'm looking for a designer."

Hai: "Found 325 designers; which one are you looking for?
- product designer
- logo designer
- transportation designer

User: "Logo designer."

Hai: "Connecting you to '$name'. Have a good day! 🙂"


------

Example 2 

User: "Hai, I'm looking for a study group for Discrete Math at Johns Hopkins University."

Hai: "It seems like "$name" is also looking for a study group. Connecting you to "$name". Have fun!"

------

Example 3

User: "Hai, I am looking for someone who can teach me programming."

Hai: "What kind of programming?"

User: "Machine Learning"

Hai: "I am sorry, but I couldn't find anyone for now; however, here are some of your friends who might know!
    - Keon Kim: shared '13' posts related to 'machine learning.'
    - Sung Woo Park: shared '3' posts related to 'programming'

------

Example 4

User: "Hai, I'm looking for a girlfriend."

Hai, "I'm sorry, but there are no one looking for a boyfriend yet. I will let you know if somebody asks!"