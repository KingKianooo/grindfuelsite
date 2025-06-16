---
layout: single
title: "GrindFuel Post-Mortem"
permalink: /post-mortem/
author_profile: false
header:
  overlay_color: "#000"
  overlay_filter: "0.4"
  overlay_image: /assets/images/grindfuel-project.jpg
---

## GrindFuel Post-Mortem: A Retrospective

Developing GrindFuel was a transformative experience, filled with valuable lessons. This document outlines our reflections on the project's architecture, key design decisions, and how we would approach future iterations differently.

---

### Architectural Analysis

The GrindFuel application was built on a three-tiered architecture: Presentation, Logic, and Persistence. This layered approach fostered a robust and maintainable system:

**Presentation Layer:** This layer managed all user interactions. `GrindFuel.java` initialized services and injected them into the main `GrindFuelController` and other FXML controllers (e.g., `TaskEditController`, `NewProjectController`). These controllers were responsible for handling specific UI elements and user input.

**Logic Layer:** Business logic was encapsulated within service interfaces like `TaskService` and `ProjectService`. These interfaces defined the operations permissible on the application's data.

**Persistence Layer:** Data storage and retrieval were managed through Data Access Object (DAO) interfaces, such as `TaskDao` and `ProjectDao`. This abstraction allowed us to seamlessly switch between a mock database and a real one.

This clear separation of concerns, with controllers calling services and services interacting with DAOs, significantly enhanced the maintainability, testability, and scalability of GrindFuel. Furthermore, the use of Data Service Objects (DSOs), like `Task` and `Project` DSOs, facilitated structured data encapsulation and transfer between these layers.

---

### Project Scale and Effort Distribution

The GrindFuel project comprised approximately 142 files in total. A breakdown of the file distribution across the major system components is as follows:

- **Presentation Layer:** Approximately 15 classes
- **Persistence Layer:** 11 interfaces/full classes, with an additional 9 classes dedicated to the SQLite implementation and 8 for the stub implementation
- **Logic Layer:** 7 interfaces, a service factory, and 11 classes within the implementation package
- **Other:** 6 exception classes, 4 Data Service Objects (DSOs), and 6 classes in the core grindfuel folder

While we couldn't easily quantify the exact number of methods or classes beyond file counts, our time logs provide insights into the effort distribution. Across our three iterations, we collectively logged 537 hours. We estimate the time spent on each major component as follows:

| Component          | Percentage of Total Hours |
|-------------------|----------------------------|
| UI/Presentation    | 40%                        |
| Persistence Layer  | 25%                        |
| Logic Layer        | 20%                        |
| Testing            | 15%                        |

The presentation layer absorbed the largest portion of time, primarily due to the learning curve associated with FXML and the complexities of wrapping existing packages and functions. Two of our programmers were almost exclusively dedicated to this layer.

---

### Critical Design Decision: Controller Refactoring

A pivotal design decision made later in the final iteration was the introduction of the `ControllerFactory` and the separation of the `GrindFuelController` into a dedicated page navigator. Initially, the `GrindFuelController` was overburdened, acting as both the main page controller and the navigation hub for all other pages. While functional for a small application, this approach led to a "bloated behemoth" as the application grew.

This design flaw resulted in:

- **High Coupling:** The `GrindFuelController` was deeply coupled to many other controllers.
- **Violation of Single Responsibility Principle (SRP):** It performed multiple, unrelated tasks.

The `ControllerFactory` effectively addressed the manual dependency injection issues that previously led to excessive instance variables and tight coupling among classes. These two changes collectively reoriented and significantly improved the quality of our front-end code, reducing coupling and better adhering to fundamental design principles.

---

### Recommendations for Future Iterations: What We Learned

If given the opportunity to restart Iteration 3, our focus would be on preventing burnout, enhancing code quality, streamlining workflows, and integrating feedback more effectively.

**Prioritizing Team Well-being**

To foster a healthier work-life balance, we would implement a policy ensuring at least four nights per week where no work extends past midnight.

**Enhancing Code Quality and Process**

We would introduce dedicated GitLab tickets for manual testing, treating it as a formal, assigned, and tracked task. Our success metric would be the number of previously undetected bugs identified and fixed through this deliberate effort.

To prevent duplicate work and ensure clear ownership, all work would be tied to a GitLab ticket, and every ticket would be assigned before work commences. Success would be measured by a clear record of task ownership and the elimination of redundant efforts.

To minimize merge conflicts and simplify code reviews, we would prioritize submitting smaller, more frequent merge requests, aiming for most to involve fewer than five changed files.

**Streamlining Workflow and Feedback Integration**

Our sprint planning would incorporate dedicated "breathing room" to integrate feedback efficiently without disrupting overall progress. The goal would be to consistently spread out work throughout the sprint, aiming to complete at least one major feature by Wednesday each week.

These changes would collectively lead to a more sustainable, efficient, and higher-quality development process.
