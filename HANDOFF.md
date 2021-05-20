# Funding Finder Handoff Documentation
---
**Note our project folder & Google Drive are associated with our UW student emails which expire after our graduation, therefore it is recommended that these documents are saved elsewhere and backup accordingly.**

## Project Description

Funding Finder is the capstone project created by Team kala, a group of UW Informatics majors, and sponsored by the Washington State Department of Commerce. Our objective with Funding Finder was to create the infrastructure for an online platform in which small businesses can become more knowledgeable and resilient by connecting them with resources and funding opportunities.

Said platform consists the following:
- A website where small businesses can be matched with appropriate technical assistance providers and funding opportunities and access other online resources to build financial literacy.
- A website that acts as a content management system for the database of funding opportunities and technical assistance. Said information can be created, updated, and deleted by those with proper access to the system
- An API that connects the database to the main Funding Finder website

We made Funding Finder with a focus on supporting Tribal and Native American owned businesses first with hopes to expand the target demographic after our involvement.

To learn more about Team kala and our story click this link: [Website](https://addlinklater)

---

## Handoff Plan

As per agreement and the nature of our Capstone project, we intend to handoff our project with the materials listed below to our sponsor, the Washington State Department of Commerce and their affiliated partner, so that Funding Finder will live on after our involvement.

---

## Project Documentation & Assets

### Source Code & Documentation
Asset Name | Links
-------------------|-------------------
Funding Finder | [Github Repo](https://github.com/laurenng/Kala-Resilient-Small-Business)
Funding Finder API | [Github Repo](https://github.com/kelsonflint/rsbAPI)
Commerce Content Management System | [Github Repo](https://github.com/kelsonflint/rsbCommercePortal)
Front End Diagram | [PDF](https://drive.google.com/file/d/13jCrhQyt1GhTzryZtyrBmBNIYHchC9CF/view?usp=sharing)
Back End Diagram | [PNG](https://drive.google.com/file/d/1bMYJBAlAsX9n40OyYAnj22SLUT0VFB3M/view?usp=sharing)
Code Styling Guidelines | [PDF](https://airbnb.io/javascript/react/)

### Useful References
Asset Name | Links
-------------------|-------------------
Assorted Project Materials | [Google Drive](https://drive.google.com/drive/folders/1WWqiFswhnRUtzVISSQB4AmkxQtvRp9J5?usp=sharing)
Contacts Sheet | [Google Doc](https://docs.google.com/document/d/1mfG3p6qLAJpOfs7AgEJ3Lcjn00RxmbU6DtsXm9sQmzE/edit?usp=sharing)
Website Prototypes & Wireframes | [Figma](https://www.figma.com/file/2J2k7Jxc90jZH8ndi0ZIKo/kala-Wireframes?node-id=0%3A1)
Problem Context Research | [Folder](https://drive.google.com/drive/folders/1qDCsFTKwaYvcqBwzdajNHw8qshxRCeFz?usp=sharing)
User Research | [Folder](https://drive.google.com/drive/folders/1fb6A-0X_10IZSfI1q1zILfkYQosDiPT6?usp=sharing)
Cost Analysis & AWS Hosting Architecture | [Slides](https://docs.google.com/presentation/d/1OqSIfj7pWVKsv18hjOAFLhhW2VmnPr-GsPCBlK4Q3fM/edit?usp=sharing)


### Presentation Materials
Asset Name | Links
-------------------|-------------------
Final Presentation | [Video](https://youtu.be/IopUevw1WAo)
Final Presentation | [Slides](https://docs.google.com/presentation/d/1AQfUeK-AQ1aGYKWI4Z5g0efkkS6swOlAKysKJwTEMSg/edit?usp=sharing)
MVP Presentation | [Slides](https://docs.google.com/presentation/d/1CYb8Fmd9vHT6os6ibxAA-c_6UbzO9XVCaV9ShrfA9Co/edit?usp=sharing)
Project Summary | [Website](https://laurenng.github.io/about-kala/dist/index.html)
Project Poster | [PDF](https://drive.google.com/file/d/1-VMgGNAuQHeKHsXGmUQ5sjfbMC4_Wibs/view?usp=sharing)

---

## Design, Code, and Research Summaries

### Design

See the Design Summary section of [this presentation](https://app.pitch.com/app/presentation/c0de29c8-c84a-4a9e-8eb9-279561457e6d/5394b914-3b77-48a0-a559-ef21dce4b08a) for this information. This guide also includes style guidelines, justification for our designs, and features that were not able to be fully developed.

### Code

#### Front-End

The front end code is developed using a react-typescript framework. We chose React because it is modular and scalable. In combination with typescript, it also makes it the perfect environment for collaboration. Typescript, which is basically Javascript with enforced types, ensures that we are creating variables and parameters with the right intentions across all developers.

For our UI-components, we decided to use a component library called [Bulma](https://bulma.io/). This library helps keep our style and components consistent across the entire application with minimal styling and up keepings. This component library also provides great templates and structures for both mobile and desktop views.

The structure of the project is grouped by features and broad categories. We have a folder for each major feature (ie: library, searchPage, questionnaire, etc) as well as general groupings of (redux, assets, etc). Descriptions and usage for each page is described in the comments at the top of the page.

#### Back-End

The API has been built using Python's Flask framework. This has allowed for easy scalability and simplified requests. The application has been deployed to Amazon's API Gateway and utilizes AWS Lambda to handle requests. The deployment to AWS is handled by the [Zappa Package](https://pythonforundergradengineers.com/deploy-serverless-web-app-aws-lambda-zappa.html). Through this implementation, we can meet our variable demand without having to rely on servers. This allows for little to no-cost management of our application.

The API manages Funding Finder's user accounts/businesses, funding opportunities, assistance organizations, and announcements.

Funding Finder website, API, and Commerece Content Management System are all host via AWS - see Useful References: Cost Analysis & AWS Hosting Architecture for more information about the cloud infrastructure.

### Research

From our initial research we validated the claims of our sponsor regarding the struggles small businesses were facing, especially those owned by minorities, in the wake of the COVID-19 pandemic.

From reviewing literature we learned of the astonishing number of businesses that were forced to close permanently and how many were barely keeping their heads above water.

Through this review we were able to identify major issues that created the daunting problem we were challenged to solve.
- There is a general lack of resources for small businesses - particularly those aimed at aiding minority owned businesses. Whether it was access to funding, financial literacy, or general aid, these resources were scattered about the Internet and not made accessible.
- Government distrust not only makes small business owners trepidatious about grant/loans but historic and systemic issues also discourage them from even applying to begin with.
- The application process for funding opportunities is convoluted and contains jargon that requires a certain level of financial literacy. Such level of literacy small business owners often lack whether it be because of language barriers or lack of formal financial/business education. This creates a high barrier to entry when applied to the funding process for these business owners.

From our research we concluded that Funding Finder needed to help bridge that gap between small business owners and the resources they need to survive and thrive as a business.

**We chose to focus on Tribal small businesses because we wanted to prioritize the needs of a group of people that is often overlooked.** Ernie, the Tribal Liaison at the Washington State Department of Commerce, has also been very vocal about his excitement about this project, so we wanted to take advantage of his ability to connect us to users. Our TA, Tessa, is also a member of the Tulalip tribe, so we knew if we chose to focus on Tribal small businesses we could get quick feedback and input from someone who is closely related to our target user group.

 This lead to us focusing on creating features such as the Financial Literacy Library where users can browse curated resources, and the Funding & Assistance Matching Form that allows users to find the funding opportunities and technical assistance providers best suited for their business.

---

## Next Steps

We suggest that the next group that takes over this does more research to ensure our product is meeting user needs. This research would also be useful in figuring out what features need to be prioritized in terms of development.

Depending on findings from that research, I think these would also be good to prioritize in further development:
- Increase language accessibility by adding hard-coded translations
- Make the matching form more accessible to people with less financial literacy by adding tooltips and definitions for certain terms
- Improving overall usability and design

Please view the “Future Features” section of the Design Summary Guide for more of our thoughts on further development.
