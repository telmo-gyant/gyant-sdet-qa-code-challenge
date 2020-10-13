# Doctor Case Label

GYANT Doctor Case Label Challenge

## Background

To obtain training data for  our ML-based diagnosis, Gyant ask doctors to label medical cases by reading the EHR (electronic health record) of a patient encounter and labeling it with a diagnosis (condition).

An EHR is a text file that may look something like this:
The patient is a 32 year old female who presents to the Urgent Care complaining of sore throat that started 7 days ago. Developed into post nasal drip and then cough. No measured fevers. Had chills and body aches at the onset that resolved after the first day. A little facial headache with the congestion at times; better today. Some pressure on and off in the ears, no pain, hearing loss or tinnitus. Cough is mostly dry, sometimes productive of clear sputum. Denies shortness of breath. Never smoker. Has never needed inhalers. No history of pneumonia. Currently treating with ibuprofen which helps. Tried some over-the-counter Mucinex ES and vitamin C.

A condition consists of an ICD-10 condition code and description, e.g.:
F411    Generalized anxiety disorder
J00     Acute nasopharyngitis

Assignment

Create a web application that allows a doctor to review the EHR (one after another) and label it with one of a number of conditions. The case id, doctor id, label and time to label the case should be recorded for each decision.

Data
Please find the list of conditions and sample cases here.

Technology
Back-end: Node.js and MongoDB
Front-end: HTML5/JS/JQuery/CSS (Bootstrap optional)


Use Case
Doctor logs in using email/password (you can create a mock account in the DB)
The next case is presented
Doctor labels the case and moves on to the next one
When no more cases are left, a message "You are Done" is displayed
Doctor can log out and re-log in at any point


## Installation

*Note: This application was developed using [Node.js](https://nodejs.org/) version 13.*

Download or clone this repository and:

### 1. Install Dependencies

Install all needed dependencies:
```sh
$ npm i
```

### 2. Set Environment Variables

You can choose to set env variables while starting the server, or you can create a `.env` file by creating a duplicate of `.env.sample`.

*Note: Due to the nature of the project, a `.env` file is already included.*

### 3. Start the server

After following the previous steps, you can start the application with:
```sh
$ npm start
```

*Note: The server will be available on port `3000`.* 

## Notes

There is already a user created in the database:
```json
{
    "name": "Doctor Who",
    "email": "who@doctor.com",
    "password": "qwerty"
}
```

After you review every case it might be useful to drop the collection and repopulate, so that you can test the application again with a clean state.
To do so, please complete the following requests:
1. DELETE http://localhost:3000/cases
2. POST http://localhost:3000/cases/import
