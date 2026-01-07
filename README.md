# ![GPT Prompts](https://raw.githubusercontent.com/voytas75/GPTprompts/main/images/OM_1683528517050_32x32.jpg) GPT prompts

![GPTprompt](https://github.com/voytas75/GPTprompts/blob/main/images/smartlot_ultra_realistic.png?raw=true "GPTprompt")

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/A0A6KYBUS)

> Welcome to our site, where GPT prompts are just the beginning of the journey. Remember, just as there are countless individuals around us with their own unique stories to tell, there are infinite possibilities for exploration and discovery here. Let's embark on this journey together, with curiosity and an open mind.

## Table of Contents

1. [GPT-5 prompt optimizer tool](#1-gpt-5-prompt-optimizer-tool)
2. [Chain-of-Thought (CoT) Prompting](#2-chain-of-thought-cot-prompting)
3. [Line-of-Thought (LoT) Prompting](#3-line-of-thought-lot-prompting)
4. [Few-Shot Prompting](#4-few-shot-prompting)
5. [Self-Consistency](#5-self-consistency)
6. [Meta Prompting](#6-meta-prompting)
7. [Retrieval-Augmented Generation](#7-retrieval-augmented-generation)
8. [Prompt's classification (new)](#8-prompts-classification-new)
9. [Prompts](#9-prompts)
10. [Useful Links](#10-useful-links)

---

## 1. GPT-5 prompt optimizer tool

[...prompt optimizer tool we’ve built, will serve as a launchpad for your use of GPT-5...](https://platform.openai.com/chat/edit?optimize=true)

## 2. Chain-of-Thought (CoT) Prompting

1. **Step-by-Step Instructions**:

    ```text
    First, identify the key variables. Next, analyze their relationships. Finally, predict the outcome.
    ```

    ```text
    Break down the problem into smaller steps and solve each one.
    ```

2. **Explicit Reasoning**:

    ```text
    Explain your reasoning step-by-step.
    ```

    ```text
    Describe how you arrived at this conclusion.
    ```

3. **Intermediate Steps**:

    ```text
    List the steps needed to solve this problem before giving the final answer.
    ```

    ```text
    What are the intermediate steps to reach the solution?
    ```

4. **Clarifying Questions**:

    ```text
    Can you provide more details on why this solution works?
    ```

    ```text
    What assumptions are you making in this reasoning?
    ```

5. **Contextual Prompts**:

    ```text
    Given the historical data, predict the future trend.
    ```

    ```text
    Based on the provided information, what is the next logical step?
    ```

## 3. Line-of-Thought (LoT) Prompting

1. **Identify Key Events:**:

   ```text
   List all significant events explicitly mentioned in the narrative, regardless of their chronological order.
   ```
   
2. **Extract Potential Causal Links:**:

   ```text
   For each event, explicitly state possible causes and effects based solely on narrative evidence.
   ```

3. **Evaluate Evidence Strength:**:

   ```text
   Assign a confidence level (high, medium, low) to each identified causal link based on textual support.
   ```

4. **Construct Preliminary Causal Graph:**:

   ```text
   Represent identified causal relationships visually, clearly indicating the directionality and confidence levels.
   ```

5. **Review for Chronological Bias:**:

   ```text
   Critically assess whether identified causal links rely incorrectly on narrative sequence rather than logical causation.
   ```

6. **Refine and Validate Graph:**:

   ```text
   Adjust the causal graph to remove chronological biases, ensuring causal relationships are logically sound and narrative-independent.
   ```

7. **Summarize Findings:**:

   ```text
   Provide a concise summary highlighting robust causal relationships, identified biases, and areas requiring further narrative clarification.
   ```

## 4. Few-Shot Prompting

1. **Examples**:

    ```text
    Here are some examples of similar problems and their solutions. Use these to solve the new problem.
    ```

    ```text
    Given these examples, how would you approach this new task?
    ```

2. **Analogies**:

    ```text
    This problem is similar to [example]. How would you solve it using the same approach?
    ```

    ```text
    Think of this situation like [analogy]. What would be the next step?
    ```

## 5. Self-Consistency

1. **Multiple Solutions**:

    ```text
    Generate multiple solutions and choose the most consistent one.
    ```

    ```text
    Provide different approaches to solve this problem and compare them.
    ```

2. **Verification**:

    ```text
    Verify the solution by checking each step.
    ```

    ```text
    Cross-check the final answer with the initial conditions.
    ```

## 6. Meta Prompting

1. **Reflective Prompts**:

    ```text
    Reflect on the steps taken and identify any potential errors.
    ```

    ```text
    What could be improved in the reasoning process?
    ```

2. **Self-Questioning**:

    ```text
    Ask yourself if the solution makes sense.
    ```

    ```text
    What questions would you ask to verify this solution?
    ```

## 7. Retrieval-Augmented Generation

1. **Information Retrieval**:

    ```text
    Retrieve relevant information from the provided data before solving the problem.
    ```

    ```text
    Use the given resources to gather necessary details.
    ```

2. **Contextual Integration**:

    ```text
    Integrate the retrieved information into your reasoning.
    ```

    ```text
    How does the additional data influence your solution?
    ```

## 8. Prompt's classification (new)

1. Arts and Humanities:
   1. Creative Writing and Narrative Composition.
      - [prompt 78](prompt/078-life-event.md) Life event
      - [prompt 87](prompt/087-the-ai-spark-exploring-the-impact-of-ai-on-human-creativity-and-diversity.md) The AI Spark: Exploring the Impact of AI on Human Creativity and Diversity
      - [prompt 90](prompt/090-craft-your-thesis-ai-assistant-for-argumentative-essay-writing.md) Craft Your Thesis: AI Assistant for Argumentative Essay Writing
      - [prompt 93](prompt/093-unpacking-the-layers-transforming-statements-into-insightful-questions-and-answers.md) Unpacking the Layers: Transforming Statements into Insightful Questions and Answers
      - [prompt 100](prompt/100-guiding-the-user-crafting-clear-and-contextual-instructions.md) Guiding the User: Crafting Clear and Contextual Instructions
      - [prompt 118](prompt/118-genre-adaptive-narrative-direction.md) Genre-Adaptive Narrative Direction
      - [prompt 151](prompt/151-mega-meta-prompt-curiosity-open-loop-engine.md) Curiosity Open-Loop Engine
   2. Other Specialized Areas in Arts and Humanities.
      - [prompt 114](prompt/114-cross-domain-ai-resilient-test-analysis.md) Cross-Domain AI-Resilient Test Analysis
2. Biological Sciences.
   - [prompt 114](prompt/114-cross-domain-ai-resilient-test-analysis.md) Cross-Domain AI-Resilient Test Analysis
   - [prompt 134](prompt/134-neural-model-interpretability-exploration-guide.md) Neural Model Interpretability Exploration Guide
   - [prompt 154](prompt/154-from-randomness-to-life-memory-chains-and-emergent-causation.md) From Randomness to Life: Memory Chains and Emergent Causation
3. Business and Economics:
    1. Marketing and Advertising.
       - [prompt 116](prompt/116-crafting-conversion-driven-marketing-copy.md) Crafting Conversion-Driven Marketing Copy
       - [prompt 117](prompt/117-xgboost-insights-for-customer-engagement-strategy.md) XGBoost Insights for Customer Engagement Strategy
       - [prompt 155](prompt/155-change-communication-pack-release-notes-rollout-support-playbook.md) Change Communication Pack: Release Notes, Rollout Plan, and Support Playbook
    2. Finance and Financial Management.
       - [prompt 18](prompt/018-personal-financial-advisor.md) Personal financial advisor
       - [prompt 126](prompt/126-stochastic-decision-forests-insight.md) Stochastic Decision Forests Insight
    3. Entrepreneurship and Startup Culture.
       - [prompt 24](prompt/024-build-a-prompt.md) Build a prompt
       - [prompt 86](prompt/086-dorm-room-revolution-design-products-to-empower-college-students.md) Dorm Room Revolution: Design Products to Empower College Students
       - [prompt 127](prompt/127-ascending-auction-analysis-and-application.md) Ascending Auction Analysis and Application
    4. International Business and Trade.
    5. Human Resources and Organizational Behavior.
       - [prompt 59](prompt/059-refund-request.md) Refund request
       - [prompt 101](prompt/101-understanding-your-needs-clarifying-refund-requests-effectively.md) Understanding Your Needs: Clarifying Refund Requests Effectively
       - [prompt 121](prompt/121-organizational-knowledge-management-analysis.md) Organizational Knowledge Management Analysis
    6. Operations Management.
       - [prompt 106](prompt/106-optimization-algorithm-simulation.md) Optimization Algorithm Simulation
       - [prompt 121](prompt/121-organizational-knowledge-management-analysis.md) Organizational Knowledge Management Analysis
    7. Business Strategy and Competitive Analysis.
       - [prompt 105](prompt/105-expert-panel-synthesis-with-authority-regularization.md) Expert Panel Synthesis with Authority Regularization
       - [prompt 127](prompt/127-ascending-auction-analysis-and-application.md) Ascending Auction Analysis and Application
       - [prompt 145](prompt/145-executive-summary-synthesis-prompt-transforming-detailed-research-reports.md) Executive Summary Synthesis Prompt: Transforming Detailed Research Reports
    8. Accounting and Auditing.
    9. Business Ethics and Corporate Social Responsibility.
       - [prompt 59](prompt/059-refund-request.md) Refund request
       - [prompt 121](prompt/121-organizational-knowledge-management-analysis.md) Organizational Knowledge Management Analysis
    10. Real Estate and Property Management.
    11. Supply Chain Management.
    12. Economics Theory and Application.
        - [prompt 94](prompt/094-the-trade-offs-we-make-demystifying-opportunity-cost.md) The Trade-Offs We Make: Demystifying Opportunity Cost
        - [prompt 127](prompt/127-ascending-auction-analysis-and-application.md) Ascending Auction Analysis and Application
    13. Economic Development and Policy.
    14. Investment and Portfolio Management.
        - [prompt 68](prompt/068-financial-sentiment.md) Financial Sentiment
        - [prompt 127](prompt/127-ascending-auction-analysis-and-application.md) Ascending Auction Analysis and Application
    15. Consumer Behavior and Market Research.
        - [prompt 86](prompt/086-dorm-room-revolution-design-products-to-empower-college-students.md) Dorm Room Revolution: Design Products to Empower College Students
        - [prompt 101](prompt/101-understanding-your-needs-clarifying-refund-requests-effectively.md) Understanding Your Needs: Clarifying Refund Requests Effectively
        - [prompt 116](prompt/116-crafting-conversion-driven-marketing-copy.md) Crafting Conversion-Driven Marketing Copy
    16. Corporate Finance and Governance.
        - [prompt 68](prompt/068-financial-sentiment.md) Financial Sentiment
    17. Risk Management and Insurance.
         - [prompt 126](prompt/126-stochastic-decision-forests-insight.md) Stochastic Decision Forests Insight
    18. Taxation and Public Finance.
    19. Management Information Systems.
    20. Innovation and Technology Management.
        - [prompt 86](prompt/086-dorm-room-revolution-design-products-to-empower-college-students.md) Dorm Room Revolution: Design Products to Empower College Students
        - [prompt 116](prompt/116-crafting-conversion-driven-marketing-copy.md) Crafting Conversion-Driven Marketing Copy
        - [prompt 121](prompt/121-organizational-knowledge-management-analysis.md) Organizational Knowledge Management Analysis
    21. Other Specialized Areas in Business and Economics.
4. Chemistry.
   - [prompt 92](prompt/092-stepping-up-to-the-challenge-categorization-and-problem-solving-with-clear-reasoning.md) Stepping Up to the Challenge: Categorization and Problem Solving with Clear Reasoning
5. Computer and Information Sciences:
    1. Artificial Intelligence and Machine Learning.
       - [prompt 17](prompt/017-experienced-prompt-engineer.md) Experienced prompt engineer
       - [prompt 21](prompt/021-developergpt.md) DeveloperGPT
       - [prompt 42](prompt/042-optimo.md) Optimo
       - [prompt 57](prompt/057-lark-prompt.md) LARK Prompt
       - [prompt 62](prompt/062-adaptive-interactive-logic-prompt-ailp.md) Adaptive Interactive Logic Prompt (AILP)
       - [prompt 63](prompt/063-keyphrase-expansion-clustering-assistant.md) Keyphrase Expansion Clustering Assistant
       - [prompt 65](prompt/065-dynamic-expertise-activation-prompt-deap.md) Dynamic Expertise Activation Prompt (DEAP)
       - [prompt 66](prompt/066-roleplay-discussion.md) Roleplay-discussion
       - [prompt 69](prompt/069-mire.md) MiRe
       - [prompt 70](prompt/070-codegpt-three-experts.md) CodeGPT - Three experts
       - [prompt 71](prompt/071-olmo.md) OLMo
       - [prompt 72](prompt/072-beyond-the-paper.md) Beyond the Paper
       - [prompt 73](prompt/073-beyond-humanity.md) Beyond Humanity
       - [prompt 74](prompt/074-machine-learning-made-easy.md) Machine Learning Made Easy
       - [prompt 75](prompt/075-maximizing-the-power-of-large-language-models-a-comprehensive-guide-for-beginners-and-experts.md) Maximizing the Power of Large Language Models: A Comprehensive Guide for Beginners and Experts
       - [prompt 76](prompt/076-unveiling-bias-in-nlp-benchmarks-understanding-parameters-and-implications.md) Unveiling Bias in NLP Benchmarks: Understanding Parameters and Implications
       - [prompt 80](prompt/080-e-3-equivariant-mesh-neural-networks-a-comprehensive-explanation.md) E(3)-Equivariant Mesh Neural Networks: A Comprehensive Explanation
       - [prompt 81](prompt/081-understanding-automatic-behavior-optimization-abo-a-step-by-step-guide.md) Understanding Automatic Behavior Optimization (ABO): A Step-by-Step Guide
       - [prompt 84](prompt/084-beyond-pairwise-optimizing-conversational-ai-using-listwise-preference-optimization.md) Beyond Pairwise: Optimizing Conversational AI using Listwise Preference Optimization
       - [prompt 85](prompt/085-beyond-traditional-metrics-analyzing-document-processing-with-anls-and-specialized-prompting.md) Beyond Traditional Metrics: Analyzing Document Processing with ANLS and Specialized Prompting
       - [prompt 87](prompt/087-the-ai-spark-exploring-the-impact-of-ai-on-human-creativity-and-diversity.md) The AI Spark: Exploring the Impact of AI on Human Creativity and Diversity
       - [prompt 88](prompt/088-building-better-together-a-guide-to-ai-powered-product-copilot-development.md) Building Better Together: A Guide to AI-Powered Product Copilot Development
       - [prompt 97](prompt/097-balancing-accuracy-and-density-mastering-the-task-spectrum.md) Balancing Accuracy and Density: Mastering the Task Spectrum
       - [prompt 99](prompt/099-crafting-solutions-a-user-centric-approach-to-problem-solving.md) Crafting Solutions: A User-Centric Approach to Problem-Solving
       - [prompt 110](prompt/110-blockchain-efficiency-dynamic-transaction-storage-and-verkle-tree-strategies.md) Blockchain Efficiency: Dynamic Transaction Storage and Verkle Tree Strategies
       - [prompt 111](prompt/111-advanced-guide-to-machine-learning-in-survey-sampling-and-estimation.md) Advanced Guide to Machine Learning in Survey Sampling and Estimation
       - [prompt 112](prompt/112-cross-domain-application-of-machine-learning-and-bootstrap-techniques.md) Cross-Domain Application of Machine Learning and Bootstrap Techniques
       - [prompt 113](prompt/113-adversarial-robustness-evaluation-prompt.md) Adversarial Robustness Evaluation Prompt
       - [prompt 115](prompt/115-robust-ic-sf-hypothesis-generation.md) Robust IC-SF Hypothesis Generation
       - [prompt 120](prompt/120-actionsense-insight-generator.md)
       - [prompt 126](prompt/126-stochastic-decision-forests-insight.md) Stochastic Decision Forests Insight
       - [prompt 128](prompt/128-academic-paper-structure-comprehension-and-model-enhancement.md) Academic Paper Structure Comprehension and Model Enhancement
       - [prompt 129](prompt/129-understanding-individual-fairest-community-search-in-hins.md) Understanding Individual Fairest Community Search in HINs
       - [prompt 131](prompt/131-privacy-conscious-oov-discovery-for-language-model-enhancement.md) Privacy-Conscious OOV Discovery for Language Model Enhancement
       - [prompt 132](prompt/132-comprehensive-collaborative-perception-dataset-analysis.md) Comprehensive Collaborative Perception Dataset Analysis
       - [prompt 133](prompt/133-dptraj-pm-implementation-and-analysis-guide.md) DPTraj-PM Implementation and Analysis Guide
       - [prompt 134](prompt/134-neural-model-interpretability-exploration-guide.md) Neural Model Interpretability Exploration Guide
       - [prompt 135](prompt/135-mathematical-reasoning-model-evaluator-mrme.md) Mathematical Reasoning Model Evaluator (MRME)
       - [prompt 140](prompt/140-prompt-improver.md) Prompt improver
       - [prompt 142](prompt/142-summarize-with-metrics.md) Summarize with metrics
       - [prompt 147](prompt/147-narrative-causality-analysis.md) Narrative Causality analysis
       - [prompt 152](prompt/152-multi-role-scientific-query-processor.md) SR-Agent Ensemble: Multi-Role Scientific Query Processor
       - [prompt 153](prompt/153-intent-driven-specs-alignment-response-generator.md) Intent-Driven Specs & Alignment Response Generator
    2. Data Science and Big Data Analytics.
       - [prompt 62](prompt/062-adaptive-interactive-logic-prompt-ailp.md) Adaptive Interactive Logic Prompt (AILP)
       - [prompt 63](prompt/063-keyphrase-expansion-clustering-assistant.md) Keyphrase Expansion Clustering Assistant
       - [prompt 66](prompt/066-roleplay-discussion.md) Roleplay-discussion
       - [prompt 76](prompt/076-unveiling-bias-in-nlp-benchmarks-understanding-parameters-and-implications.md) Unveiling Bias in NLP Benchmarks: Understanding Parameters and Implications
       - [prompt 106](prompt/106-optimization-algorithm-simulation.md) Optimization Algorithm Simulation
       - [prompt 116](prompt/116-crafting-conversion-driven-marketing-copy.md) Crafting Conversion-Driven Marketing Copy
       - [prompt 117](prompt/117-xgboost-insights-for-customer-engagement-strategy.md) XGBoost Insights for Customer Engagement Strategy
       - [prompt 135](prompt/135-mathematical-reasoning-model-evaluator-mrme.md) Mathematical Reasoning Model Evaluator (MRME)
       - [prompt 142](prompt/142-summarize-with-metrics.md) Summarize with metrics
       - [prompt 143](prompt/143-expert-techniques-for-solving-complex-problems-a-multi-disciplinary-approach.md) Data Science and Big Data Analytics Prompt Generator
    3. Human-Computer Interaction.
       - [prompt 105](prompt/105-expert-panel-synthesis-with-authority-regularization.md) Expert Panel Synthesis with Authority Regularization
    4. Software Engineering.
       - [prompt 26](prompt/026-code-performancer.md) Code performancer
       - [prompt 27](prompt/027-powershell-s-code-troubleshooter.md) Powershell's code troubleshooter
       - [prompt 31](prompt/031-powershell-problem-solver.md) Powershell Problem Solver
       - [prompt 32](prompt/032-analyze-and-improve-powershell-code.md) Analyze and improve PowerShell code
       - [prompt 35](prompt/035-analyze-and-improve-parts-of-long-powershell-code.md) Analyze and improve parts of long PowerShell
       - [prompt 38](prompt/038-powershell-code-optimization-and-best-practices.md) PowerShell Code Optimization and Best Practices
       - [prompt 41](prompt/041-powershellgpt-wizard.md) PowerShellGPT Wizard
       - [prompt 47](prompt/047-powershell-adds-course.md) Powershell ADDS course
       - [prompt 50](prompt/050-psdeveloper.md) PSDeveloper
       - [prompt 54](prompt/054-powershell-pester-helper.md) Powershell Pester Helper
       - [prompt 66](prompt/066-roleplay-discussion.md) Roleplay-discussion
       - [prompt 70](prompt/070-codegpt-three-experts.md) CodeGPT - Three experts
       - [prompt 79](prompt/079-code-refactoring.md) Code refactoring
       - [prompt 88](prompt/088-building-better-together-a-guide-to-ai-powered-product-copilot-development.md) Building Better Together: A Guide to AI-Powered Product Copilot Development
       - [prompt 106](prompt/106-optimization-algorithm-simulation.md) Optimization Algorithm Simulation
       - [prompt 136](prompt/136-code-analyzer-powershell.md) Code Analyzer - Powershell
       - [prompt 137](prompt/137-code-functional-report.md) Code functional Report
       - [prompt 148](prompt/148-systematic-debugging.md) Systematic Debugging: Identifying Root Causes Through Reflective Analysis and Targeted Logging
       - [prompt 153](prompt/153-intent-driven-specs-alignment-response-generator.md) Intent-Driven Specs & Alignment Response Generator
       - [prompt 155](prompt/155-change-communication-pack-release-notes-rollout-support-playbook.md) Change Communication Pack: Release Notes, Rollout Plan, and Support Playbook
    5. Computer Systems and Networks.
       - [prompt 53](prompt/053-powershell-script-analysis-and-commenting-guidelines.md) PowerShell Script Analysis and Commenting Guidelines
    6. Cybersecurity and Information Assurance.
       - [prompt 20](prompt/020-security-examine-code.md) Security examine code
       - [prompt 25](prompt/025-powershield.md) PowerShield
       - [prompt 39](prompt/039-secure-powershell-code-analysis-and-improvement.md) Secure PowerShell Code Analysis and Improvement
       - [prompt 52](prompt/052-it-administrator-assistant.md) IT Administrator' Assistant
       - [prompt 54](prompt/054-powershell-pester-helper.md) Powershell Pester Helper
       - [prompt 105](prompt/105-expert-panel-synthesis-with-authority-regularization.md) Expert Panel Synthesis with Authority Regularization
       - [prompt 106](prompt/106-optimization-algorithm-simulation.md) Optimization Algorithm Simulation
       - [prompt 113](prompt/113-adversarial-robustness-evaluation-prompt.md) Adversarial Robustness Evaluation Prompt
       - [prompt 131](prompt/131-privacy-conscious-oov-discovery-for-language-model-enhancement.md) Privacy-Conscious OOV Discovery for Language Model Enhancement
    7. Database Management and Data Retrieval:
        1. Relational Database Design and Optimization.
        2. NoSQL Databases and Data Stores.
        3. Data Warehousing and Business Intelligence.
        4. Distributed Database Systems.
        5. Database Administration and Security.
        6. Data Mining and Knowledge Discovery.
           - [prompt 63](prompt/063-keyphrase-expansion-clustering-assistant.md) Keyphrase Expansion Clustering Assistant
           - [prompt 71](prompt/071-olmo.md) OLMo
           - [prompt 84](prompt/084-beyond-pairwise-optimizing-conversational-ai-using-listwise-preference-optimization.md) Beyond Pairwise: Optimizing Conversational AI using Listwise Preference Optimization
           - [prompt 98](prompt/098-keyphrase-catalyst-extracting-intent-through-chain-of-thought.md) Keyphrase Catalyst: Extracting Intent Through Chain of Thought
           - [prompt 103](prompt/103-unraveling-complexities-logical-reasoning-on-knowledge-graphs.md) Unraveling Complexities: Logical Reasoning on Knowledge Graphs
           - [prompt 112](prompt/112-cross-domain-application-of-machine-learning-and-bootstrap-techniques.md) Cross-Domain Application of Machine Learning and Bootstrap Techniques
           - [prompt 123](prompt/123-vector-field-analysis-and-cyclone-tracking.md) Vector Field Analysis and Cyclone Tracking
           - [prompt 129](prompt/129-understanding-individual-fairest-community-search-in-hins.md) Understanding Individual Fairest Community Search in HINs
           - [prompt 134](prompt/134-neural-model-interpretability-exploration-guide.md) Neural Model Interpretability Exploration Guide
           - [prompt 142](prompt/142-summarize-with-metrics.md) Summarize with metrics
        7. Database Query Languages (e.g., SQL, SPARQL).
           - [prompt 49](prompt/049-kqlsenbot.md) KQLSenBot
        8. Data Modeling and Metadata Management.
        9. Database Performance Tuning.
        10. Data Governance and Compliance.
        11. Database Scalability and High Availability.
        12. In-Memory Databases.
        13. Graph Databases and Networked Data.
        14. Object-Oriented and Object-Relational Databases.
        15. XML and Semi-Structured Data Management.
        16. Data Integration, ETL, and Data Quality.
            - [prompt 84](prompt/084-beyond-pairwise-optimizing-conversational-ai-using-listwise-preference-optimization.md) Beyond Pairwise: Optimizing Conversational AI using Listwise Preference Optimization
        17. Database Theory and Foundations.
        18. Temporal, Spatial, and Multimedia Databases.
        19. Big Data Storage and Processing.
        20. Data Privacy and Anonymization.
            - [prompt 131](prompt/131-privacy-conscious-oov-discovery-for-language-model-enhancement.md) Privacy-Conscious OOV Discovery for Language Model Enhancement
            - [prompt 133](prompt/133-dptraj-pm-implementation-and-analysis-guide.md) DPTraj-PM Implementation and Analysis Guide
        21. Other Specialized Areas in Database Management and Data Retrieval.
            - [prompt 29](prompt/029-examples-of-operations-in-powershell-where-using-net-classes-is-more-efficient-than-using-built-in-cmdlets.md) Examples of operations in PowerShell where using .NET classes is more efficient than using built-in cmdlets
            - [prompt 62](prompt/062-adaptive-interactive-logic-prompt-ailp.md) Adaptive Interactive Logic Prompt (AILP)
            - [prompt 123](prompt/123-vector-field-analysis-and-cyclone-tracking.md) Vector Field Analysis and Cyclone Tracking
    8. Theoretical Computer Science
       - [prompt 57](prompt/057-lark-prompt.md) LARK Prompt
       - [prompt 99](prompt/099-crafting-solutions-a-user-centric-approach-to-problem-solving.md) Crafting Solutions: A User-Centric Approach to Problem-Solving
       - [prompt 129](prompt/129-understanding-individual-fairest-community-search-in-hins.md) Understanding Individual Fairest Community Search in HINs
       - [prompt 134](prompt/134-neural-model-interpretability-exploration-guide.md) Neural Model Interpretability Exploration Guide
    9. Computer Graphics and Visualization
    10. Robotics and Automation
        - [prompt 91](prompt/091-unlocking-potential-exploring-the-role-and-functions-of-social-robots-in-education.md) Unlocking Potential: Exploring the Role and Functions of Social Robots in Education
        - [prompt 120](prompt/120-actionsense-insight-generator.md)
        - [prompt 122](prompt/122-robotic-recovery-plan-generation-prompt.md) Robotic Recovery Plan Generation Prompt
        - [prompt 132](prompt/132-comprehensive-collaborative-perception-dataset-analysis.md) Comprehensive Collaborative Perception Dataset Analysis
    11. Bioinformatics and Computational Biology
    12. Quantum Computing
        - [prompt 42](prompt/042-optimo.md) Optimo
    13. Information Systems
        - [prompt 16](prompt/016-prompt-generation-robot.md) Prompt generation robot
        - [prompt 28](prompt/028-diverse-code-generation-task-instructions-for-powershell.md)
        - [prompt 32](prompt/032-analyze-and-improve-powershell-code.md) Analyze and improve PowerShell codeDiverse code generation task instructions for PowerShell
        - [prompt 35](prompt/035-analyze-and-improve-parts-of-long-powershell-code.md) Analyze and improve parts of long PowerShell
        - [prompt 41](prompt/041-powershellgpt-wizard.md) PowerShellGPT Wizard
        - [prompt 45](prompt/045-taskcraftopia.md) TaskCraftopia
        - [prompt 52](prompt/052-it-administrator-assistant.md) IT Administrator' Assistant
        - [prompt 54](prompt/054-powershell-pester-helper.md) Powershell Pester Helper
        - [prompt 71](prompt/071-olmo.md) OLMo
        - [prompt 75](prompt/075-maximizing-the-power-of-large-language-models-a-comprehensive-guide-for-beginners-and-experts.md) Maximizing the Power of Large Language Models: A Comprehensive Guide for Beginners and Experts
        - [prompt 95](prompt/095-bookworm-buddy-your-online-bookstore-chatbot-assistant.md) Bookworm Buddy: Your Online Bookstore Chatbot Assistant
        - [prompt 97](prompt/097-balancing-accuracy-and-density-mastering-the-task-spectrum.md) Balancing Accuracy and Density: Mastering the Task Spectrum
    14. Educational Technology
        - [prompt 40](prompt/040-powerpoint-gpt-assistant.md) PowerPoint GPT assistant
    15. Computer Game Design and Development
    16. Web and Internet Computing
    17. Programming Languages and Compilers
        - [prompt 137](prompt/137-code-functional-report.md) Code functional Report
    18. Digital Libraries and Archives
    19. Multimedia Computing
    20. Mobile and Ubiquitous Computing
         - [prompt 132](prompt/132-comprehensive-collaborative-perception-dataset-analysis.md) Comprehensive Collaborative Perception Dataset Analysis
    21. Cloud Computing and Virtualization
         - [prompt 127](prompt/127-ascending-auction-analysis-and-application.md) Ascending Auction Analysis and Application
    22. Computer Architecture and Engineering
    23. High-Performance Computing
    24. Computer Ethics and Professional Practice
        - [prompt 35](prompt/035-analyze-and-improve-parts-of-long-powershell-code.md) Analyze and improve parts of long PowerShell
        - [prompt 71](prompt/071-olmo.md) OLMo
        - [prompt 88](prompt/088-building-better-together-a-guide-to-ai-powered-product-copilot-development.md) Building Better Together: A Guide to AI-Powered Product Copilot Development
        - [prompt 153](prompt/153-intent-driven-specs-alignment-response-generator.md) Intent-Driven Specs & Alignment Response Generator
    25. Innovation and Technology Management.
        - [prompt 50](prompt/050-psdeveloper.md) PSDeveloper
        - [prompt 52](prompt/052-it-administrator-assistant.md) IT Administrator' Assistant
        - [prompt 53](prompt/053-powershell-script-analysis-and-commenting-guidelines.md) PowerShell Script Analysis and Commenting Guidelines
        - [prompt 65](prompt/065-dynamic-expertise-activation-prompt-deap.md) Dynamic Expertise Activation Prompt (DEAP)
        - [prompt 71](prompt/071-olmo.md) OLMo
        - [prompt 84](prompt/084-beyond-pairwise-optimizing-conversational-ai-using-listwise-preference-optimization.md) Beyond Pairwise: Optimizing Conversational AI using Listwise Preference Optimization
        - [prompt 113](prompt/113-adversarial-robustness-evaluation-prompt.md) Adversarial Robustness Evaluation Prompt
        - [prompt 122](prompt/122-robotic-recovery-plan-generation-prompt.md) Robotic Recovery Plan Generation Prompt
        - [prompt 132](prompt/132-comprehensive-collaborative-perception-dataset-analysis.md) Comprehensive Collaborative Perception Dataset Analysis
        - [prompt 135](prompt/135-mathematical-reasoning-model-evaluator-mrme.md) Mathematical Reasoning Model Evaluator (MRME)
    26. Other Specialized Areas in Computer and Information Sciences.
        - [prompt 32](prompt/032-analyze-and-improve-powershell-code.md) Analyze and improve PowerShell code
        - [prompt 42](prompt/042-optimo.md) Optimo
        - [prompt 44](prompt/044-turbocodeai.md) TurboCodeAI
        - [prompt 45](prompt/045-taskcraftopia.md) TaskCraftopia
        - [prompt 64](prompt/064-dual-category-task-optimizer-dcto-prompt.md) Dual-Category Task Optimizer (DCTO) Prompt
        - [prompt 96](prompt/096-understanding-your-needs-analyzing-user-requests-with-mops.md) Understanding Your Needs: Analyzing User Requests with MoPs
        - [prompt 114](prompt/114-cross-domain-ai-resilient-test-analysis.md) Cross-Domain AI-Resilient Test Analysis
        - [prompt 131](prompt/131-privacy-conscious-oov-discovery-for-language-model-enhancement.md) Privacy-Conscious OOV Discovery for Language Model Enhancement
        - [prompt 133](prompt/133-dptraj-pm-implementation-and-analysis-guide.md) DPTraj-PM Implementation and Analysis Guide
        - [prompt 137](prompt/137-code-functional-report.md) Code functional Report
        - [prompt 138](prompt/138-log-analyzer.md) Log analyzer
        - [prompt 142](prompt/142-summarize-with-metrics.md) Summarize with metrics
6. Earth and Environmental Sciences.
   - [prompt 106](prompt/106-optimization-algorithm-simulation.md) Optimization Algorithm Simulation
   - [prompt 123](prompt/123-vector-field-analysis-and-cyclone-tracking.md) Vector Field Analysis and Cyclone Tracking
7. Education:
   1. Educational Psychology and Learning Theories.
         - [prompt 60](prompt/060-instructadapt.md) INSTRUCTADAPT
         - [prompt 93](prompt/093-unpacking-the-layers-transforming-statements-into-insightful-questions-and-answers.md) Unpacking the Layers: Transforming Statements into Insightful Questions and Answers
   2. Curriculum Development and Instructional Design.
         - [prompt 43](prompt/043-coursecraftopia.md) CourseCraftopia
         - [prompt 47](prompt/047-powershell-adds-course.md) Powershell ADDS course
         - [prompt 60](prompt/060-instructadapt.md) INSTRUCTADAPT
         - [prompt 61](prompt/061-claritychain.md) ClarityChain
         - [prompt 89](prompt/089-unlocking-innovation-supercharge-your-problem-solving-with-supermind-design.md) Unlocking Innovation: Supercharge Your Problem-Solving with Supermind Design
         - [prompt 90](prompt/090-craft-your-thesis-ai-assistant-for-argumentative-essay-writing.md) Craft Your Thesis: AI Assistant for Argumentative Essay Writing
         - [prompt 99](prompt/099-crafting-solutions-a-user-centric-approach-to-problem-solving.md) Crafting Solutions: A User-Centric Approach to Problem-Solving
         - [prompt 100](prompt/100-guiding-the-user-crafting-clear-and-contextual-instructions.md) Guiding the User: Crafting Clear and Contextual Instructions
   3. Educational Technology and Digital Learning.
         - [prompt 55](prompt/055-promptperfector.md) PromptPerfector
         - [prompt 60](prompt/060-instructadapt.md) INSTRUCTADAPT
         - [prompt 65](prompt/065-dynamic-expertise-activation-prompt-deap.md) Dynamic Expertise Activation Prompt (DEAP)
         - [prompt 75](prompt/075-maximizing-the-power-of-large-language-models-a-comprehensive-guide-for-beginners-and-experts.md) Maximizing the Power of Large Language Models: A Comprehensive Guide for Beginners and Experts
         - [prompt 91](prompt/091-unlocking-potential-exploring-the-role-and-functions-of-social-robots-in-education.md) Unlocking Potential: Exploring the Role and Functions of Social Robots in Education
         - [prompt 99](prompt/099-crafting-solutions-a-user-centric-approach-to-problem-solving.md) Crafting Solutions: A User-Centric Approach to Problem-Solving
         - [prompt 113](prompt/113-adversarial-robustness-evaluation-prompt.md) Adversarial Robustness Evaluation Prompt
   4. Teaching Methods and Pedagogy.
         - [prompt 156](prompt/156-master-educator-mental-model-selection.md) Master Educator: Mental Model Selection
         - [prompt 157](prompt/157-misconceptions-map-and-refute.md) Misconceptions: Map and Refute
         - [prompt 158](prompt/158-personalized-learning-roadmap-three-paths.md) Personalized Learning Roadmap (Three Paths)
         - [prompt 159](prompt/159-pareto-mastering-topic.md) Pareto Mastery Plan (80/20)
         - [prompt 160](prompt/160-compare-concepts-with-venn.md) Compare Two Concepts (Frameworks + Venn)
         - [prompt 161](prompt/161-prerequisite-gap-diagnosis.md) Prerequisite Gap Diagnosis (Backward Chaining)
         - [prompt 162](prompt/162-teach-by-negative-space.md) Teach by Negative Space (“What It’s Not”)
         - [prompt 163](prompt/163-create-and-evaluate-analogies.md) Create and Evaluate Analogies
         - [prompt 164](prompt/164-expert-perspectives-probing-questions.md) Expert Perspectives: Probing Questions
         - [prompt 165](prompt/165-simplify-for-8th-grader-choose-style.md) Simplify for an 8th Grader (Choose a Style)
         - [prompt 166](prompt/166-pareto-resource-curator.md) Pareto Resource Curator (80% Understanding Fast)
   5. Assessment and Evaluation in Education.
   6. Special Education and Inclusive Practices.
   7. Higher Education Administration and Policy.
      - [prompt 113](prompt/113-adversarial-robustness-evaluation-prompt.md) Adversarial Robustness Evaluation Prompt
   8. Early Childhood Education.
   9. Adult Education and Lifelong Learning.
   10. Educational Leadership and Management.
       - [prompt 91](prompt/091-unlocking-potential-exploring-the-role-and-functions-of-social-robots-in-education.md) Unlocking Potential: Exploring the Role and Functions of Social Robots in Education
   11. Multicultural Education and Diversity in Learning.
   12. Language Education and Linguistics in Education.
   13. Educational Research Methods and Statistics.
       - [prompt 114](prompt/114-cross-domain-ai-resilient-test-analysis.md) Cross-Domain AI-Resilient Test Analysis
       - [prompt 125](prompt/125-structural-causal-inquiry.md) Structural Causal Inquiry
       - [prompt 128](prompt/128-academic-paper-structure-comprehension-and-model-enhancement.md) Academic Paper Structure Comprehension and Model Enhancement
   14. Education Law and Policy.
   15. International and Comparative Education.
   16. STEM Education (Science, Technology, Engineering, and Mathematics).
       - [prompt 91](prompt/091-unlocking-potential-exploring-the-role-and-functions-of-social-robots-in-education.md) Unlocking Potential: Exploring the Role and Functions of Social Robots in Education
   17. Arts Education and Creativity in Learning.
       - [prompt 91](prompt/091-unlocking-potential-exploring-the-role-and-functions-of-social-robots-in-education.md) Unlocking Potential: Exploring the Role and Functions of Social Robots in Education
   18. Health Education and Wellness Promotion.
   19. Environmental Education and Sustainability.
   20. Career and Technical Education.
   21. Education for Sustainable Development.
   22. Online and Distance Learning.
         - [prompt 43](prompt/043-coursecraftopia.md) CourseCraftopia
         - [prompt 47](prompt/047-powershell-adds-course.md) Powershell ADDS course
         - [prompt 127](prompt/127-ascending-auction-analysis-and-application.md) Ascending Auction Analysis and Application
   23. Social and Emotional Learning.
   24. Critical Pedagogy and Education for Social Justice.
   25. Other Specialized Areas in Education.
         - [prompt 64](prompt/064-dual-category-task-optimizer-dcto-prompt.md) Dual-Category Task Optimizer (DCTO) Prompt
         - [prompt 125](prompt/125-structural-causal-inquiry.md) Structural Causal Inquiry
8. Engineering and Technology.
   - [prompt 58](prompt/058-iterative-optimization-prompting-iop.md) Iterative Optimization Prompting (IOP)
   - [prompt 104](prompt/104-adaptive-requirements-exploration-prompt.md) Adaptive Requirements Exploration Prompt
   - [prompt 110](prompt/110-blockchain-efficiency-dynamic-transaction-storage-and-verkle-tree-strategies.md) Blockchain Efficiency: Dynamic Transaction Storage and Verkle Tree Strategies
   - [prompt 119](prompt/119-iterative-refinement-application-guide-for-linear-systems.md)
   - [prompt 120](prompt/120-actionsense-insight-generator.md)
   - [prompt 122](prompt/122-robotic-recovery-plan-generation-prompt.md) Robotic Recovery Plan Generation Prompt
   - [prompt 123](prompt/123-vector-field-analysis-and-cyclone-tracking.md) Vector Field Analysis and Cyclone Tracking
9. Health and Medicine.
10. Law and Legal Studies.
    - [prompt 105](prompt/105-expert-panel-synthesis-with-authority-regularization.md) Expert Panel Synthesis with Authority Regularization
11. Mathematics.
    - [prompt 83](prompt/083-mastering-multi-step-word-problems-breakdown-and-solution-with-clear-explanations.md) Mastering Multi-Step Word Problems: Breakdown and Solution with Clear Explanations
    - [prompt 112](prompt/112-cross-domain-application-of-machine-learning-and-bootstrap-techniques.md) Cross-Domain Application of Machine Learning and Bootstrap Techniques
    - [prompt 119](prompt/119-iterative-refinement-application-guide-for-linear-systems.md) Iterative Refinement Application Guide for Linear Systems
    - [prompt 135](prompt/135-mathematical-reasoning-model-evaluator-mrme.md) Mathematical Reasoning Model Evaluator (MRME)
    - [prompt 146](prompt/146-mathematical-proof-construction.md) Advanced Mathematical Concepts in Machine Learning
12. Physical Sciences.
    - [prompt 92](prompt/092-stepping-up-to-the-challenge-categorization-and-problem-solving-with-clear-reasoning.md) Stepping Up to the Challenge: Categorization and Problem Solving with Clear Reasoning
    - [prompt 124](prompt/124-mechanism-analysis.md) Mechanism Analysis
13. Social Sciences.
    - [prompt 73](prompt/073-beyond-humanity.md) Beyond Humanity
    - [prompt 124](prompt/124-mechanism-analysis.md) Mechanism Analysis
    - [prompt 125](prompt/125-structural-causal-inquiry.md) Structural Causal Inquiry
    - [prompt 127](prompt/127-ascending-auction-analysis-and-application.md) Ascending Auction Analysis and Application
14. Life Sciences.
    - [prompt 92](prompt/092-stepping-up-to-the-challenge-categorization-and-problem-solving-with-clear-reasoning.md) Stepping Up to the Challenge: Categorization and Problem Solving with Clear Reasoning
15. Philosophy and Ethics.
    1. Responsible AI practices and ethical use of language models.
       - [prompt 71](prompt/071-olmo.md) OLMo
       - [prompt 73](prompt/073-beyond-humanity.md) Beyond Humanity
       - [prompt 75](prompt/075-maximizing-the-power-of-large-language-models-a-comprehensive-guide-for-beginners-and-experts.md) Maximizing the Power of Large Language Models: A Comprehensive Guide for Beginners and Experts
       - [prompt 77](prompt/077-decoding-fairness-exploring-ai-decision-making-in-the-dictator-game.md) Decoding Fairness: Exploring AI Decision-Making in the Dictator Game
       - [prompt 82](prompt/082-the-reasoning-chain-verifier-deep-dive-into-evidence-and-logic.md) The Reasoning Chain Verifier: Deep Dive into Evidence and Logic
       - [prompt 89](prompt/089-unlocking-innovation-supercharge-your-problem-solving-with-supermind-design.md) Unlocking Innovation: Supercharge Your Problem-Solving with Supermind Design
       - [prompt 99](prompt/099-crafting-solutions-a-user-centric-approach-to-problem-solving.md) Crafting Solutions: A User-Centric Approach to Problem-Solving
       - [prompt 113](prompt/113-adversarial-robustness-evaluation-prompt.md) Adversarial Robustness Evaluation Prompt
       - [prompt 116](prompt/116-crafting-conversion-driven-marketing-copy.md) Crafting Conversion-Driven Marketing Copy
    2. Other Specialized Areas in Philosophy and Ethics.
16. Physics.
17. Political Science and International Relations.
    - [prompt 110](prompt/110-blockchain-efficiency-dynamic-transaction-storage-and-verkle-tree-strategies.md) Blockchain Efficiency: Dynamic Transaction Storage and Verkle Tree Strategies
    - [prompt 127](prompt/127-ascending-auction-analysis-and-application.md) Ascending Auction Analysis and Application
18. Psychology and Cognitive Sciences.
    1. Critical Thinking and Analysis.
       - [prompt 71](prompt/071-olmo.md) OLMo
       - [prompt 90](prompt/090-craft-your-thesis-ai-assistant-for-argumentative-essay-writing.md) Craft Your Thesis: AI Assistant for Argumentative Essay Writing
    2. Logic and Reasoning
       - [prompt 67](prompt/067-veryfier.md) Veryfier
    3. Other Specialized Areas in Psychology and Cognitive Sciences.
       - [prompt 73](prompt/073-beyond-humanity.md) Beyond Humanity
       - [prompt 87](prompt/087-the-ai-spark-exploring-the-impact-of-ai-on-human-creativity-and-diversity.md) The AI Spark: Exploring the Impact of AI on Human Creativity and Diversity
       - [prompt 144](prompt/144-sentiment-classification-prompt-addressing-sarcasm-and-irony.md) Sentiment Classification Prompt: Addressing Sarcasm and Irony
19. Cultural and Area Studies.
20. Linguistics and Language Studies.
    - [prompt 30](prompt/030-dyktando.md) Dyktando (polish)
21. Literature.
22. Music and Performing Arts.
23. Religion and Theology.
24. Visual Arts and Film Studies.
25. Entertainment.
    - [prompt 46](prompt/046-game-lost-in-the-enchanted-forest.md) Game "Lost in the Enchanted Forest"
    - [prompt 48](prompt/048-formula-1-game.md) Formula 1 game
    - [prompt 51](prompt/051-chess.md) Chess
26. General Templates or Frameworks:
    1. Problem-Solving and Optimization Templates.
       - [prompt 102](prompt/102-optimizing-through-iteration-learning-from-past-solutions.md) Optimizing Through Iteration: Learning from Past Solutions
       - [prompt 106](prompt/106-optimization-algorithm-simulation.md) Optimization Algorithm Simulation
       - [prompt 108](prompt/108-co-create-spectrum-a-value-driven-brainstorming-prompt.md) Co-Create Spectrum: A Value-Driven Brainstorming Prompt
       - [prompt 109](prompt/109-adaptive-learning-assistant.md) Adaptive Learning Assistant
       - [prompt 112](prompt/112-cross-domain-application-of-machine-learning-and-bootstrap-techniques.md) Cross-Domain Application of Machine Learning and Bootstrap Techniques
       - [prompt 130](prompt/130-strategic-reasoning-via-predictive-planning.md) Strategic Reasoning via Predictive Planning
       - [prompt 139](prompt/139-simple-prompt-creator.md) Simple prompt creator
       - [prompt 141](prompt/141-summariza-to-200-words.md) Summariza to 200 words
    2. Project Management Frameworks.
    3. Instructional Design and Educational Frameworks.
       - [prompt 109](prompt/109-adaptive-learning-assistant.md) Adaptive Learning Assistant
    4. Strategic Planning and Analysis Templates.
       - [prompt 105](prompt/105-expert-panel-synthesis-with-authority-regularization.md) Expert Panel Synthesis with Authority Regularization
       - [prompt 108](prompt/108-co-create-spectrum-a-value-driven-brainstorming-prompt.md) Co-Create Spectrum: A Value-Driven Brainstorming Prompt
       - [prompt 139](prompt/139-simple-prompt-creator.md) Simple prompt creator
    5. Research Methodology and Experimental Design Templates.
       - [prompt 107](prompt/107-scholarly-synthesis.md) Scholarly Synthesis
       - [prompt 112](prompt/112-cross-domain-application-of-machine-learning-and-bootstrap-techniques.md) Cross-Domain Application of Machine Learning and Bootstrap Techniques
       - [prompt 128](prompt/128-academic-paper-structure-comprehension-and-model-enhancement.md) Academic Paper Structure Comprehension and Model Enhancement
       - [prompt 143](prompt/143-expert-techniques-for-solving-complex-problems-a-multi-disciplinary-approach.md) Data Science and Big Data Analytics Prompt Generator
    6. Creative and Ideation Frameworks.
       - [prompt 108](prompt/108-co-create-spectrum-a-value-driven-brainstorming-prompt.md) Co-Create Spectrum: A Value-Driven Brainstorming Prompt
       - [prompt 124](prompt/124-mechanism-analysis.md) Mechanism Analysis
       - [prompt 139](prompt/139-simple-prompt-creator.md) Simple prompt creator
       - [prompt 151](prompt/151-mega-meta-prompt-curiosity-open-loop-engine.md) Curiosity Open-Loop Engine
    7. Decision-Making and Analysis Templates.
       - [prompt 108](prompt/108-co-create-spectrum-a-value-driven-brainstorming-prompt.md) Co-Create Spectrum: A Value-Driven Brainstorming Prompt
       - [prompt 109](prompt/109-adaptive-learning-assistant.md) Adaptive Learning Assistant
       - [prompt 123](prompt/123-vector-field-analysis-and-cyclone-tracking.md) Vector Field Analysis and Cyclone Tracking
       - [prompt 139](prompt/139-simple-prompt-creator.md) Simple prompt creator
    8. Other Specialized Templates or Frameworks.
       - [prompt 150](prompt/150-topic-transforming.md) Topic transforming.
27. Other.
    - [prompt 19](prompt/019-luna.md) Luna
    - [prompt 22](prompt/022-stoned-surfer-bro.md) Stoned surfer bro
    - [prompt 23](prompt/023-witcher.md) Witcher
    - [prompt 33](prompt/033-king-of-prompts-chatgpt-prompt-generator.md) King Of Prompts - Chatgpt Prompt Generator
    - [prompt 34](prompt/034-god-of-prompts-chatgpt-prompt-generator.md) God Of Prompts - Chatgpt Prompt Generator
    - [prompt 37](prompt/037-crafting-an-effective-nlp-prompt.md) Crafting an Effective NLP Prompt
    - [prompt 56](prompt/056-nicegpt.md) NiceGPT

<details>
<summary>Prompt's classification (old)</Summary>

1. **Content Expansion and Strategy:**
   - [Prompt 1](prompt/001-keywords-for-topic.md): Create a list of 10 keywords related to a given topic to expand content strategy for a new business website.
   - [Prompt 50](prompt/050-psdeveloper.md): PSDeveloper. Invent new aspect of provided product' (programming related) description.

2. **Explanation and Definition:**
   - [Prompt 2](prompt/002-asking-chatgpt-to-explain-a-concept-or-idea-can-be-valuable-in-gaining-a-deeper-understanding-of-a-particular-topic.md): Ask ChatGPT to explain a concept or idea.
   - [Prompt 3](prompt/003-requesting-a-definition-from-chatgpt-can-help-clarify-the-meaning-of-a-word-or-concept-and-provide-a-solid-foundation-for-further-exploration.md): Request ChatGPT to define a word or concept.

3. **Comparison and Analysis:**
   - [Prompt 4](prompt/004-asking-chatgpt-to-compare-two-or-more-things-can-be-useful-in-understanding-the-similarities-and-differences-between-them.md): Ask ChatGPT to compare two or more things.
   - [Prompt 5](prompt/005-requesting-an-analysis-from-chatgpt-can-help-break-down-a-complex-idea-or-situation-into-its-component-parts-for-better-understanding.md): Request ChatGPT to analyze a complex idea or situation.

4. **Prediction and Evaluation:**
   - [Prompt 6](prompt/006-asking-chatgpt-to-predict-future-outcomes-based-on-available-data-or-trends-can-provide-valuable-insights-for-decision-making.md): Ask ChatGPT to predict future outcomes based on data or trends.
   - [Prompt 7](prompt/007-requesting-an-evaluation-from-chatgpt-can-help-assess-the-effectiveness-or-value-of-a-particular-approach-or-strategy.md): Request ChatGPT to evaluate the effectiveness of an approach or strategy.

5. **Recommendation and Simplification:**
   - [Prompt 8](prompt/008-asking-chatgpt-to-recommend-a-course-of-action-or-solution-can-be-useful-in-addressing-a-particular-problem-or-challenge.md): Ask ChatGPT to recommend a course of action or solution.
   - [Prompt 9](prompt/009-requesting-that-chatgpt-simplify-a-complex-topic-or-idea-can-be-helpful-in-gaining-a-basic-understanding-before-delving-deeper.md): Request ChatGPT to simplify a complex topic or idea.

6. **Interpretation and Exploration:**
   - [Prompt 10](prompt/010-asking-chatgpt-to-interpret-a-particular-text-or-data-set-can-help-uncover-hidden-meanings-or-insights.md): Ask ChatGPT to interpret a text or data set.
   - [Prompt 11](prompt/011-requesting-that-chatgpt-explore-a-particular-topic-or-idea-can-be-valuable-in-discovering-new-perspectives-or-avenues-for-inquiry.md): Request ChatGPT to explore a particular topic or idea.
   - [Prompt 56](prompt/056-nicegpt.md): NiceGPT

7. **Teaching and Role-Playing:**
   - [Prompt 12](prompt/012-teach-me.md): Teach about a specific topic in simple terms.
   - [Prompt 13](prompt/013-albert-einstein.md): Act as Albert Einstein or other characters to explain a topic.

8. **Guide and Instructions:**
   - [Prompt 14](prompt/014-guide-of-topic.md): Generate a comprehensive guide on a topic, including accuracy and web sources.
   - [Prompt 24](prompt/024-build-a-prompt.md): Build a prompt to generate content about a specific product or service.

9. **Regex Generator and Code Generation:**
   - [Prompt 15](prompt/015-regex-generator.md): Generate regular expressions for specific patterns in text.
   - [Prompt 28](prompt/028-diverse-code-generation-task-instructions-for-powershell.md): Propose diverse code generation task instructions for PowerShell.
   - [Prompt 41](prompt/041-powershellgpt-wizard.md): PowerShellGPT Wizard

10. **Programming Related Tasks and Analysis:**
    - [Prompt 20](prompt/020-security-examine-code.md): Examine and secure PowerShell code against potential security flaws.
    - [Prompt 27](prompt/027-powershell-s-code-troubleshooter.md): Analyze and troubleshoot PowerShell code.
    - [Prompt 35](prompt/035-analyze-and-improve-parts-of-long-powershell-code.md): Analyze and improve parts of PowerShell code.
    - [Prompt 38](prompt/038-powershell-code-optimization-and-best-practices.md): PowerShell Code Optimization and Best Practices
    - [Prompt 39](prompt/039-secure-powershell-code-analysis-and-improvement.md): Secure PowerShell Code Analysis and Improvement
    - [Prompt 44](prompt/044-turbocodeai.md): Turbo Code AI
    - [prompt 53](prompt/053-powershell-script-analysis-and-commenting-guidelines.md): Powershell script analysis and commenting guidelines
    - [Prompt 54](prompt/054-powershell-pester-helper.md): PowerShell Pester Helper

11. **Role-Playing and Persona Interaction:**
    - [Prompt 19](prompt/019-luna.md): Role-play as Luna, a coding assistant, following the Luna Ruleset.
    - [Prompt 22](prompt/022-stoned-surfer-bro.md): Explain a topic as a stoned surfer bro or Witcher.

12. **Specific Coding Questions and Assistance:**
    - [Prompt 21](prompt/021-developergpt.md): Act as DeveloperGPT, providing coding answers and examples.
    - [Prompt 25](prompt/025-powershield.md): Provide best practices for secure PowerShell coding.
    - [prompt 47](prompt/047-powershell-adds-course.md): Powershell AD course

13. **Optimization and Performance Improvement:**
    - [Prompt 26](prompt/026-code-performancer.md): Optimize PowerShell code for better performance.
    - [Prompt 31](prompt/031-powershell-problem-solver.md): Powershell Problem Solver
    - [Prompt 32](prompt/032-analyze-and-improve-powershell-code.md): Analyze and improve PowerShell code

14. **Examples and Use Cases:**
    - [Prompt 29](prompt/029-examples-of-operations-in-powershell-where-using-net-classes-is-more-efficient-than-using-built-in-cmdlets.md): Provide examples of operations in PowerShell where .NET classes are more efficient than built-in cmdlets.

15. **Prompt Engineering**
    - [Prompt 33](prompt/033-king-of-prompts-chatgpt-prompt-generator.md): King of prompts - chatGPT prompt generator
    - [Prompt 34](prompt/034-god-of-prompts-chatgpt-prompt-generator.md): God of prompts - chatGPT prompt generator
    - [Prompt 37](prompt/037-crafting-an-effective-nlp-prompt.md): Crafting prompt
    - [Prompt 55](prompt/055-promptperfector.md): PromptPerfector
    - [Prompt 149](prompt/149-self-guided-exploration.md) Prompt-and-Answer - Self-Guided Exploration

16. **Classification**
    - [Prompt 36](prompt/036-classification.md): Prompt classificator

</details>

These prompts cover a wide range of tasks, from content creation to code generation, role-playing, and specific programming-related questions. Each prompt serves a different purpose, catering to various user needs.

## 9. Prompts

All prompt bodies have been moved into individual files under `prompt/` (one prompt per file).

Use the "Prompt's classification" section above to browse prompts by category; each entry links directly to the corresponding file.


## 10. Useful Links

1. [6 Useful AI Tools](https://www.instagram.com/reel/CoFh1jLqq8I/)
2. [Prompt Tools](https://www.instagram.com/reel/CqOCKsDMNa5/)
3. [Learn Prompting](https://learnprompting.org/)
4. [150+ Best ChatGPT Prompts for All Kinds of Workflow](https://beebom.com/best-chatgpt-prompts/amp/)
5. [120 Best ChatGPT Prompts for Every Type of Work](https://www.greataiprompts.com/chat-gpt/best-chat-gpt-prompts/)
6. [100 Best ChatGPT Prompts to Unleash AI’s Potential](https://mpost.io/100-best-chatgpt-prompts-to-unleash-ais-potential/)
7. [215+ ChatGPT Prompts You Can’t Miss to Try Out in 2023](https://writesonic.com/blog/chatgpt-prompts/)
8. <https://www.instagram.com/p/Crgob97JRqk/>
9. <https://www.instagram.com/p/CriGOz3oWAA/>
10. Search Chat <https://flowgpt.com/>
11. Top 12 CHAT GPT Prompts to Use in 2023 <https://www.linkedin.com/pulse/top-12-chat-gpt-prompts-use-2023-mary-vista>
12. Best GPT-3 Prompts <https://promptbase.com/gpt3>
13. 70+ ChatGPT Prompts for SEO to Dominate the Search Engines <https://popupsmart.com/blog/chatgpt-prompts-for-seo>
14. Chat GPT Prompts <https://prompto.chat/>
15. My collection of +30 Chat-GPT Prompts For Quality Assurance <https://medium.com/@vincent.ferreira/my-collection-of-20-chat-gpt-prompts-for-quality-assurance-7eaef6633bd5>
16. Unlocking the Potential of AI in Education: ChatGPT Prompts and Use Cases <https://www.learnprompt.org/chat-gpt-prompts-for-education/>
17. GPT Prompts <https://simplified.com/gpt-prompts>
18. GPT prompts for developers <https://textcortex.com/post/chatgpt-prompts-for-developers>
19. Free GPT resource for programming <https://godsol.gumroad.com/l/100-chatgpt-programming-prompts>
20. Grow your biz: <https://www.instagram.com/p/Cp7Xvwxo-MO/>
21. [LIST OF +50 CLEVER GPT-3 PROMPTS 🤖](https://docs.google.com/spreadsheets/d/1EuciDyKqFg2CIoQS89tF238oGtJq8a4mRx8kV9eA1Lc/edit#gid=2011839893)
22. <https://www.promptvibes.com/>
23. [Awesome chat GPT prompts](https://github.com/f/awesome-chatgpt-prompts)
24. [Gold 10K Ultimate Prompts Bundle](https://miguelanticonam.gumroad.com/l/10k-prompts?ref=upstract.com) - 5$
25. <https://www.instagram.com/reel/Cr1lGaULYRy>
26. <https://www.instagram.com/p/Cs_IDaBNsMK/?igshid=MzRlODBiNWFlZA==>
27. <https://www.instagram.com/p/CsDa1t3tPj3/?igshid=MzRlODBiNWFlZA==>
28. <https://www.instagram.com/p/CtGD44TMlhh/?igshid=MzRlODBiNWFlZA==>
29. <https://www.instagram.com/p/CtMN67FgOVK/?igshid=MzRlODBiNWFlZA==>
30. <https://www.instagram.com/p/CqiYlJXDvVY/?igshid=MzRlODBiNWFlZA==>
31. <https://www.instagram.com/p/Cst3lfcAxoj/>
32. [ShareGPT Chrome extension](https://sharegpt.com/)
33. [FastChat](https://github.com/lm-sys/FastChat)
34. [650+ Best Prompts for ChatGPT](https://www.writingbeginner.com/best-prompts-for-chatgpt/)
35. [Prompts' db](https://www.prompthackers.co/)
36. [ChatGPTPromptshub: Master ChatGPT with Our Extensive Prompt Database](https://chatgptpromptshub.com)
37. [The Prompt Index: Explore the Ultimate Free AI Resource](https://www.thepromptindex.com)
38. [ChatGPT Prompts for Database Development and Management with Examples](https://www.developerupdates.com/blog/chatgpt-prompts-for-database-development-and-management-with-examples)
39. [1100 ChatGPT Content Marketing Expert Prompts](https://chatgpt-business-prompts.notion.site/chatgpt-business-prompts/1100-ChatGPT-Content-Marketing-Expert-Prompts-eea03b0bc9b84ae7a5bdbd76a67460f3)
40. [How to Write the Perfect ChatGPT Prompt (With Examples!)](https://www.mindandmetrics.com/blog/how-to-write-the-perfect-chatgpt-prompt-with-examples)
41. [The best AI tools & services in one place](https://easywithai.com/)
42. [Overview of 26 prompt principles](https://github.com/VILA-Lab/ATLAS/blob/main/data/README.md)
43. [Mastering Prompt Engineering for LLMs: Best Practices and Advanced Techniques](https://blog.dynopii.com/tutorials/mastering-prompt-engineering-for-llms-best-practices-and-advanced-techniques/)
44. [The Beginner's Guide to LLM Prompting](https://haystack.deepset.ai/blog/beginners-guide-to-llm-prompting)
45. [Zero Shot Chain of Thought](https://learnprompting.org/docs/intermediate/zero_shot_cot)
46. [7 Different Prompting Techniques](https://iq.opengenus.org/different-prompting-techniques/)
47. [Prompt Engineering: Advanced Techniques](https://www.mlq.ai/prompt-engineering-advanced-techniques/)
48. [12 ChatGPT Prompts for Text Analysis](https://mimlearnovate.com/chatgpt-prompts-for-text-analysis/#:~:text=12%20ChatGPT%20Prompts%20for%20Text%20Analysis%201%2012,ChatGPT%20to%20analyze%20multiple%20texts%20at%20once%3F%20)
49. [Generative AI for Beginners](https://microsoft.github.io/generative-ai-for-beginners/#/)
50. [26 prompting tricks to improve LLMs](https://www.superannotate.com/blog/llm-prompting-tricks#:~:text=26%20prompting%20techniques%201%201.%20No%20need%20to,examples%208%208.%20Format%20your%20prompt%20Wi%C4%99cej%20pozycji)
51. [Best Prompt Techniques for Best LLM Responses](https://medium.com/the-modern-scientist/best-prompt-techniques-for-best-llm-responses-24d2ff4f6bca)
52. [AI AUTOMATION AGENT FOR CHROME](https://harpa.ai/)
53. [26 prompting tricks to improve LLMs - SuperAnnotate](https://www.superannotate.com/blog/llm-prompting-tricks)
54. [Prompting Techniques | Prompt Engineering Guide](https://www.promptingguide.ai/techniques)
55. [5 advanced prompts to get better answers from ChatGPT - Descript](https://www.descript.com/blog/article/5-advanced-prompts-to-get-better-answers-from-chatgpt)
56. [Effective Prompting Techniques for Large Language Models](https://trypromptly.com/u/promptly_knowledge/prompting-techniques-llms-9EPgTI)
57. [The Ultimate Guide to Prompt Engineering - Techniques ... - XGrid.co](https://www.xgrid.co/resources/guide-to-prompt-engineering/)
58. [Advanced Prompt Engineering - Practical Examples - TensorOps](https://www.tensorops.ai/post/prompt-engineering-techniques-practical-guide)
59. [Build a LangChain agentic RAG system using Granite-3.0-8B-Instruct in watsonx.ai](https://www.ibm.com/think/tutorials/agentic-rag)
60. [Langchain RAG : From Basics to Production-Ready RAG Chatbot](https://blog.futuresmart.ai/langchain-rag-from-basics-to-production-ready-rag-chatbot)
61. [AI Stack](https://reymondin.notion.site/144643c1f67680a1ad7dde9416d9fc9b?v=9cfd6789c44e41e3baa2cdf3c6ddbd6e)
62. [building effective agents](https://www.anthropic.com/research/building-effective-agents)
63. [Cursor AI Prompts](https://ai-cursor.com/prompts/)
64. [Best practices for prompt engineering with the OpenAI API](https://help.openai.com/en/articles/6654000-best-practices-for-prompt-engineering-with-the-openai-api) – *OpenAI Help Center*  Official OpenAI documentation with practical guidelines (e.g., clear instructions, delimiters, structured outputs). Authoritative and concise.
65. [Prompt engineering best practices for ChatGPT](https://help.openai.com/en/articles/10032626-prompt-engineering-best-practices-for-chatgpt) – *OpenAI Help Center* Focused on ChatGPT users. Covers clarity, context, and iterative prompt refinement. Accessible and broadly applicable.
66. [Prompt engineering overview](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) – *Anthropic Documentation*  Explains why prompt design is faster/cheaper than finetuning. Offers a structured approach with testing and evaluation.
67. [Prompt Engineering Best Practices: Tips, Tricks, and Tools](https://www.digitalocean.com/resources/articles/prompt-engineering-best-practices) – *DigitalOcean Blog*  
   Lists 10 best practices with examples (specificity, examples, output structure). Practical and beginner-friendly.
68. [15 Tips to Become a Better Prompt Engineer for Generative AI](https://techcommunity.microsoft.com/blog/azure-ai-foundry-blog/15-tips-to-become-a-better-prompt-engineer-for-generative-ai/3882935) – *Microsoft Azure AI Foundry Blog*  
   Developer-oriented tips (clarity, examples, roles, refinement). Strong focus on practical application.
69. [7 Different Prompting Techniques](https://iq.opengenus.org/different-prompting-techniques/) – *OpenGenus IQ*  
   Covers zero-shot, few-shot, chain-of-thought, RAG, and more. Serves as a broad reference with clear examples.
70. [10 Essential Prompt Engineering Best Practices (With Examples)](https://www.promptjesus.com/blog/10-essential-prompt-engineering-best-practices) – *PromptJesus Blog*  
   Model-agnostic guide with concrete before/after examples. Covers clarity, context, roles, iterative refinement.
71. [Prompt engineering techniques](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/concepts/prompt-engineering) – *Microsoft Docs*  
   Systematic explanation of prompt components and best practices. Official technical resource, updated 2025.
72. [Prompting Capabilities](https://docs.mistral.ai/guides/prompting_capabilities/) – *Mistral AI Documentation*  
   Demonstrates use-cases (classification, summarization, personalization). Includes few-shot, delimiters, role-playing.
73. [Prompt Engineering Guide](https://learnprompting.org/docs/introduction) – *LearnPrompting.org*  
   Free, comprehensive tutorial from fundamentals to advanced tactics. Widely cited by industry (Google, Microsoft, O’Reilly).
