1.0 Introduction

We live in a world where many people cannot achieve their life goals because the external conditions like poverty, geographical localization, socio-cultural issues, etc. had a negative influence on their lives. We live in a world where success is tied mostly to good education but many don’t have access to it. Although the Internet is an enormous repository of knowledge, this knowledge is often disorganized and dispersed, costly or there’s simply not enough motivation for people to get in front of the computer to learn. 
Mentee is going to change this because thanks to its attention to mentorship. We aim at fostering the relationship between mentees and mentors because mentorship is the next big thing that empowers people and has the potential to turn anyone in a leader.
 
“A mentor is someone who allows you to see the hope inside yourself” 
— Oprah Winfrey
Mentors not only share their knowledge and experience with others but through the relationship developed with their mentees they provide moral support and stimulate personal and professional growth. This relationship can push people to new heights and make them achieve things they wouldn’t be otherwise capable of. This is why they can have a real impact on the people and their lives.
The power of mentorship is always more appreciated within communities of a certain kind, academic field or corporate setting. Mentorship it is slowly gaining traction in today’s society as always more people look for mentors online. Also there are always more people willing to be mentors and look proactively for people to dedicate their time to.
People who have achieved success often say that their success would never be possible without certain people who acted as mentors in their lives.

2.0 The vision

Mentee platform, powered by the EOS.IO software, wants to be the place where mentees and mentors meet and exchange knowledge and acquire new experiences, where they can establish a connection and begin the mentorship, bringing mutual benefit to both. 
The ability to have access to different mentors makes Mentee a perfect solution for unlimited access to knowledge which is retained in the minds of many people. Each experience and each successful story is different and only those who succeeded know what needs to be done to get there. Using Mentee, these people have the opportunity to access this knowledge and to connect with others to be more successful. Thanks to Mentee they can have a real positive impact on someone’s life.
Mentee Network’s goal is to create the world’s first on-chain educational platform where learning courses and scientific content can be stored. Through an API it can be  accessed by different decentralized applications as a peer-reviewed and trustworthy source of information. 
Though the mentorship the real focus of the platform as the end result is a blockchain Curriculum Vitae. Official education and past working experiences matter but it isn’t always the proof of what a person really knows. Life experiences, undocumented works or courses make often a big part of someone’s personal kit. The successful entrepreneurs without higher education are proof that what we learn during our lives is often more valuable than the titles on the paper. Mentee will bring onto the surface all these skills showing employers what mentees really know which will be beneficial for both parties.
Mentee Network has the potential to become a school for entrepreneurs where they get the knowledge and experience from mentors, complete tasks, create and work in teams and deliver results. It benefits not only mentees but also mentors as, through mentoring,  they get to reflect on their own leadership style and methods, which can make them more thoughtful and intentional about own leadership. Mentee Network can be used as online classes where students and teachers meet.
There’s a reason why this app is built on the EOSIO blockchain and this is because blockchain is an immutable ledger. Whatever new skill and progress will be achieved by the mentee, it will be recorded in a permanent way. This means that the blockchain CV will act as a live certificate of the real knowledge and skills possessed that can be updated in real time as new information is being added.

full whitepaper consultable at http://mentee.network/wp-content/uploads/2019/11/MENTEE-WHITE-PAPER-.pdf

# Guide to Mentee development

# Intro
Mentee is a platform intended to be developed on top of EOSIO blockchain. Main components of Mentee will be written in C++ (smart-contracts) and the UI will represent a JS website that will display the state of the platform which is obtained from smart-contracts.

# Platform mechanics

Mentees will stake their MNT tokens and take to the platform to look for mentors with whom they will enter in contact through chat or a video conference. Mentees will also go through different courses created by other platform participants, quizzes and tests to check the level of their knowledge and visualize it on the blockchain CV diagram. All actions will take place and are processed in the EOSIO blockchain. 
Mentees and mentors will get Menteepower and Mentorpower from their mentorship activity and from creating courses and solving quizzes and tests. They will interact with the smart contract during platform activities thus they need to have a signed up EOSIO account.
Mentees and mentors will vote on courses, quizzes and tests to create a decentralized source of verified repository of educative material. Mentors will give mentees tasks to make them gain new skills and knowledge. A mentor will be also able to create a task for anyone to pick and he will then have the possibility to choose the best to join his team.
Platform's state is recorded and stored on the blockchain.
The platform process requires that information (platform state) be read from the smart-contract, as well as that user actions are converted into transactions and broadcasted to EOSIO network, thus sent to the smart-contract.

All the actions that a user can perform are invocations of various functions of the smart-contract which are performed by signing and sending transactions. This includes:

- creating personal profile

- placing "tasks" in the task queue (each mentee takes on tasks)

- giving tasks to a specific mentee (this is resolved by the mentor)

- voting

- creating courses, tests,quizzes

- opening groups

Every type of actions requires (1) a certain task to be placed and (2) a certain amount of time to complete.


# Resources
There are three resource types in the platform: CPU, NET, RAM.

The user will need to manage these resources by its own. 

# Blockchain CV
Blockchain CV is an arbitrary size 2D circular grid. Each cell represents a category. Each category may be filled with information (transactions about mentorship activity, completed tasks, courses, quizzes, certificates, attestations etc.) or not. Each user may have multiple mentors who contributed to his blockchain CV.

