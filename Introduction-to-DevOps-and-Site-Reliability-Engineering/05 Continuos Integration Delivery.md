# 05 Continuous Integration (CI) Continuous Delivery/Continuous Deployment (CD) 
**Continuous Integration (CI)** is a software development practice focused on regularly merging code modifications from development teams into a central repository. Its primary objective is to identify and resolve integration problems at an early stage of the development cycle and it emphasizes frequent code integration, automated building and testing procedures.
**Continuous Delivery (CD)** is a software development practice that aims to automate the process of releasing software changes to production environments in a frequent and reliable manner. It builds upon the concept of Continuous Integration (CI) by extending the automated pipeline to include deployment and release processes. In continuous delivery, the goal is to have software in a state where it can be released to production at any given time.
## What Is Continuous Integration (CI)?
Continuous Integration (CI) is a pivotal methodology in software development, reshaping the way teams collaborate and deliver high-quality code. At its core, CI involves the regular merging of code changes from multiple contributors into a shared repository. This iterative process serves as a proactive measure to identify and rectify integration issues at an early stage, fostering a development environment characterized by stability and efficiency. The build process includes tasks such as code compilation, automated testing, and the creation of executable artifacts. The automation ensures that the codebase is consistently and reliably built, reducing variability and ensuring a standardized output.  

Automated testing is another integral component of CI. Developers leverage various types of tests, including unit tests and integration tests, to validate the correctness of their code. This emphasis on automated testing serves a dual purpose: it verifies that the newly integrated code functions as expected, and it provides a safety net for catching regressions and defects.

A key feature of CI is the immediate feedback loop. Developers receive prompt notifications about the success or failure of their code integration. This rapid feedback allows for quick identification and resolution of issues, preventing the accumulation of defects that could lead to more complex problems down the line.
## What Is Continuous Delivery (CD)? (with humans making final release decision)
Continuous Delivery is a software development practice that extends the principles of Continuous Integration to ensure that the codebase is always in a deployable state. The primary objective is to make software releases reliable, predictable, and sustainable. In a Continuous Delivery pipeline, automated testing, and deployment processes are integral components.  
- Automated Testing: Similar to Continuous Integration, Continuous Delivery places a strong emphasis on automated testing. This includes unit tests, integration tests, and other forms of testing that validate the correctness and functionality of the codebase.
- Deployment Automation: Continuous Delivery involves automating the deployment process to create a consistent and repeatable method of releasing software. While the deployment to production may not occur automatically, the process leading up to deployment is automated.
- Deployment to Staging or Pre-Production: In Continuous Delivery, the software is typically deployed to a staging or pre-production environment where additional testing, user acceptance testing, or other validation processes can take place. This allows teams to ensure that the software is ready for production release.
- Manual Intervention for Production Release: Unlike Continuous Deployment, Continuous Delivery stops short of automatically deploying changes to the production environment. The decision to release to production requires human intervention, providing an additional layer of control and oversight.
## What Is Continuous Deployment (CD)? (without human)
Continuous Deployment takes the principles of Continuous Delivery a step further by automatically deploying every code change that passes automated testing directly to the production environment. The goal is to maximize efficiency and deliver new features or bug fixes to end-users as quickly as possible. 
- Automated Production Deployment: The hallmark of Continuous Deployment is the automatic deployment of code changes to the production environment once they pass automated tests. This minimizes manual intervention in the release process.
- High Level of Automation: Continuous Deployment relies heavily on automation throughout the entire development pipeline, from code integration to deployment. Automated testing and deployment scripts play a crucial role in achieving this level of automation.
- Immediate User Access: With Continuous Deployment, new features or fixes become immediately accessible to end-users. This rapid deployment cycle allows for quick responses to user feedback and changing market conditions.
## GitOps as a Deployment Tool
GitOps is a deployment methodology that leverages Git as a single source of truth for infrastructure and application configuration. This approach enables developers to manage their applications and infrastructure in a declarative manner, using familiar Git workflows.
- Declarative configuration: The desired state of the infrastructure and application is declared in Git repositories as YAML manifests, Helm charts, or other declarative formats.
- Single source of truth: The Git repository serves as the only source of truth for the desired state of the system, ensuring consistency and traceability.
- Pull-based reconciliation: A GitOps controller continuously monitors the Git repository for changes and automatically applies them to the target environment, ensuring the desired state is achieved.

Argo CD, Flux CD , Tekton CD , Jenkins X  

Which of the following is a primary benefit of Continuous Delivery (CD)?
- Increased deployment complexity
- Longer time to market
- **Higher software quality and reduced deployment risk**
- Increased manual testing
