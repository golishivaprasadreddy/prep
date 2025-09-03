# RPA UNIT 1

This document provides detailed notes on **RPA (Robotic Process Automation)** and the **UiPath platform**, structured for easy understanding and exam preparation.

---

## 1. Components of RPA

RPA consists of multiple components that work together to automate repetitive tasks:

### **1. Development Tools**

* **Purpose:** Used to design automation workflows.
* **Examples:** UiPath Studio, Blue Prism Process Studio.
* **Functionality:** Drag-and-drop activities, recorders, scripting.

### **2. Bots / Robots**

* **Purpose:** Software agents that execute automation workflows.
* **Types:** Attended, Unattended.
* **Functionality:** Interact with applications, perform repetitive tasks.

### **3. Control Room / Orchestrator**

* **Purpose:** Central platform to manage, schedule, and monitor bots.
* **Functionality:** Deployment, job scheduling, logging, error handling.

### **4. Recorder**

* **Purpose:** Captures human actions and converts them into automation steps.
* **Functionality:** Records mouse clicks, keystrokes, and generates workflows automatically.

### **5. Analytics / Dashboard**

* **Purpose:** Provides performance tracking, execution reports, and ROI insights.
* **Functionality:** Helps identify bottlenecks and optimize processes.

### **Diagram (Text Form)**

```
[ Development Tools ] ---> [ Control Room / Orchestrator ] ---> [ Robots ] ---> [ Applications ]
                                   |
                           [ Analytics / Dashboard ]
```

---

## 2. Architecture of UiPath Stack (Studio, Robot, Orchestrator)

### **Components**

1. **UiPath Studio**

   * Development environment to create automation workflows (.xaml files).
   * Publishes workflows as packages (.nupkg) to Orchestrator or local feed.
   * Example: Create automation to extract invoice data.

2. **UiPath Robot**

   * Executes the workflows created in Studio.
   * **Types:** Attended & Unattended.
   * Example: Automatically read emails and save attachments.

3. **UiPath Orchestrator**

   * Web-based control center.
   * Handles deployment, scheduling, monitoring, and reporting.
   * Example: Schedule a bot to run payroll at the end of the month.

### **Architecture Flow**

1. Workflow created in Studio.
2. Published to Orchestrator (or local machine).
3. Robot downloads and executes the workflow.
4. Logs/results sent back to Orchestrator.

### **Diagram (Text Form)**

```
[ UiPath Studio ] ---> Publishes ---> [ Orchestrator ] ---> Assigns ---> [ Robots ] ---> Runs on Applications
```

---

## 3. Role of UiPath Orchestrator in Automation Lifecycle

### **Key Roles**

1. **Deployment:** Distributes automation packages to robots.
2. **Scheduling:** Runs bots at defined times.
3. **Execution:** Starts and stops automation jobs.
4. **Monitoring:** Tracks logs, errors, and robot status.
5. **Queue Management:** Handles task distribution for multiple robots.
6. **Analytics:** Generates performance reports and insights.

### **Examples**

* Scheduling a payroll bot every month.
* Monitoring invoice-processing bots and checking error logs.

---

## 4. Types of Robots in UiPath

| **Robot Type**       | **Description**                                  | **Example**                          |
| -------------------- | ------------------------------------------------ | ------------------------------------ |
| Attended Robot       | Works with humans, triggered manually            | Customer service agent launching bot |
| Unattended Robot     | Runs in background without human help            | Nightly invoice processing           |
| Non-Production Robot | Used for development and testing                 | Developer testing workflows          |
| Test Robot           | Used in UiPath Test Suite for automation testing | Automated regression tests           |

---

## 5. UiPath Project Types

| **Project Type**        | **Purpose**                                   | **Example**                       |
| ----------------------- | --------------------------------------------- | --------------------------------- |
| Process                 | Standard automation workflow                  | Invoice data entry automation     |
| Library                 | Reusable components                           | Custom "Send Email" workflow      |
| Orchestration Process   | Long-running workflows with human interaction | Loan approval process             |
| Background Process      | Runs without disturbing user                  | Email monitoring bot              |
| Test Automation Project | For application/API testing                   | Automated regression testing      |
| Template                | Predefined project structure                  | Login workflow template           |
| Trigger-Based Attended  | Starts on user actions                        | Bot runs when a new file is added |

---

## 6. Scope and Techniques of Automation

### **Scope (Where Automation is Used)**

* **Industry:** Robots in manufacturing.
* **Business:** RPA in finance, HR.
* **IT:** Automated deployments, backups.
* **Office:** Excel macros, email auto-replies.
* **Smart Homes:** IoT devices like Alexa.
* **Healthcare:** Robotic surgery, appointment scheduling.

### **Techniques (How Automation is Done)**

1. **Fixed Automation:** Single repetitive task (Bottle filling machine).
2. **Programmable Automation:** Can be reprogrammed (CNC machines).
3. **Flexible Automation:** Easily switch tasks (3D printing, robots assembling cars).
4. **Business Process Automation (RPA):** Office tasks (Data entry bots).
5. **Cognitive Automation:** AI-based automation (Chatbots, fraud detection).

---

## 7. UiPath / RPA Platforms

### **Components of UiPath Platform**

1. **UiPath Studio:** Build automation workflows.
2. **UiPath Robots:** Execute automation.
3. **UiPath Orchestrator:** Manage and monitor robots.
4. **UiPath Assistant:** Interface for launching attended automations.
5. **UiPath AI Center:** Integrate ML/AI models.
6. **UiPath Test Suite:** Application/API testing.
7. **UiPath Insights:** Analytics and reporting.

### **Diagram (Text Form)**

```
 UiPath Platform:
   [ Studio ] -> [ Robots ] -> [ Orchestrator ]
                        |
   +--------------------+---------------------+
   | Assistant | AI Center | Test Suite | Insights |
```

---

**Quick Tips:**

* Architecture questions → focus on Studio, Robot, Orchestrator.
* Platform questions → include all UiPath components (Assistant, AI Center, Insights, Test Suite).
* Components of RPA → general RPA parts, not UiPath-specific.

---