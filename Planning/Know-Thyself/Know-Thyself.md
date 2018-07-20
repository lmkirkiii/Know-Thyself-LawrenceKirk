# Welcome To Know-Thyself: Proposal Version
## A way to hear what you cannot see. 
---------------------------------------------------------------------------------------

## Project Proposal 

We are living in a world with constant external stimuli and a social facisnation on the external be it our material possessions, personal appearance or life achievements. Know ThySelf helps us take a break from this constant looking out to look in. Our app allows the user to provide information about there lives in a anonymous enviroment through a series of questions, activities, and tests. Once the user passes through the assesment they will recieve a series of relfections based on the nature of their responses allowing them to better see who they are. 

---------------------------------------------------------------------------------------

## Models Used

- Users

```
const Users = new Schema({
   userinfo: { 
    name: String,
    age: String, 
    firstTimeTakingQuiz: Boolean,
   },
   answers: [
       {
           type: Schema.Answer.ObjectId,
           ref: "answer"
       }
   ]
});
```

- Answer
```
const Answer = new Schema({
    content: String,
    author: {
        type: Schema.Types.ObjectId,
        ref: "User"
    }
   
});

```

- Response 

```

const Response = new Schema({
    content: String,  
});

```

- UserFeedback 

```
const Comment = new Schema({
  content: String,
  author: {
    type: Schema.Types.ObjectId,
    ref: "User"
  }
});

```
---------------------------------------------------------------------------------------




