# EXPT-5-Speech-Recognition-using-Python

# AIM: 

# To perform and verify speech recognition using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
!pip install SpeechRecognition pydub

import speech_recognition as sr

# Path to your audio file
audio_file_path = '/content/shivani.wav'  # Change this to your file name if different

r = sr.Recognizer()

# Load the audio file
with sr.AudioFile(audio_file_path) as source:
    print("Reading audio file...")
    audio = r.record(source)  # read the entire audio file

    print("Attempting to recognize speech...")
    try:
        text = r.recognize_google(audio)
        print("Recognized Text:")
        print(text)
    except sr.UnknownValueError:
        print("Google Speech Recognition could not understand audio")
    except sr.RequestError as e:
        print(f"Could not request results from Google Speech Recognition service; {e}")
```

# OUTPUT: 
<img width="1600" height="313" alt="image" src="https://github.com/user-attachments/assets/352622e9-a8a3-4f77-b523-7cd3014caae7" />


# RESULT: 
Thus the speech recognition using SCILAB was performed and verified.
