# Problem Statement : EMERGENCY MEDICAL SERVICES

SCDF works closely with Community First Responders (CFRs) to provide timely relief and response to emergency situations. With the increasingly aging population and a growing segment of vulnerable populations in mind (e.g. increasing trend of elderly with no next of kin), how might we leverage analytics for better sense-making to be alerted at the onset of incidents which require emergency response (e.g. cardiac arrests, falls, unattended cooking fires etc.) and mobilise CFRs for effective early intervention especially to the vulnerable populations?

# Submission name

[![License](https://img.shields.io/badge/License-Apache2-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0) [![Slack](https://img.shields.io/badge/Join-Slack-blue)](https://callforcode.org/slack) [![Website](https://img.shields.io/badge/View-Website-blue)](https://code-and-response.github.io/Project-Sample/)


## Contents

1. [Short description](#short-description)
1. [Demo video](#demo-video)
1. [The architecture](#the-architecture)
1. [Long description](#long-description)
1. [Project roadmap](#project-roadmap)
1. [Getting started](#getting-started)
1. [Running the tests](#running-the-tests)
1. [Live demo](#live-demo)
1. [Built with](#built-with)
1. [Contributing](#contributing)
1. [Versioning](#versioning)
1. [Authors](#authors)
1. [License](#license)
1. [Acknowledgments](#acknowledgments)

## Short description

### What's the problem?

The main problem is that elderly may have health problems which go unnoticed when they do not have a caregiver to take care of their well being. Also, some elderly living alone may not be able to seek out assistance in times of emergency. In such instances, we seek to find an alternative to monitor the health condition of the elderly.

### How can technology help?

Voice-enabled chatbot and artificial intelligence is used to communicate with our elderly. Data Analysis on what the Elderly had been saying to the chatbot (Pattern Recognition) and Tone ‘Analysis to detect emotions to access the situation.


### The idea

Through the use of voice-enabled chatbot and artificial intelligence, we seek to communicate with the elderly in the absence of a human caretaker. The chatbot will be able to detect conditions such as dementia or a bad fall through communication and to act as a one-stop service for elderly seeking help.


## Demo video

[![Watch the video](https://github.com/Code-and-Response/Liquid-Prep/blob/master/images/IBM-interview-video-image.png)](https://youtu.be/vOgCOoy_Bx0)

## The architecture


### Voice enabled COVID-19 crisis communication chatbot using Node-RED

![Elderly Helper Architecture diagram](/images/Architecture_Graph.png)

1. User launches the voice-enabled Node-RED Elderly chatbot android app and App initiates a conversation. 
2. User replies.
3. Node-RED records the speech wav file and calls the Watson Speech to Text service hosted in IBM Cloud.
4. Watson Speech to Text uses machine learning to decode the user's speech.
5. (Optionally), Watson Language Translator translates speech into english.
6. (Optionally) Watson Tone Analyzer to detect user emotion to detect emergency, natural language understanding and historical data to analyse the condition and wellbeing of the user.
7. Watson Speech to Text replies with a transcript of the question and Node-RED calls Watson Assistant service hosted in IBM Cloud.
8. Watson Assistant uses natural language understanding and machine learning to extract entities and intents of the user's question using Natural Language Classifier.
9. Source (specific stuff here) FAQ information from trusted data like(give sources)
10. Watson Assistant invokes an OpenWhisk open source powered IBM Cloud Function.
11. IBM Cloud Function calls the Watson Discovery service running in IBM Cloud or other services to fulfil the user intent.
12. Watson Assistant invokes an OpenWhisk open source powered IBM Cloud Function.
13. IBM Cloud Function calls the Elderly chatbot to get statistics.
14. Watson Assistant replies to the user inquiry and Node-RED sends the text transcript to Watson Text to Speech.
15. (Optionally), Watson Language Translator translate the text object into the user’s native language
16. Watson Text to Speech encodes the message
17. Node-RED plays the chat answer .wav file to the user.
18. User listens to the chat answer
19. Chatbot waits for input from elderly by initiating further small talk and checks for responses from the user.


## Getting started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

1.An android phone with usb debugging and untrusted app installation permissions.

### Installing

A step by step series of examples that tell you how to get a development env running

1. Download the .apk [here.](url)
2. Install and try it out for yourself!
## Live demo
Alternatively, You can find a live web demo of our ChatBot to test [here](second url)

## Built with

* [IBM Cloudant](https://cloud.ibm.com/catalog?search=cloudant#search_results) - The NoSQL database used
* [IBM Cloud Functions](https://cloud.ibm.com/catalog?search=cloud%20functions#search_results) - The compute platform for handing logic
* [IBM API Connect](https://cloud.ibm.com/catalog?search=api%20connect#search_results) - The web framework used

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Authors

* **Cai Xin Rui** - [CaiXinRui](https://github.com/CaiXinRui)
* **Chee Jia Yuan** - [cheejiayuan512](https://github.com/cheejiayuan512)
* **Jefferson Li** - [JLZJ](https://github.com/JLZJ)
* **Shao Ya Kun** - [Yakun212](https://github.com/Yakun212)
* **Noah Seah** - [noahseah](https://github.com/noahseah)

See also the list of [contributors](https://github.com/cheejiayuan512/scdfxibm/contributors) who participated in this project.

## License

This project is licensed under the Apache 2 License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* Based on [Billie Thompson's README template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2).
