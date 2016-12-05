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