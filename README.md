# Pulse-AI
## Inspiration
In emergency situations, dispatchers are often inundated with a high volume of calls, many of which are waiting in a FIFO (First-In, First-Out) queue to connect with a dispatcher. Compounding this challenge is the fact that approximately 20% of the U.S. population speaks a language other than English as their first language, which can further complicate communication and delay response times. Pulse AI is designed to assist dispatchers by automating the triage process for these queued calls.

Pulse AI ensures a seamless and effective solution for managing emergency call prioritization and enhances dispatcher efficiency by utilizing:

Google Kubernetes Engine for orchestration and deployment, ensuring availability

Azure AI Speech Service for real-time speech-to-text conversion

XGBoost (Extreme Gradient Boosting) for developing models to predict severity scores

MongoDB Atlas integration for data management

Gemini large language model (LLM) for real-time summarization and analysis

React + JS for front-end

Flask + Python for back-end support

Our "severity score" was inspired by Common Vulnerabilities and Exposures (CVE) ratings.
## What it does
Pulse AI is an AI-powered call triage and prioritization system designed to assist emergency dispatchers by:

Automatically transcribing calls in real-time using generative AI.

Supporting multiple languages with automatic language translation.

Using machine learning to predict a severity score for each case based on trained data.

Ranking emergencies based on urgency to optimize resource allocation.
## How we built it
Speech-to-Text Conversion: Leveraged Azure's Speech-to-Text API to transcribe live audio recordings of emergency calls that are in the dispatch queue.

Severity Scoring: Developed a machine learning algorithm using gradient-boosted trees to assign severity scores based on features pulled from transcribed calls, incorporating crucial details such as location, nature of the emergency, and immediate risks.

Priority Ranking: Implemented a system to rank emergencies and help dispatchers focus on the highest-priority cases first.

Database Integration: Utilized MongoDB Atlas to store call data and transcripts, and developed a query system to summarize key points and update severity scores in real-time.

Technology Stack: Built the system using Google Kubernetes Engine for orchestration, Azure AI Speech Service for transcription, and integrated with large language models like Gemini. The frontend and backend are developed using React and Flask with Python, respectively.
## Challenges we ran into
Accuracy of Transcriptions: Ensuring high accuracy of speech-to-text conversion in noisy environments.

Severity Scoring: Developing an algorithm that can reliably assess the severity of a situation from sometimes ambiguous or incomplete information.

Front-end Development: Handling the high volume of incoming calls and processing data quickly enough to be actionable in urgent situations.
## What we learned
Dynamic Systems are Crucial: Real-time updates and dynamic severity scoring are essential for handling evolving emergency situations.

Human-AI Collaboration: AI can significantly enhance human decision-making but should work with a human for judgment rather than replace one.

##Accomplishments we are proud of
Efficient Triage: Successfully reduced dispatcher workload by automating the initial triage process and prioritizing calls effectively.

Real-Time Updates: Enabled dynamic updates to severity scores, ensuring that dispatchers have the most current information.

Improved Dispatcher Focus: Helped dispatchers focus on critical cases by providing an AI-generated priority list and reducing manual effort.
## Whats next?
Integration with Additional Services: Explore opportunities to integrate Pulse AI with other public health and emergency response services to broaden its impact.

Continual Improvement: Refine severity scoring algorithms based on real-world data.

Expansion of Features: Develop new features such as automated follow-ups for ambiguous cases and more advanced analytics for emergency response optimization.

AI Prompts: Prompting dispatchers with follow-up questions to gather missing information.
