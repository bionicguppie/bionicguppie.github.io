---
published: true
layout: post
title: Email Flow in Power Automate
---
One of the tasks that I do on a regular basis is send out an email to multiple people that mostly has consistent information, with just a few different variables depending on the person. Since this is sent out to more than 20 people at a time, it can be difficult to keep track of which information goes to which person and if I'd sent the email to that individual yet. 

I made a very simple flow in Microsoft Power Platform to send out an email to each individual using an excel spreadsheet. This allows me to use variables from the spreadsheet in the body of the email without having to use mail merge. 

![Overall Flow.png]({{site.baseurl}}/images/Overall Flow.png)

For a Flow, something has to trigger it. Currently, I use a "button", though in practice it just means that the Flow will run one time when I test it. 

The flow starts with an excel table. It uses the step called "List rows present in a table". The step needs to know where the file is located and the file needs to be formatted correctly. For this step to work, there needs to be a "key" column in the file. The key column is just numbers, 1 through however many items you need to send. Each email row needs it's own number. In this file, I used "ID" for the key column.

![excel table formatting.png]({{site.baseurl}}/images/excel table formatting.png)

The next step is "Apply to each" for each of the rows you've listed. Within that step, you'll have the step "Send an email (V2)" The Apply to each step takes the variables from each row and applies them to whatever step you put inside the Apply to each step. So in this instance, I'm taking variables such as their email address and their first name and applying those to each email that is sent.

![email variables.png]({{site.baseurl}}/images/email variables.png)

You'll write out the email the same way you'd normally write an email, the only difference is adding in the dynamic content of the individual columns from the excel spreadsheet of the variables you want each email to have. In addition, you can put any variable you want in the file. If the date for an appointment is the same for everyone in the batch, but different each time you send it, you can include a Date variable so that you don't have to change the date in the email itself each time.