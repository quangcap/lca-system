# lca-system
Automatically Generating Questions about Students’ Code using Abstract Syntax Tree (AST)

## Overview

This project presents a system that automatically generates questions about students’ programming assignments by analyzing their source code through Abstract Syntax Trees (AST).
It aims to support instructors and students in automated code understanding, feedback, and evaluation, bridging the gap between static code analysis and educational assessment.

## Motivation

Most existing auto-assessment tools focus primarily on theoretical correctness or test-based evaluation.
However, they lack mechanisms to:
- Analyze how students write their code.
- Ask insightful questions that encourage reflection and conceptual understanding.
Manual assessment, on the other hand, is time-consuming and inconsistent.

This project introduces an automated, extensible system that:
- Traverses Java programs via their AST representation.
- Detects specific code structures or elements.
- Generates human-like questions using template-based analyzers.

🧩 System Architecture

The system consists of two main components:
1. Code Analyzers:
- Built using Spoon, a state-of-the-art Java AST analysis library.
- Traverses the AST to detect code patterns and specific programming constructs.
- Custom analyzers are provided as modular JAR files.
- Developers can extend the system by adding new analyzers.
2. Web Application: Enables users (teachers, TAs, or students) to:
- Submit and review programming assignments.
- View automatically generated questions about submitted code.
- Discuss and provide feedback on generated questions.
- Upload or contribute new analyzers.

## Methodology
1. AST Traversal: The system parses each submitted Java program and constructs its Abstract Syntax Tree.
2. Analyzer Matching: Each analyzer checks if certain elements (e.g., methods, loops, inheritance) exist in the AST.
3. Question Generation: When an element is detected, the system applies a question template (e.g., “Why did you use a loop here?”).
4. Customization: Users can create and integrate custom analyzers, while each analyzer is modular and independently loaded as a .jar file.

## Prototype Features
- Assignment Submission and Review
- Interactive Question Discussion
- Custom Analyzer Integration
- AST-based Pattern Detection

The prototype was tested using the open-source project PlantsVersusZombies as the target codebase.

## Technologies Used
- For AST Traversal: Spoon & Java
- Backend: Java Spring Boot
- Web: NextJS
