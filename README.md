# cognito-quotient
CognitoQuotient is a React Native application that enables users to take a quiz, record their responses via video, and upload the video for analysis. The results are then displayed on a separate screen. The project includes a Python backend for handling video uploads and analysis.

The landscape of talent assessment has evolved significantly in response to the demands of today's competitive job market and the emergence of advanced technologies. In this context, a range of related work encompasses cutting-edge practices and methodologies aimed at enhancing the efficacy, fairness, and objectivity of talent assessment processes. From the utilization of psychometric assessments to the integration of AI-driven algorithms and predictive analytics, organizations are leveraging innovative tools to identify, evaluate, and select top-tier talent. Furthermore, ethical considerations play a crucial role in shaping the implementation and governance of these technologies, ensuring transparency, fairness, and compliance with privacy regulations.

Table of Contents
Installation
Usage
Project Structure
Components
APIs
Dependencies
Installation
To set up this project locally, follow these steps:

Frontend
Clone the repository:

git clone https://github.com/Pirates-of-The-Galaxy/CognitoQuotient.git
cd CognitoQuotient
Install dependencies:

npm install
Set up Expo CLI (if not already installed):

npm install -g expo-cli
Start the project:

expo start
Backend
Navigate to the backend directory:

cd backend
Set up a virtual environment:

python3 -m venv venv
source venv/bin/activate   # On Windows, use `venv\Scripts\activate`
Install dependencies:

pip install -r requirements.txt
Start the backend server:

python app.py
Usage
Home Screen: Choose options and navigate through different screens.
Quiz Screen: Take the quiz with the provided questions.
Recording Screen: Record your response via the camera.
Upload Screen: Upload the recorded video.
Result Screen: View the analysis results of your uploaded video.
Project Structure
Frontend
/src
  /assests
    /images
  /components
    Box_EQ.js
    Box.js
  /constants
    theme.js
  /data
    EQquizdata.js
    quizdata.js
  /screens
    Home.js
    Disc.js
    Option.js
    Quiz.js
    Tst.js
    Try.js
    Result.js
  App.js
  app.json
  package.json

Backend
/backend
  app.py
  requirements.txt
  AudioSenti.py
  StutterCheck.py
  .gitignore
Components
Result.js
Displays the results of the video analysis. It uses useRoute to get the passed data and useLayoutEffect to hide the header.

Try.js
Handles the quiz questions and video recording functionality. It requests camera and microphone permissions and provides buttons to start/stop recording.

FileUpload.js
Allows users to pick a video from the library and upload it to the server. After successful upload, it navigates to the Result screen with the response data.

APIs
POST /upload
Description: Uploads a video file for processing.
Request: Multipart form data with a key video containing the video file.
Response: JSON indicating success or failure.
Dependencies
Frontend
react-native
expo
@react-navigation/native
@react-navigation/native-stack
expo-camera
expo-media-library
axios
Backend
Flask
flask_cors
moviepy
nltk
speech_recognition
opencv-python
numpy
roboflow
