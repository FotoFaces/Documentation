# FotoFaces - Documentation
This repository was created to help organize all the documentation made by the Fotofaces Project.

# Development Team
- [Filipe Gonçalves - 98083](https://github.com/FlipGoncalves)
- [Pedro Lopes - 97827](https://github.com/Pedro-Lopes-Frisson)
- [Goncalo Machado - 98359](https://github.com/goncalo-machado)
- [Vicente Costa - 98515](https://github.com/SrPhoenix)
- [João Borges - 98155](https://github.com/JoaoBorgesUA)

# Index
- [FotoFaces - Documentation](#FotoFaces---Documentation)

    - [Inception Phase](#Inception-Phase)
        - [Context](#Context)
        - [Problem](#Problem)
        - [Goals](#Goals)
        - [Risks](#Risks)
        - [Expected Results](#Expected-Results)
        - [Related Work](#Related-Work)
        - [Architecture](#Architecture)
        - [Roles](#Roles)
        - [Tasks](#Tasks)
        - [Communication Plan](#Communication-Plan)
        - [Development Tools](#Development-Tools)
        - [Project Calendar](#Project-Calendar)
            - [Milestone 1](#Milestone-1)
            - [Milestone 2](#Milestone-2)
            - [Milestone 3](#Milestone-3)
            - [Milestone 4](#Milestone-4)

    - [Elaboration Phase](#Elaboration-Phase)
        - [Requirements](#Requirements)
            - [Non-Functional](#Non-Functional)
            - [Functional](#Functional)
                - [Mobile App](#Mobile-App)
                - [FotoFaces](#FotoFaces)
                - [FotoFaces Algorithms](#FotoFaces-Algorithms)
        - [Actors](#Actors)
        - [Diagrams](#Diagrams)
            - [Deployment Diagram](#Deployment-Diagram)
            - [Domain Model](#Domain-Model)
            - [Architecture](#Architecture)
        - [Other Organizations](#Other-Organizations)
            - [Use Case](#Use-Case)
            - [Database](#Database)
        - [State of Art](#State-of-Art)

    - [Construction Phase](#Construction-Phase)
        - [API](#API)
        - [Mobile Applicaion](#Mobile-Applicaion)
            - [Design](#Design)
            - [Photos](#Photos)
            - [API connection](#API-connection)
        - [FotoFaces](#FotoFaces)
            - [Plugin Architecture](#Plugin-Architecture)
            - [API connection](#API-connection)
        - [FotoFaces Algorithms](#FotoFaces-Algorithms)
            - [Face Recognition](#Face-Recognition)
            - [Face Comparison](#Face-Comparison)


## Inception Phase

### Context
The University has a system for updating photos.
Our project resides in identifying people in them and adjusting those photos in order to have a high quality and an easy association between a person’s name and their face.
We strive to invalidate photos which do not respect some standards: wearing glasses, using a hat, tilted head, etc. .

### Problem
- Send photo to an API
- It will respond with the characteristics of the photo
- The app will check if the characteristics are valid
- Updates the photo to the database

### Goals
- Facial Recognition
- Fix face orientation
- Analyse photo quality
- Blur background
- Recognize invalid objects, such as hats and sunglasses
- Crop face accordingly
- Implement deep learning

### Risks
- Modularization Problems
- Performance and Efficiency of the algorithms
- Bad implementation of deep learning
- Biased or insufficient training set

### Expected Results
- Fully functional mobile app with FotoFaces integration
- Reliable Facial Recognition
- Robust backend capable of scaling

### Related Work
- https://github.com/hamzasafdar01/Image-Blur-detection-and-image-quality-check-python
- https://www.pyimagesearch.com/2015/09/07/blur-detection-with-opencv/
- https://github.com/WillBrennan/BlurDetection2
- http://scikit-image.org/docs/dev/api/skimage.exposure.html
- https://github.com/AndreasMerentitis/detect-contrast-blurriness
- https://github.com/TianxingWu/realtime-glasses-detection
- https://pyimagesearch.com/2019/03/11/liveness-detection-with-opencv/

### Architecture

### Roles
| Filipe | Gonçalo | João | Pedro | Vicente |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Team Manager | DevOps | Lead Developer | Quality Manager | Architect |
| Communications | Backend | Frontend | Backend | Infrastructure |

### Tasks
| Filipe | Gonçalo | João | Pedro | Vicente |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Organise the team and generate backlog | Operate and do maintenance for the project repository | Design the aesthetic of the project | Manage software quality among all algorithms | Design the Architecture of the project |
| Integrate communication service with the backend and frontend | Integrate with the communications logic | Create the required communication services with the backend | Develop the API and its endpoints | Maintain and upgrade the infrastructure when needed |

### Communication Plan
- Discord for team discussion and communication
- Outlook for advisor-team discussion relationship
- GitHub Project for backlog management
- Promotional Website for organisation and advertisement
- File maintaining architectural choices and most asked questions

### Development Tools
- GitHub for code repository
- React for website builder
- React Native for mobile app builder
- Discord for team communication

### Project Calendar
In each iteration the documentation should be updated

#### Milestone 1
- Create a project calendar
- Set up code repositories
- Define the system architecture
- Build a draft for the website

#### Milestone 2
- Validate the architecture
- Simple Project Development
- Research technologies
- Improve the promotional website

#### Milestone 3
- Build the API
- Rebuild old algorithms
- Add new algorithms
- Start the build of the mobile app

#### Milestone 4
- Finish the mobile app
- Add new algorithms





## Elaboration Phase

### Requirements

#### Non-Functional
- Scalability - When many users use the API at the same time
- Reliability - It shouldn’t crash all the time 
- Availability - Always available to any user 
- Maintainability - Maintain documentation and infrastructure 
- Usability - Intuitive application

#### Functional

##### Mobile App
- The system must allow the user to login with username and password (or SSO)
- The system must allow the user to check his current photo
- The system must allow the user to check the properties needed for a photo to be valid
- The system must allow the user to pick between taking a live photo or choosing a photo from the gallery and do one of them
- The system must allow the user to choose between updating a valid photo, going back to the last menu or return to the main page
- The system must send a photo and the user ID to the FotoFaces API 
- The system must receive a JSON from the FotoFaces API with the validation properties
- The system must check the validity of a photo (based on its properties)
- The system must show the user if the chosen photo is valid

##### FotoFaces
- The system must be able to receive a photo and an user ID
- The system must get the user old photo from the database
- The system must compare the photos and check if it’s the same person
- The system must detect a series of properties from the new photo
- The system must send the detected properties in a JSON format to the user
- The system must allow for plugins to be added for detection of more properties

##### FotoFaces Algorithms
- Facial Recognition
- Face Reference Detected
- Face Orientation
- Frontal Face
- Analyse photo quality
- Analyse photo brightness
- Analyse colored Picture
- Blur background
- Resize
- Cropping
- EyesOpen
- Gaze
- Hat
- Glasses
- Sunglasses
- Implement deep learning

##### FotoFaces Properties
Returns True or False for the following:
- Face Recognized
- Matches old photo
- Frontal Face
- Eyes Open
- Hat
- Glasses
- Sunglasses
- Blurred
- Colored
- Cropped
- Liveliness

Returns Levels for the following:
- Brightness
- Quality

### Actors
The UA Information System holds photos from students', professors', investigators' and administration workers' faces, and as such these are our actors 
- Employees
- Human Resources Representatives

### Diagrams
All diagrams are in the Images/Architecture_Diagrams folder

#### Deployment Diagram
![Deployment Diagram](https://github.com/FotoFaces/Documentation/blob/main/Images/Architecure_Diagrams/DeploymentModel.png)

#### Domain Model
![Domain Model](https://github.com/FotoFaces/Documentation/blob/main/Images/Architecure_Diagrams/DomainModel.png)

#### Architecture
![Simple Architecture](https://github.com/FotoFaces/Documentation/blob/main/Images/Architecure_Diagrams/Simple_Architecture.png)

### Other Organizations
All images  are in the Images/Simple_Organizations folder

#### Use Case
![Use Case](https://github.com/FotoFaces/Documentation/blob/main/Images/Simple_Organizations/UseCase.png)

#### Database
![Database](https://github.com/FotoFaces/Documentation/blob/main/Images/Simple_Organizations/db.png)
Currently the database that is being used by FotoFaces belongs to the UA and we don’t have full access for testing purposes.
To solve this, we will create a mock database that simulates the UA database.

### State of Art
- [Face Recognition](https://www.luxand.com/facesdk/?utm_source=google&utm_medium=cpc&utm_campaign=face-detection)
- [Blurred](https://github.com/hamzasafdar01/Image-Blur-detection-and-image-quality-check-python)
- [Cropped](https://github.com/davisking/dlib/blob/master/python_examples/face_alignment.py)
- [Liveliness](https://pyimagesearch.com/2019/03/11/liveness-detection-with-opencv/)
- [Eyes Open](https://github.com/Chris10M/open-eye-detector)
- [Frontal Profile](https://github.com/juan-csv/profile_detection)
- [Glasses](https://github.com/TianxingWu/realtime-glasses-detection)
- [Quality](https://sightengine.com/docs/image-quality-detection)
- [id.ua.pt](https://id.ua.pt/) already offers services to UA, which includes similar software with the one we are going to build





## Construction Phase

### Database API
REST API with four endpoints, two for each object.
The endpoints are mapped to the ip:8393/user/-parameters- or ip:8393/image/-parameters-, depending on the type of the object

#### Image
- GET
    - fetches the image from the database, for the user with a specific id; returns a json with the type of command ("get_photo"), the photo and the identification
- PUT
    - updates the photo in the database, for the user with a specific id; returns a json with the type ("upload_photo"), the photo and the identification

#### User
- GET
    - fetches the user from the database, for the user with a the requested email; returns a json with the type of command ("get_user") and state (error or success)
- PUT
    - inserts the user in the database, with his photo, hashed password, username and email; returns a json with the type of command ("create_user") and state (error or success)

### Mobile Application 
The Mobile application was made with react-native, using firstly a template for the design and later with a hand-made style.
It has 8 screens, from LoginScreen and RegisterScreen, to PhotoAccept and MainScreen. Each one of them, represent a step to complete the update of the photo.
It also has some photo parameters, in which the taken photo needs to be pass to be validated to be presented to the FotoFaces algorithm, whenever a photo is taken, either in MainScreen and RegisterScreen.

#### Screens
Below, its listed the most important screens used in the application, and what exactly each one of them do.

- StartScreen
    - Screen in which the application starts
    - Prompts the user to select either login in the app or register an account

- LoginScreen
    - Screen in which the user logins in the application
    - Prompts the user to enter their email and password, or use the login via SSO
    - Can be used to go to the RegisterScreen, if the user does not have an account already
    - Can be used to go to the ResetPasswordScreen, if the user does not remember their password

- RegisterScreen
    - Screen in which the user will create an account in our applciation
    - Prompts the user to enter their email, a username, password and a photo, from which he can choose to take a new one or select from the gallery of his phone

- ResetPasswordScreen
    - Screen in which the user will try and recuperate its account
    - ^^^^^^^^^^^^^^^^^^^^^^^^^^^
    - ^^^^^^^^^^^^^^^^^^^^^^^^^^^
    - ^^^^^^^^^^^^^^^^^^^^^^^^^^^
    - ^^^^^^^^^^^^^^^^^^^^^^^^^^^
    - ^^^^^^^^^^^^^^^^^^^^^^^^^^^ 

- MainScreen
    - Screen in which the user can see some of their personal information and update their photo
    - Prompts the user to select between choosing a photo from his gallery or take a new live photo 
    - After a photo is sleected, the user can validate it in the FotoFaces algorithms, and, in case of invalidation, see what went wrong
    - If the photo is valid, he will be redirected to the PhotoAccept screen

- PhotoAccept
    - Screen in which the user can choose to update its photo with the new one or not
    - Prompts the user with both old and new photo and asks the user if he will update or not
    - If he updates, then he will be redirected to the StartScreen, else he will be redirected back to the MainScreen

#### Design
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#### API connection
The connection between both the Database API and Mobile App, and Mobile App and FotoFaces is made using the function fetch() with FormData to encrypt the body.

### FotoFaces

#### Plugin Architecture

#### API connection
The connection between Database API and FotoFaces is not existing, because the old photo is sent directly from the Mobile App, meaning that the FotoFaces is completely independent to the Database.

### FotoFaces Algorithms
All the algortihms used, will be presented and analyzed here, in the section below.


#### Face Detection
- Converts the image to gray scale
- Uses the dlib face detector to get all possible match in a dlib rectangle
- Verifies if each rectangle is a good result (not None or all the rectangle is in the photo)
- Converts the dlib rectangles to an array in opencv format (x y width height)  (function rect_to_bb)
- Calculates the area of the rectangles (function bb_area)
- Chooses the one with the biggest area
- Uses dlib face predictor with the 68 facial landmarks to detect each part of the face  (raw_shape) 
- Converts the face raw_shape to numpy format (shape) (function shape_to_np)
- Returns the shape, rectangle in opencv format and the raw shape  
- This algorithm is the same implemented in the old fotoface

![68 facial landmarks](https://github.com/FotoFaces/Documentation/blob/main/Images/algorithms/68-facial-landmarks.jpg)

<p align = "center">
<b>dlib face predictor 68 facial landmarks</b>
</p>


#### Brightness
- The Brightness plugin uses the Cropping function to cut the face of the person in the photo with a more tight result so the background captured is the small possible
- Then it converts the image color from bgr (Blue Green Red) to hsv (hue saturation value) and separate in its components
- Finally to calculate the brightness of the person face it calculates the mean value of the third component, the value.

#### Rotate


#### Cropping
- This function is used to cut a photo in a format defined as an argument (crop_alpha).
- It calculates the best location in the image due to the argument shape
- This algorithm is the same implemented in the old fotoface

#### Open Eyes
- This plugin uses the argument shape to calculate the distance between the eyelash using the landmarks 37 to 42 (left eye) and 43 48 (right eye)
- Then ir return the average of this two distances
- This algorithm is the same implemented in the old fotoface

#### Face Recognition
- Uses the face detection function on the reference image to get the reference raw_shape 
- Get the dlib get face chip function to get the reference and candidate face as a numpy array 
- Uses the dlib face recognition model v1 to convert each face into 128D vectors (This function is a machine learning algorithm that maps human faces into a vectors where the pictures of the same person are mapped near to each other and different people are mapped far apart).
- Returns the norm of the difference of both matrices 

#### Glasses

#### Head Position
 
- Use the opencv fucntion solvePnP to estimate the orientation of the face 
- converts the rotation vector to rotation matrix using opencv function rodrigues 
- Stacks concatenate the rotation matrix with the translation vector (column wise) to get a projection matrix
- Decomposes the  projection matrix using opencv to euler Angles
- Seperate the euler angles to its components (pitch yaw and roll)
- Convert this components from radians to degrees 
- Returns an array with the pitch roll yaw metrics of the face
- This algorithm is the same implemented in the old fotoface

#### Image Quality
- converts the image from bgr to gray scale
- calculate the BRISQUE score using the opencv function QualityBRISQUE_compute with the brisque model and the brisque range yml files
- This algorithm is the same implemented in the old fotoface

#### Sunglasses

#### Focus / Gaze


- gets the values fo the landmarks of the left eye (37/38 and 40/41)
- gets the image eye filtering by the landmarks
- converts the eye to gray scale
- uses opencv Bilateral filter to blur the eye without damaging the edges (eyelash)
- uses opencv erode function to apply erosion (just like soil erosion) on the edges of the eye
- uses opencv threshold function to convert the eye to black and white image, by converting all pixels above the threshold to white and to black otherwise. It choose the optimal threshold with the otsu algorithm
- https://docs.opencv.org/4.x/d4/d73/tutorial_py_contours_begin.html


- Does the same for the right eye
- returns the average of both ratio if has result for both eyes or just the one that has result 
- This algorithm is the same implemented in the old fotoface



