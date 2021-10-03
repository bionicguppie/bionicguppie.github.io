---
published: true
layout: post
title: Email Flow in Power Automate
---
One of the tasks that I do on a regular basis is send out an email to multiple people that mostly has consistent information, with just a few different variables depending on the person. Since this is sent out to more than 20 people at a time, it can be difficult to keep track of which information goes to which person and if I'd sent the email to that individual yet. 

I made a very simple flow in Microsoft Power Platform to send out an email to each individual using an excel spreadsheet. This allows me to use variables from the spreadsheet in the body of the email without having to use mail merge. 

![Overall Flow.png]({{site.baseurl}}/_posts/Overall Flow.png)

For a Flow, something has to trigger it. Currently, I use a "button", though in practice it just means that the Flow will run one time when I test it. 

The flow starts with an excel table. It uses the step called "List rows present in a table. The step needs to know where the file is located and the file needs to be formatted correctly. For this step to work, there needs to be a "key" column in the file. The key column is just numbers, 1 through however many items you need to send. Each email row needs it's own number.

![excel table formatting.png]({{site.baseurl}}/_posts/excel table formatting.png)

The next step is "Apply to each" for each of the rows you've listed. Within that step, you'll have the step "Send an email (V2)" The Apply to each step takes the variables from each row and applies them to whatever step you put inside the Apply to each step. So in this instance, I'm taking variables such as their email address and their first name and applying those to each email that is sent.

![email variables.png]({{site.baseurl}}/_posts/email variables.png)
