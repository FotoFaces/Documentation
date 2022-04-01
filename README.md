# FotoFaces - Documentation
This repository was created to help organize all the documentation made by the Fotofaces Project.

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
                - [FotoFaces Algorithms](#Algorithms)
        - [Actors](#Actors)
        - [Use Case](#Use-Case)
        - [Database](#Database)

## Inception Phase

### Context
Being able to identify someone by their face is globally used in normal day life, but when we try and categorise people in a certain company, or enterprise, it is not always easy. Inserting a photo anywhere is not the main problem, but assuring that when updating it with a new photo, it’s valid and usable can get tricky. Therefore, the search for a way to upload new photos and validate it with new/better algorithms that prevent any backlash is highly requested.

### Problem
Our project will consist of a mobile application that sends a photo to an API which will respond with characteristics of that photo (Ex.: Has a face, has glasses…) and, according to the response message, the mobile app will check if it’s valid and update it to the database.

### Goals
- Facial Recognition functionalities
- Improve existing algorithms in FotoFaces
- Add algorithms to FotoFaces to improve the reliability of the Facial Recognition
- Implement deep learning to make the FotoFaces algorithms more reliable

### Risks
- Modularization Problems
- Performance and Efficiency of the algorithms
- Bad implementation of deep learning

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
| Team Manager | DevOps | FrontEnd & Quality Team | Quality Manager | Architect |

### Tasks
| Filipe | Gonçalo | João | Pedro | Vicente |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| Organise the team and generate backlog | Operate and do maintenance for the project repository | Design the aesthetic of the project | Manage software quality among all algorithms | Design the Architecture of the project |
| Maintain a good project documentation for posteriori | Make sure the project runs everywhere | Manage software quality among all algorithms | Organise the tasks for the Quality Team | Maintain and upgrade the architecture when needed |
| Developer | Developer | Developer | Developer | Developer |

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
- Professors
- Students

### Use Case
- Use Case

### Database
- Database