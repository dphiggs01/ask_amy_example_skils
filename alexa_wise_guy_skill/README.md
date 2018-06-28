# The Alex Wise Guy Skill
This skill tells some pretty punny knock knock jokes

### This example skill demonstrates the following features:
* logging level setting (debug)
* custom intent
* Amazon intent
* use of slots
* conditional response
* stack dialog manager
* default intent handler
* voice response (ssml) with variable content
* provide a card title and card content creation


### Prerequisites
Before starting make sure you have satisfied the prerequisites.
https://dphiggs01.github.io/ask_amy/prerequisites.html

### Deployment

1. Update ``arn:aws:iam::**********:role/alexa_lambda_role`` in cli_config.json.
    *  ~~~
        $ vim cli_config.json
        ~~~
2. Deploy the code to AWS Lambda
    * Note: Initial deploy should use (create).
        ~~~
        $ ask-amy-cli create_lambda --deploy-json-file cli_config.json
      ~~~
    * Note: Subsequent deploys should use (deploy).
        ~~~
        $ ask-amy-cli deploy_lambda --deploy-json-file cli_config.json
        ~~~


3. Create a new skill in your Amazon Development Account.
    * Select the `JSON Editor` and Drag & drop the _interaction_model.json_ on to the new skill.
    Click `Save` and `Build Model`.
    * Select `Endpoint` copy the _Lambda arn_  _arn:aws:lambda:us-east-1:********_
    (Note: It was returned in step two above) to `Default Region` select `Save Endpoint`.
    * Test your new skill!

**"Congratulations you have deployed a new skill!"**

Note: If you want to check the lambda logs you can use the below
~~~
$ ask-amy-cli logs --log-group-name /aws/lambda/alexa_wise_guy_skill
~~~

###### Credit
Many of the example skills were first published as Java or Node.js code
by Amazon https://github.com/amzn. However since Amazon created the _new_
interaction model the original code is no longer available.


