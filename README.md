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
        - [Arquitecture](#Arquitecture)
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
        - [Database](#Database)

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

### Arquitecture

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
- Algorithm 1

### Actors
The UA Information System holds photos from students', professors', investigators' and administration workers' faces, and as such these are our actors 
- Employees
- Human Resources Representatives

### Diagrams
![alt text](Simple_Organizations/UseCase.png)

### Database
- Database
