# Models 

- Users

```
const Users = new Schema({
   userinfo: { 
    name: String,
    age: String, 
    profile-picture: String, 
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