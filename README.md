# Landing
![Alt text](/images/resumeforge/landing.PNG)

The AI Resume Generator is a web application developed using Bubble.io. Using parameters given by an API request from Bubble, it generates data using an integrated Node.js API that interacts with OpenAI language models. This instruction will walk you through the application's primary features, such as how to log in, complete the form, and create a sample resume.

# Log in
![Alt text](/images/resumeforge/loginn.PNG)

Users will be forwarded to the login page when they access the application. There is only one method for logging in for now, and that is using GitHub authentication. The user will return to the landing page after logging in with their GitHub credentials.

# Form Submission
![Alt text](/images/resumeforge/click_submit.PNG)

Form Filling: After logging in, the user can start filling out the form. The form is intended to record the user's employment history, including the name of the employer, the position held, and the length of time. With the Bubble backend layer, the user's data is saved in a nearby database. The formData data type is used to store the data.

# Fetch Generated Data from External API
![Alt text](/images/resumeforge/after_submit.PNG)

Making the resume: The user may click the "See Resume" button after submitting the form. This action causes a post request to be sent to the [Node.js API](https://github.com/ChikangaTakudzwa/resumeforge), which then produces a response depending on the user-provided data. Goals, key points, and job responsibilities are all included in the response, which is kept as a response data type in the local database.

*form data table*
![Alt text](/images/resumeforge/formdata_table.PNG)

*api response data table*
![Alt text](/images/resumeforge/response_table.PNG)

# [Node.js API](https://github.com/ChikangaTakudzwa/resumeforge)
Node.js API: Based on the parameters given through the API static call, text is generated using the Node.js API in conjunction with OpenAI language models. The API is currently initialized using static data that was provided by the Bubble API connector. The answer must be a JSON object, like the server expects.
