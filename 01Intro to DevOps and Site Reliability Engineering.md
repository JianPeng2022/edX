# 01 DevOps and Site Reliability Engineering
## What is Development + Operations (DevOps) and Site Reliability Engineering (SRE)?
**DevOps (Development + Operations)** is a set of practices, principles, and cultural philosophies that aim to enhance collaboration and communication between software development (Dev) and IT operations (Ops) teams. The primary goal is to automate and streamline the processes of software delivery and infrastructure changes, fostering a culture of continuous improvement and faster, more reliable releases.  
**Site Reliability Engineering (SRE)**, is a discipline that incorporates aspects of software engineering and applies them to infrastructure and operations problems. It was developed at Google to create scalable and highly reliable software systems.  
DevOps is the chef, focusing on creating new features and improvements. They're constantly innovating and experimenting, trying out new recipes and cooking techniques. SRE is the kitchen assistant, ensuring everything runs smoothly behind the scenes. They're responsible for setting up the kitchen, maintaining the equipment, and creating workflows that make the chef's job easier.  
1. **New Recipe Development**:
   - DevOps: Brainstorms new dishes, experiments with flavors and ingredients, and writes down the recipes (code).
   - SRE: Sets up the kitchen with all the necessary tools and equipment, creates a clean and organized workspace, and ensures everything is functioning properly.
2. **Preparing the Kitchen**:
   - DevOps: Gathers ingredients (data), prepares them (cleans and formats the code), and begins the cooking process (testing and deploying the code).
   - SRE: Manages inventory, ensures ingredients are fresh and available, and monitors the kitchen for any potential issues.
3. **Cooking and Serving**:
   - DevOps: Continuously monitors the cooking process, makes adjustments as needed, and ensures the dish is cooked to perfection (testing and refining the code).
   - SRE: Handles any unexpected hiccups or spills, makes sure the kitchen remains clean and organized and helps the chef deliver the finished dish to customers (users).
4. **Cleaning Up**:
   - DevOps: Analyzes the finished dish, identifies areas for improvement, and cleans up any leftovers (code or resources).
   - SRE: Cleans the kitchen, puts away tools and equipment, and prepares for the next round of cooking.
## Characteristics of the Pre-DevOps Era
Waterfall Model: a linear approach where each stage had to be completed before moving on to the next. This made it difficult to adapt to changes and respond quickly to new requirements.  
Siloed Teams: Developers, testers, and operations teams worked independently, often with little communication or collaboration. This created a "throw it over the wall" mentality, where each team blamed the other for problems.  
Manual Processes: Most tasks, from testing to deployment, were done manually. This was time-consuming and error-prone, leading to delays and inconsistencies.  
Limited Automation: There were few tools available to automate repetitive tasks, making it difficult to scale software development.  
Slow and Unreliable Delivery: Releases were infrequent and often buggy, causing frustration for both developers and users.  

Key Factors Contributing to the Emergence of DevOps: 
- Need for faster software delivery
- Inefficiencies of siloed teams
- Rise of automation tools
- Cloud computing: Cloud platforms offered scalability, flexibility, and access to shared resources, facilitating collaboration and faster deployments.

Key Principles of DevOps:
- Collaboration
- Automation
- Continuous Integration (CI): Developers integrate their code into a shared repository multiple times a day, with automated builds and tests to detect and address issues early in the development process.
- Continuous Deployment (CD): Continuous Deployment involves automatically deploying code changes to production environments after passing automated tests. This ensures rapid and reliable releases.
- Infrastructure as Code (IaC): IaC involves managing and provisioning infrastructure through code, enabling consistent and repeatable infrastructure deployments.
- Monitoring and Feedback: DevOps emphasizes continuous monitoring of applications and infrastructure, providing real-time feedback to identify and address issues promptly.

Which of the following are characteristics of the pre-DevOps era?
Select all answers that apply.
- **Inconsistent infrastructure**
- **Operations Engineers did not have a lot of insight into the product they were pushing into production**
- Infrastructure changes were done in a continuous manner, in small batch releases
- **Infrastructure changes were done ad hoc**
- Logs were pulled automatically and centrally managed