# Mentees
Mentees and mentors represent the main platform object. A mentee may have a mentor or it may be awaiting to be approved.

Mentee and mentor fill his profile with the following information:

- MNT stake, total MNT, available MNT, Menteepower, Mentorpower
- location
- eos account
- name
- profession
- about me
- photo
- education
- skills
- experience
- goals
- mentors
- mentees


Mentees and mentors both need to work on the development of the knowledge and skills to gain Menteepower and Mentorpower and add to their blockchain CV.

# Incentives

- Each mentor can open a free group. The group with over 2 mentees will require an additional stake. Adding each ten mentees (10, 20, 30 etc.) requires more stake.

- Additionally to the mentorship, each mentor will have the ability to set a minute-payment for each minute of their time so they can work as profssional advisers directly from the platform. Mentee platform collects a fee for this activity.

- Courses, quizzes, tests, tasks creation generates Mentorpower

- Completing courses, tasks etc. generates Menteepower

- Voting on courses, quizzes, tasks, tests generates Mentorpower

## Mentorpower
Voting on course edit proposals will require a stake of MNT tokens for a period of 21 days. Voting up or down the course edit proposals stakes MNT for the amount of the vote. Proposing an edit stakes 50 MNT as an anti-spam measure.


# Actions

## Generate edu
A function called each time a user wants to create an educational course, quiz, test etc. It can be presented under the form of questions, videos, graphics, pictures, etc. Each time an edu is created it will be available for approval of other users. The more users voted on a specific edu, the more reliable the information contained in it is. The edu module is used to create
courses to be included in the database. Proposed tasks contain an IPFS (or dStor) hash time stamped on the EOS blockchain. Staked MNT tokens are needed for edu creation. The user creates Menteepower for each successful edu.

## Edit edu
Edit edu function is called each time a user wants to edit an edu module. Each proposed change is a tuple object containing an IPFS hash pointing to the parent version as well as an IPFS hash pointing to the new version. Staked MNT tokens are
needed to propose the edits. The user creates Menteepower for each successful edu module edit. This creates a proportional amount of the MNT inflationary token reward allotted for content.

## Generate task
This function is called by the mentor in case she wants to create a specific task for a specific kind of mentee. In this sense, it can be used by an employer acting as a mentor who generates tasks for mentees as candidates for a workplace inside her business. The task meets a specific mentor’s need and is created with a specific purpose rather than being a general edu content. Staked MNT tokens are needed to generate a task.

## Complete task
The mentee needs to stake MNT tokens to accept a task created by a mentor. After the task is completed she’s rewarded with Menteepower.

## Minute-payment
A mentor sets the price for each minute of his consulting. He starts the clock when a mentee checks in. 



# Development instructions
We invite everyone to help building Menee platform to create a fully decentralized EOSIO based app.
Start by joining https://t.me/menteenetdev on Telegram 

At the current stage, we started building the front end in react (consultable here https://menteenetwork.commoneffort.now.sh/#/ or here https://www.youtube.com/watch?v=CvB9wc7p_bA&feature=youtu.be).

We have also Scatter implementation that needs to get updated and connected to the user profile.
Mentee is planned to be built on the https://github.com/EveripediaNetwork code base and it will use https://github.com/qTox/qTox for communication, files transfer, groups, and screen sharing.

## Educational courses
Use https://github.com/EveripediaNetwork/backend-api to build Generate edu, Edit edu, Generate task (see above). Everipedia's article module need to be transformed into module for educational courses, quizzes and tasks.

## User profile
Use https://github.com/EveripediaNetwork/backend-api to build user profile. It requires Scatter connection.
User profile needs to handle the following information:
On-chain:
- Balance detail: MNT stake, total MNT, available MNT, Mneteepower, Mentorpower
- location
- eos account
- name
- profession
- about me
- photo
- goals
- mentors
- mentees
- my courses
- my votes
- activity
- education
- skills
- experience
Off-chain, saved on IPFS or dStore, private
- detailed feedback from mentors and mentees
- character traits

We can use https://github.com/TokTok/c-toxcore to handle mentee-mentor connection requests.

## Token contract
The MNT token will use the same token contract as Everipedia https://github.com/EveripediaNetwork/Everipedia with the difference that instead of Brainpower the contract will mint Menteepower and Mentorpower for the activities pertaining to mentees and mentors. 
Total MNT supply is 1B with an initial 5% inflation rate. Each time the contract mints 5 Menteepower or 5 Mentorpower, 1 Menteepower or 1 Mentorpower is minted and sent to the Mentee DAC account menteedac.x

## Communication
We use https://github.com/qTox/qTox code base to build encrypted video communication, voice calls, and instant messagging. qTox is built from https://github.com/TokTok/c-toxcore. The Mentee platform should have all the functionalities of qTox. 

## Blockchain CV
Blockchain CV is an NTT (non-transferabe token) with some off-chain data that will be accessible by mentors or anyone else on demand. We want to use https://github.com/CryptoLions/SimpleAssets. Here's a list of all EOSIO standards https://github.com/eosio-standards-wg/tokenconfigs
The CV example we aim for is below

![Image description](https://github.com/Commoneffort/mentee.network/blob/master/public/assets/images/blockchain%20cv.png)

## 
