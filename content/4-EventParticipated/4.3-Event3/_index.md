---
title: "Event 3"
date: 2026-06-27
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Summary Report: "AWS Knowledge Battle" - Inter-group Competition

### Event Objectives

- Create an engaging and competitive environment where interns can test their knowledge of AWS core services.
- Encourage fast-paced teamwork, quick thinking, and collaborative problem-solving under pressure.
- Reinforce learning of AWS concepts such as EC2, S3, VPC, Security, Serverless, and Cost Management.

### Participants and Format

- **Participants:** 4 intern teams from the FCAJ program (including my team, Team AQI).
- **Format:** A quiz-based battle with rapid-fire questions.
    - **Round 1 (Individual):** Everyone answers on their own. Top performers advance.
    - **Round 2 (Team-based):** Teams huddle together to answer more complex, scenario-based questions.
    - **Round 3 (Finale):** A "shootout" where teams pick a category and answer a high-difficulty question to win points.

### Key Highlights

#### The Pressure of "Battle Mode"

- The rapid-fire nature pushed us to communicate effectively and make decisions quickly.
- We had less than 30 seconds to discuss each question and submit a single answer as a team.
- Staying calm and listening to each other was more valuable than shouting the loudest.

#### Real-World Scenario Questions

- The questions required more than just memorizing definitions; they tested our understanding of trade-offs.
- Example: Choosing the right architecture for a high-availability, low-latency application for Southeast Asian users.
- My team's solution (ECS/Fargate containers + ALB) was well received by the mentors, who appreciated our reasoning about removing EC2 management overhead.

#### Spotting Tricky Wording

- Some questions were designed to trap those who didn't read carefully.
- Example: The most cost-effective storage class for infrequently accessed JSON files that need instant retrieval is **S3 Standard-IA**, not S3 Intelligent-Tiering. The keyword was "accessed infrequently".

### Key Takeaways

#### Technical Knowledge

- **Network Basics are Fundamental:** Many questions covered VPCs, Subnets, Security Groups, and NACLs. Understanding networking is crucial even for ML Engineers.
- **Serverless vs. Managed vs. Unmanaged:** Knowing the differences between fully managed (Lambda), partially managed (ECS/Fargate), and unmanaged (EC2) services is key to choosing the right tool.
- **AWS Global Infrastructure:** Understanding which services are global (IAM, S3) and which are regional (EC2, VPC) is essential for designing resilient architectures.

#### Teamwork and Communication

- **Trust your Team's Strengths:** We won several rounds by quickly assigning roles and trusting each other's expertise.
- **Silence can be Golden:** The best teams were not the loudest, but the ones that listened carefully and submitted a unified answer.

### Applying to Work

- **Resource Naming & Tagging:** Proper tagging is crucial for cost tracking; I will ensure all my project resources are tagged correctly.
- **VPC and Subnets:** I now better understand why my SageMaker Notebook needs to be in a specific subnet; I will pay closer attention to networking configurations.
- **Cost Optimization:** I will prioritize using Spot Instances for non-critical training tasks and monitor spending with AWS Budgets.
- **High Availability & Fault Tolerance:** Designing for multi-AZ deployments is a requirement for enterprise systems.
- **Understand the "Why" of Services:** Understand the trade-offs of AWS services, not just their features, to make better architectural decisions.

### Event Experience

The AWS Knowledge Battle was much more than a fun quiz. It was a perfect summary of the internship's first few weeks.

- It forced us to recall and synthesize everything we learned about EC2, S3, Security Groups, IAM, and Serverless architectures under pressure.
- The competitive environment was highly effective for consolidating knowledge.
- It helped me step out of my "ML silo" and recognize the importance of foundational infrastructure like VPCs, Load Balancers, and Security Groups.

#### Some event photos

![Teams discussing and answering quiz questions during the Knowledge Battle](/images/4-Events%20Participated/event3.1.jpg)

![Scoreboard showing the results of the inter-group competition](/images/4-Events%20Participated/event3.2.jpg)

> This event reminded me that a good ML Engineer doesn't just know the model—they also understand the infrastructure it relies on.
