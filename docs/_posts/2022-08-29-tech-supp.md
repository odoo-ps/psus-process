---
layout: post
title:  "Technical Support"
permalink: /techsupp/
date:   2022-08-29 10:19:51 -0700
categories: jekyll update
---

## Basic Rules to Follow
1. Communication is Key
   - Notify Reviewer(Consultant, Sales Person, etc.) of ticket progress
   - Remind Reviewer or Customer if there are pending items
     - Ex: need access to something, error logs, code
   - Do not leave a thread unanswered
     - Log note if the communication was done somewhere else(skype,discord,email)
2. Not sure what to do?
   - Consult with a senior member of the team or Jigar(jam)
     - Do not hesitate to ask questions, everyone is more than happy to help
   - Avoid spending time with random guessing or rabbit hole researching
   - If there is any issue with the ticket, ticket subject, or customer, reach out to the Team leader(cic) or Jigar(jam)
3. Gather all the required information first
   - Always check that you have all the information before beginning a ticket
   - If something is missing, gather everything first before starting your investigation
     - Ex:  code, clarification, more detailed information, etc.
     - You can block the ticket(kanban state red) if something is missing/blocking you from continuing

## Mandatory Items

1. Each task must have Sale Order Line, Parent Task, and Subscription fields set on the tab “Extra Info”. 
   - The Sale Order Line is the most important, without that we are not billing the customer.
2. The Process Leader will review and ask the consultant/ticket creator to fill out the information but please double check your ticket in case. 


## Stages

