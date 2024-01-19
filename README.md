# Building a Chatbot to order a Pizza using Amazon Lex

# Goal

My goal was to build a sample chatbot with automated text and voice which can be used to build an order for a pizza place in our case without the need of any human interaction.
This template can be used for building complex bots for other purposes depending on the use case of the business helping in decreasing the need for human interaction.
Amazon Lex has pre-buil integration with AWS services which can be configured according to the business requirement and use case.

## What is Amazon Lex? 

Amazon Lex is an AWS service for building conversational interfaces for applications using voice
and text. With Amazon Lex, the same conversational engine that powers Amazon Alexa is now
available to any developer, enabling you to build sophisticated, natural language chatbots into
your new and existing applications. Amazon Lex provides the deep functionality and flexibility
of natural language understanding (NLU) and automatic speech recognition (ASR) so you can
build highly engaging user experiences with lifelike, conversational interactions, and create new
categories of products.


## Terminology used within Amazon Lex

1. Intent -  An intent represents an action that the user wants to perform. You create a bot to
support one or more related intents. For example, we are creating an intent that orders pizzas
and drinks.

2. Utterances - Spoken or typed phrases that invove our intent.

3. Slots -  Slots are the input data required to fullfill the intent.

4. Fullfillment - Fullfillment mechnist for our intent


## Process of building a Chatbot to order a Pizza

This is conversational bot to order food and drinks from Ankur's Pizza, Either using keyboard for our input or our voice.

1. Log in to AWS console and navigate to Amazon Lex.

2. Click on Create bot and give select the type of bot giving it a name and description.

   ![Screenshot 2024-01-18 161427](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/78674511-862e-4d82-891e-fd56dff78368)

3. Create an IAM role with basic Amazon Lex permissions.

4. select COPPA as no and leave other things as default and click on next.

5. Select the language (English US in our case) and select the voice type. And click on done.

   ![image](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/a6f39eed-23db-4935-8a7f-b1dfd0e14bb6)


6. Create an Intent OrderPizza.

    ![Screenshot 2024-01-18 161934](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/96a15dc3-86cb-430f-9da6-fcc6ad17cc11)

7. Add few Utterences in order to make it more user friendly.
   
    ![Screenshot 2024-01-18 161952](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/bac8d14b-2e85-4512-8d0c-d4476f7bdba7)

9. Creatings slots, which is basically the data from user/customer will select their choices from.

10. Create a blank Slot type, PizzaType and give values as Italian, Mexican, Chicken. Click Save Slot after adding your choices.
  
    ![Screenshot 2024-01-18 162420](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/c95e43a9-abab-4936-a497-d39166ddf06a)

11. Create a blank Slot type, Crust and give values as thin, medium, thick, and lettuce. Click Save Slot after adding your choices.

    ![Screenshot 2024-01-18 162606](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/2a683675-3dd3-4a03-bb61-01c3228670a5)

12. Create a blank Slot type, for appetizers and values such as coke, cake , mousse, etc. Click save slot after adding your choice.

    ![Screenshot 2024-01-18 162739](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/705b889d-8ffb-406f-b46b-fab383904a76)

13. All the slots required have been created.

     ![image](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/90a2a5df-5612-47fe-b9af-5efeaba0a583)

14. Go back to intent for adding slots to our bot.

15. First slot we are going to add is Name which will be the name of the customer added by him/her. Click add slot give the title as name and select slot type as Amazon.Firstname which is built in.

     ![Screenshot 2024-01-18 162931](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/fe489d70-c642-4b64-a670-28597b88206e)

16. Next add a slot PizzaType and select the slot type that we created i.e. PizzaType. And give any prompt including the name of the customer.

    ![Screenshot 2024-01-18 163456](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/c79de8fc-a1c0-4175-88fc-91e4b1078b3b)

17. Next add a slot Crust and select the slot type that we created i.e. Crust. And give appropiate prompt.

     ![Screenshot 2024-01-18 163613](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/10f18a05-96ad-45cf-b9fd-71533b83c246)

18. Next add a slot Appetizer and select the slot type that we created i.e. Appetizer. And give appropiate prompt.

     ![image](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/cf45bc04-d191-4629-a4fa-12a4d51ad983)

19. Next add a slot for delivery time and name the slot as DeliveryTime and select prebuilt type as AMAZON.Time. And add a appropriate prompt.
  
    ![Screenshot 2024-01-18 164029](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/af90da3d-fb60-4091-8c82-051fdb2e3cdf)

20. Add confirmation prompts and closing response prompts in order to initiate and end the order in a more pleasent order.

    Confirmation Prompt
     ![image](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/525f665e-b770-4ba2-8ac6-a5bdbf2d337d)

    Closing Prompt
    ![image](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/11654197-137b-41fe-9cc7-cc3222fea5ac)

21. Adding more sample utterances in order to place the order in a single command/Text.
  
    ![image](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/6cca01d9-f036-45b4-8fb0-a007bbb5e975)

22. Setting the delivery time as selection for the users in order to make the delivery selection process easier.
    It can be done through Slot Prompts editor within the slot ands select prompts as buttons and adding our values in the slot values.
  
    ![image](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/79e88d64-a807-4f40-a2e6-38df71d1c72b)

23. Save the intent and click on Build.

     ![image](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/6649e368-fd0b-405f-b59a-b26e2f62b7c7)

24. Testing and debugging the bot.
  
    ![image](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/db197c54-e5ff-4941-b4f2-75dc0caa2150)
    ![image](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/e2fc737c-aa40-4892-94b7-0184ff7d8c8c)
    ![image](https://github.com/ankurcyb/AWS-Chatbot-Ordering-Pizza/assets/141453942/8bf4f11c-ed0d-4508-866e-ccef89d1969e)


## Conclusion

This Project showcases the abilities of Amazon Lex and through this template we can lead towards designing complex template which can be used for other business purposes such Banking, Hospitals, schools., etc. And we can easily integrate with AWS services to make things more seamless.
In future, this bot can also be integrated with ChatGPT or any other AI bot in order to make it more interactive through machine learning.

## Acknowledgement 

This project/lab is inspired by AWS official documents.

Link - https://docs.aws.amazon.com/pdfs/lexv2/latest/dg/lex2.0.pdf#how-it-works
