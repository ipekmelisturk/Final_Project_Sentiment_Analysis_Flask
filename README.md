# Final_Project_Sentiment_Analysis_Flask

# Practice_Project_Sentiment_Analysis_Flask
With IBM course's initiative I developed a Python web app using Flask and integrate an Emotion Detection system that processes feedback provided by the customer in text format and deciphers the associated emotion expressed.

##Tasks and objectives that has been accomplished:
- Task 1: Fork and Clone the project repository
- Task 2: Create an emotion detection application using Watson NLP library
- Task 3: Format the output of the application
- Task 4: Package the application
- Task 5: Run Unit tests on your application
- Task 6: Deploy as web application using Flask
- Task 7: Incorporate Error handling
- Task 8: Run static code analysis
After cloning the corresponding repo you need to ensure libraries and Python:
```
python3.11 -V
pip3.11 show requests flask pylint
python3.11 -m pip install requests flask pylint
```
After creating the sentiment analysis, the execution is tried using Python shell.
```
$python3.11
>>> from sentiment_analysis import sentiment_analyzer
>>> from emotion_detection import emotion_detector
>>> emotion_detector("I love this new technology")
{'anger': 0.0132405795, 'disgust': 0.0020517302, 'fear': 0.009090992, 'joy': 0.9699522, 'sadness': 0.054984167, 'dominant_emotion': 'joy'}
>>> import json
>>> from emotion_detection import emotion_detector
>>> response = sentiment_analyzer("I love this new technology")
>>> formatted_response = json.loads(response)
>>> print(formatted_response)

```
To exit the Python shell, type exit() or press Ctrl+Z.

As the next step, the output is formatted as JSON. 
```
>>> emotion_detector("I love this new technology")
{'anger': 0.0132405795, 'disgust': 0.0020517302, 'fear': 0.009090992, 'joy': 0.9699522, 'sadness': 0.054984167, 'dominant_emotion': 'joy'}
```

Package the application by creating an __init__.py file to reference the module.

Implemented a unittest using assertEqual and run the test.
```
$ python3.11 test_emotion_detection.py
----------------------------------------------------------------------
Ran 1 test in 0.682s
```
Make sure the directory is in this structure:
directory structure:
```
final_project/
├── EmotionDetector/
│   ├── __init__.py
│   ├── emotion_detection.py
├── templates/
│   ├── index.html
├── static/
│   ├── mywebscript.js
├── server.py
```
To deploy the application, execute the file server.py from the terminal.
```
python3.11 server.py
```
<img width="%20" height="%20" alt="6b_deployment_test" src="https://github.com/user-attachments/assets/be60ced1-bf38-4b6e-9526-f4709ff3609c" />

<img width="%20" height="%20" alt="7c_error_handling_interface" src="https://github.com/user-attachments/assets/eba9ea4b-f511-4163-bb57-d7b17b879e11" />

For static code analysis, you can try:
```
pylint server.py
```

<img width="700" height="154" alt="8b_static_code_analysis" src="https://github.com/user-attachments/assets/e341fb80-121d-445f-a0b2-3aceea51ae71" />


