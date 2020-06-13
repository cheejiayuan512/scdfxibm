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

![Crisis Comms Architecture diagram](/images/Crisis-Comms-Architecture-Node-RED.png)

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


## Long description

[More detail is available here](DESCRIPTION.md)

## Project roadmap

![Roadmap](roadmap.jpg)

## Getting started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```bash
dnf install wget
wget http://www.example.com/install.sh
bash install.sh
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be, for example

```bash
export TOKEN="fffd0923aa667c617a62f5A_fake_token754a2ad06cc9903543f1e85"
export EMAIL="jane@example.com"
dnf install npm
node samplefile.js
Server running at http://127.0.0.1:3000/
```

And repeat

```bash
curl localhost:3000
Thanks for looking at Code-and-Response!
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why, if you were using something like `mocha` for instnance

```bash
npm install mocha --save-dev
vi test/test.js
./node_modules/mocha/bin/mocha
```

### And coding style tests

Explain what these tests test and why, if you chose `eslint` for example

```bash
npm install eslint --save-dev
npx eslint --init
npx eslint sample-file.js
```

## Live demo

You can find a running system to test at [callforcode.mybluemix.net](http://callforcode.mybluemix.net/)

## Built with

* [IBM Cloudant](https://cloud.ibm.com/catalog?search=cloudant#search_results) - The NoSQL database used
* [IBM Cloud Functions](https://cloud.ibm.com/catalog?search=cloud%20functions#search_results) - The compute platform for handing logic
* [IBM API Connect](https://cloud.ibm.com/catalog?search=api%20connect#search_results) - The web framework used
* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

## Authors

* **Cai Xin Rui** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)
* **Chee Jia Yuan** - *Initial work* - [PurpleBooth](https://github.com/cheejiayuan512)
* **Jefferson Li** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)
* **Shao Ya Kun** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)
* **Noah Sia** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/cheejiayuan512/scdfxibm/contributors) who participated in this project.

## License

This project is licensed under the Apache 2 License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* Based on [Billie Thompson's README template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2).
