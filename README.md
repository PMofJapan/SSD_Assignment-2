## SSD Assignment 2
Weekly assignment
(due date: 22 February 2022, 23:59)
• Create github account for this assignment
• Develop API for a machine learning model and store it
to your github account
• You may use this reference:
https://towardsdatascience.com/deploying-amachine-learning-model-as-a-rest-api-4a03b865c166
• Share your github link to email lukmanh@ugm.ac.id
• Email is sent with subject:
Name of student_assignment2_SSD_CSIUP 


## Procedure
1. Install requirements
3. Build sentiment classifier
4. Write `app.py` which is the API application that will be deployed
5. Update requirements.txt as you write the code
6. Test the API


## File Structure
* app_name
  * app.py: Flask API application
  * model.py: class object for classifier
  * build_model.py: imports the class object from `model.py` and initiates a new model, trains the model, and pickle
  * util.py: helper functions for `model.py`
  * requirements.txt: list of packages that the app will import
  * lib
      * data: directory that contains the data files from Kaggle
      * models: directory that contains the pickled model files


## Testing the API
1. Run the Flask API locally for testing. Go to directory with `app.py`.

```bash
python app.py
```


2. In a new terminal window, use HTTPie to make a GET request at the URL of the API.

```bash
curl -X POST -F 'query=something' http://localhost:5000
```


3. Example of successful output.

```bash
HTTP/1.0 200 OK
Content-Length: 57
Content-Type: application/json
Date: Tue, 21 Aug 2018 19:04:04 GMT
Server: Werkzeug/0.14.1 Python/3.6.3

{
    "confidence": 0.78,
    "prediction": "Positive"
}
```