#### Requirements (PSUS)
1. The Customer’s Consultant will create the ticket here
   - Ideally by copying this [template](https://www.odoo.com/web?#id=2170477&action=333&active_id=1415&model=project.task&view_type=form&cids=3&menu_id=4720):
2. The consultant will fill out Sale Order Line, Parent Task, and Subscription fields
3. The consultant will also add Customer’s production URL
4. The consultant will add question(s) which the customer has given them. 
5. As well as any related code/images/attachments that are relevant. 

#### Development (PSUS)
1. Once assigned, you can move the task here during investigation/planning.
2. Log all your time spent here before moving to the next stage. 

#### UAT (PSUS)
1. A stage for customer feedback. 
2. If there is no response after one week. Tasks can be moved to Done Stage. 

#### Done (PSUS)
1. All completed tasks. 
2. The ticket can be moved back to the Development stage ONLY IF the follow up from the consultant/customer is related to the original request. 
3. If the request is New, please instruct the consultant to create a new ticket with the question(s). 
4. This ticket can be taken by the same developer or left in the queue if the developer is busy with other work. 

#### Canceled (PSUS)
1. Any task that is canceled by the customer or consultant. 
2. Task can be moved back to Requirements/Development if the customer wants/approves the task again to be worked on. 
   - Must be originally canceled by the customer/consultant 
   - If canceled by the process leader, please speak to them first.

## Paid Technical Support
### Technical Support Content
#### Technical support covers 
1. Technical paid (success pack hours) support for partners/customers.
2. Code Review, answering specific development-related questions (technical only). 
3. Help expedite the resolution of technical bugs in developments or bad data-related issues.

#### Technical support does not cover
1. Functional advice: this is still the role of a functional consultant and if a customer seeks functional advice during a technical support session, it will be delegated to the respective functional consultant.
2. Technical Training: Support can not be used to do any kind of technical training sessions, we have quarterly technical training for this.
3. Live Coding sessions: Does not cover coding on the spot with the customer, where a customer requests what they want and expects the developer to make it happen. Such a case would be a new development request. This also includes live bug fixing. 

### Kanban View

#### Requirements Stage

##### Kanban Card Colors:
1. <span style="color:yellow">Yellow</span>.
   - Regular Technical Ticket Request
2. Blue
   - Priority Technical Ticket Request
     - Either approaching Lead Time
     - or Blocking customer/Urgent
3. Purple
   - Change Request Ticket Request

##### States:
1. Green
   - Ready for Assignment
2. Grey
   - Unapproved/reviewed by Process Leader
   - Still can be assigned/taken but a note may be missing info
3. Red
   - Blocked for any reason that stops the task from moving forward 
   - Ex: Customers not responding, need more information, etc. 

##### Tags:
1. PS Support
   - General tag for ps support
2. Technical Call
   - Tag for a technical call
3. Technical Email
   - Tag for technical emails
4. Spanish
   - Tag for Spanish Speaking Requests
   - (Process Leader will try to add if the consultant did not already)
5. Change Request
   - Tag for any change requests to existing development

Note: If the ticket is not created by duplicating the templates, tags may not be accurate or even on the task. 

Feel free to add any other tags or remove them if they do not apply to the ticket. Tags are generally just for visual bookkeeping and organization. 

### Assignment
#### Picking Tasks
1. Any task can be assigned to yourself. 
2. With the exception of Spanish speaking Calls/Email requests.
3. The oldest or urgent request must be picked first.
   - These are usually the Blue Kanban Cards.
4. The Process Leader may ask the team to prioritize tasks that are either urgent or have been waiting in the Requirements Stage for a long time.
   - If they are not taken they will be assigned based on work load if it reaches the lead time deadline. 

## General Technical Support Tips
1. Start with generic advice(unless a question is very specific)
   - Give general documentation first if a question is vague
2. Gage customer’s technical level
   - If they say they are “technical” are they “I know some CSS/HTML” or “Hardcore python developer, already familiar with Odoo framework”?
   - A good way to check if they know how to use something:
     - Example: Does the customer know how to use GitHub?
     - Okay: “Do you know how to use GitHub?”
     - Better: “Are you familiar with Github or any version control?”
     - Note: Above can be substituted with any other technical topic besides GitHub (python, odoo modules, javascript, SH)
   - Customer’s technical level will give you an idea on how to handle the call/email
4. Tailor the call/email to the customer’s level of experience
5. Ask clarifying questions
   - “What do you mean by _____?” 
   - “Can you explain what _____ means in relation to _____?
   - “Why do you want to do things in a specific way only”
6. Give a clear explanation of why they should do something
   - Example: 
     - Okay: Using External API is better than direct SQL and bypassing the ORM layer.
     - Better: Using External API is better than direct SQL because ORM handles most of the logic, can prevent errors and guarantee persistent data.  
7. Most of the time it's better to assume the customer does not know anything about the topic and treat them as the first-grader
   - It's better to start off generally then focus down once the customer expresses interest in something. 
   - Example: 
     - Customer: “I want help with SH?”
     - Tech: “How are you planning to use SH? What specifically about SH? Have you seen the documentation on SH?”
     - Customer: “Yes, I’ve read some documentation. I want to know how to push code to SH”
     - Tech: “Okay, first ………..”

#### Professionalism
As part of the Professional Services Team, often you will be dealing with customers directly either through email or a call. We want to maintain a professional appearance to the customer. 

This can mean:
1. Greeting the customer via their Company or Name
2. Using professional business language
3. Knowing whom to direct the customer to if their question does not relate to your technical expertise
4. Adding pleasantries such as, “Have a nice day” or “Thank you for your patience”
5. Make Meaningful Small Talk, that helps in starting the conversion in a nice way.
6. Etc.
Friendly talk is perfectly fine to engage in. Just be mindful of your topics and conversations. 

#### Dealing with Difficult Customers
It is NOT acceptable if the customer is being unprofessional on their end. 

This may include:
1. Talking down to you
2. Yelling
3. Inappropriate behaviors
4. Anything unacceptable in an office environment
5. Etc.
 
Please notify the Process Leader, Jigar(jam), or their Consultant as soon as you notice any negative behaviors. If there are also any disagreements please let us know. Even if it is a small issue, we want to make sure you are being treated with respect. 
We will raise the issue with the Account Manager/Sales Person to correctly set expectations with the customer. 

#### Call vs Email Format
If it’s not specified when should we do a Call vs Email?

Generally, an Email is good enough most of the time. 

Note that any topic usually can be either a Call or an Email. Sometimes it makes more sense to choose one over the other, but if the customer requests a specific format we try to accommodate that. 

However, if they are insisting on one format but you believe the other is better, you can always suggest that to the Consultant/Customer. But please make sure to give reasoning on why that is the better/preferred format. (Ex: “This topic on Performance/Setup is too hard to do in an email, it is better to explain through a call to see what the customer is trying to do.”)

Here are some topics that may suit one format over the other. (Remember either format is perfectly fine for any topic).

##### Example Topics for Emails:
1. Documentation or reading heavy topics
   - Ex: Navigating Odoo source code
2. Sample code/scripts
3. Very specific question
   - Ex: “I’m looking for more information on how this MRP process works in relation to ______ in the source code.”
4. Error/Debugging help
   - Ex: “My code does not work here and gives this error, how do I fix this or how should I go about fixing this?”

##### Example Topics for Calls:
1. Setting up SH, how to do development in SH
2. General advice for server setup
   - Note: we do not help the customer set up their server live, but we will give advice and information on best practices. 
3. Best practice on doing Odoo Development
4. Best practice on doing Odoo code migration
5. How to use Odoo’s External API


## Technical Calls

### Before Call
1. The consultant will have already added questions or information to be discussed during the call. 
2. Please ask the consultant for more information if the question is unclear.
3. It is Okay to have a call to gather information and follow up with either email or another call to answer the question(s).
4. Prepare general answers/documentation for the call. 
   - It might be helpful to create a google doc with questions/answers. 
   - Example: 
     - Question: Where do I find source code on SH?
     - Answer: 
     - https://www.odoo.com/documentation/user/13.0/odoo_sh/getting_started/online-editor.html#edit-the-source-code
     - Explain directory structure
     - Home > odoo > src > odoo
     - Home > odoo > src > enterprise
5. Research anything you are unsure of before the call
6. Ask the team/Jigar(jam) if there is anything you are not 100% sure on
   - It’s better to be over-prepared than under-prepared
   - A teammate may already have knowledge on that specific subject and can give other resources
   - Reference the Experts [list](https://docs.google.com/document/d/1PC2rheRFdAxVJ2PGq3uae7zBdjkqaM46wyePuR8SOIQ/edit#heading=h.nntllakza0uj) for teammates knowledgeable on specific topics
7. Schedule the call through the Consultant by either giving:
   - Certain day/time slots (ex: Wed or Thursday Next week at 11 am PDT)
   - Link to your Google calendar
8. Have the consultant send the google invite which will have the Google Hangout link to use
9. Do not book more than one call per Day
10. Give ample time to do research/prepare beforehand when scheduling the call

### During Call
1. Join the Hangout link a little before the time. (ex: Join five min or so before the scheduled time)
2. Check with the Customer to make sure everyone on their side is present before starting.
3. Introduce yourself and the team
   - Ex: “Hello, my name is ____ and I’m on the technical team at Odoo SF.”
4. See what the customer wants to talk about first. Let them explain their company/situation.
5. You don’t need to be nervous. Having more experience will give you more confidence. 
6. It's okay to not know the answer to something. Note down the question and mention you will follow up either by an email or another call if there is enough to warrant a call. 
7. Calls typically last an hour. 
   - They may be shorter. 
   - If they need to go longer and your schedule allows for it, you may continue the call. 
   - However, you can stop the call at an hour since that is the given time allocated. 

8. What if the Customer does not show up?
   - Wait 15 minutes to see if the Customer shows up or not
   - Contact the Consultant either on the task via ping or through chat to see if they know where the customer is. 
   - If the customer does not show up after 15 min.
     - Let the Consultant know the situation and how long you waited. 
     - Ask if the Customer wants to reschedule the call. 
   - Log the time you waited for the customer to show up. 

### After Call
1. Write a brief summary and send a follow-up email.
   - Check with the consultant the best email to follow up with the customer is. 
   - Add them as a follower(more on this in the Technical Email section below).
2. If there were additional questions asked that need more research, plan when you will do the research and get back to the customer. 
   - This may be in a second call if the topic is large.
   - Or a simple email if the topic is small.
3. Let the consultant know how the call went if there was anything they need to do on their end.
4. Set Activity to follow up on the ticket
   - Usually, a week is a good gap
5. If there is no response from the Customer or the Consultant, the ticket can be moved to the Done stage
   - Log a note there was no follow-up response
6. Do timesheet for the call

## Technical Emails

### Before Email
1. Take your time to do research/code reading to understand the problem and answer the question thoroughly. 
2. Ask the Consultant what is the best email to reach the Customer. 
   - Add this email as a follower to the task. 
3. Write the sample code
   - See the Sample Code section for more details

### During Email
1. Write out an email that directly answers the customer’s questions
2. Use examples
3. Link to specific documentation
   - Ex: https://www.odoo.com/documentation/13.0/howtos/backend.html#inheritance
4. Link to specific snippets of odoo source code in GitHub
   - Ex: https://github.com/odoo/odoo/blob/13.0/addons/sale/models/sale.py#L774
   - This is highly effective to give the customer a concrete example
   - Also lets them explore around that code snippet in source code
   - Will encourage the customer to do code reading/research
5. The “Why” they should do something is just as important as the “How”
6. Explain any Sample code that was written
7. Send the Email through the “Send Message” button on the Task Chatter. 
   - Please do not send it through your odoo Gmail account directly.  
   - We want to avoid the Customer having direct contact with you. 
     - Always direct them back to the Consultant if they email you directly. 
   - This is also for tracking purposes 
   - If there are any issues, it's good to easily access the email thread. 
8. You can also ping the Consultant and have them pass the response to the customer
   - This just takes longer as they become a middle man
   - Whereas responding directly through Message in the ticket will give the customer a way to communicate directly
9. Practice Professional Email writing
   - See Section below for more information

### After Email
1. Set Activity to follow up on the ticket
   - A week is a good gap for Emails as well
2. If there is no response from the Customer or the Consultant, the ticket can be moved to the Done stage
   - Log a note there was no follow-up response

### Sample Code
1. Sample code is a generic code/script that can help give the customer a guide on how to achieve something.
2. What is the difference between Sample Code and Development?
   - Customer: I want a scheduled action that does X, and Y on the specific Model Z. 
   - Development: 
     - Coding to the specific requirement
     - Giving the customer the exact scheduled action that does X, and Y on the specific Model Z. 
   - Sample: 
     - Giving a generic sample of how to achieve X and Y, maybe on Model A instead of Model Z.
     - Only doing very basic code
     - Does not go into very detailed specifics
   - If the customer has further questions, we can answer them but will not provide the complete code
3. Sample API Script Example:
   - Emmie(ehe) created a [sample script](https://www.odoo.com/web#id=2178898&action=333&active_id=1415&model=project.task&view_type=form&cids=&menu_id=4720) for the customer. 
   - Check her attached python file for an example
4. Note: We will not take responsibility for the code the customer writes based on the samples
   - If they break something or it doesn’t work, we can try debugging but that will consume more pack hours. 

### Professional Email Writing
1. As part of the Professional Services Team, we want to maintain a professional image and etiquette in our emails
2. Start with a greeting to the customer
   - Ex: “Hello _____,” or “Dear _____,”
3. Keep the body of the email neat. 
   - Use multiple paragraphs to break up a large block of text
   - This is easier to read most of the time
4. Use an outline format if there are a lot of links
5. Use numerical or dot bullet points to clearly list points or further questions
6. Do not use slang, emotes, or abbreviations
   - Ex: “lol” or  “:)”
   - This is however fine to use in chatter log notes with colleagues
8. Add pleasantries
   - Ex: “Have a good day” or “Thank you for your time”
9. Use a sign off
   - Ex: “Sincerely,” or “Regards,”
10. Double-check your Signature for your account
    - If everything is set up correctly you won’t need to add your name at the end of the email. 

## Timesheet
### What do I timesheet?
1. Any time spent on the related PSUS Tech ticket should be time sheeted.
2. This includes:
   - Research before call
   - Sample Code writing
   - Call with customer
   - Email writing
   - Long form meeting with Consultant (if ticket needed it)
   - Follow up emails/research

### How much do I timesheet?
1. There is no exact amount of time you need/should spend on one of the items listed above
2. If you are newer to the team, you can log extra hours you spend learning under PSUS - Misc. with the task R&D / Self Learning
3. Use your best judgment on what is research vs your own learning.




