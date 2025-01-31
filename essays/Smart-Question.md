---
layout: essay
type: essay
title: "Why Choose TypeScript? Insights from a Researcher's Perspective"
# All dates must be YYYY-MM-DD format!
date: 2025-01-23
published: true
labels:
  - Research
  - Learning
  - Organization
---

<img width="200px" class="rounded float-start pe-4" src="../img/Diagrams-1.jpg">

In my eyes, smart questions are characterized by clarity, specificity, and completeness. They follow to established guidelines that facilitate efficient and effective responses from the community. For software engineers, mastering the art of asking such questions not only expedites troubleshooting but also contributes to a collective repository of knowledge that benefits the broader development community. Conversely, poorly framed questions can lead to misunderstandings, insufficient assistance, and a waste of valuable time for both the asker and potential responders.

## Organization is Key!

For one of my jobs I had to interview with, they asked me how I organized my code. As any average programmer would say, I would put sections and made sure my code is readable through the comments I put. Of course, there is much more to this as any good programmer should follow clean and responsible guidelines in how to format their code. However, as I said earlier, the languages I worked with would not provide "best practices" as good as TypeScript would in terms of being organized. For example, with TypeScript, it is very easy and effective to call out a variable whether it needs to be constant or changed. Here is a function that would calculate the sum of all of the numbers under 1000 (or any number you want) that are divisible by 3 or 5:

```
function projectEulerOne(num : number){
    let sum = 0
    for (let x = 10 ; x % 3 || x % 5 == 0 ; x--){
        sum += x
    } 

    return sum;

}
console.log(projectEulerOne(1000))
```

Notice the way the parameter is written and the variable "sum" has that "let" written. With this organization, I can clearly see the types of variables they are, whether they will be changed or if they are just some kind of string or number. Doing this over and over again and reading other people's codes with this good practice, it is just great in my opinion! 


