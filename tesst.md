This lecture introduces the field of **Interactive Systems**, focusing on the **design and implementation of human-computer interfaces** for laypeople. Prof. Samit Bhattacharya explains that these systems should prioritize **user-centric design**, ensuring that users are not forced to learn complex underlying technology.

### Key Concepts Covered:
* **Defining Interactive Systems:** Any device that takes user input, processes it based on a program, and provides output—such as a *digital pedometer*, *microwave oven*, or *smart TV* (3:49 - 11:28).
* **The Goal of User-Centric Design:** Systems must be accessible to non-experts without causing anxiety or loss of motivation due to cryptic error messages (16:04 - 17:10).
* **Four Pillars of Design:** Designers must focus on **interface elements**, their **geometric layout**, user **perception of system state**, and ensuring the interaction successfully bridges the gap to the user's **goal state** (23:45 - 26:38).

### Historical Evolution of Interactive Design (27:18 - 35:09):
1. **Prehistory (1940s-1970s):** The birth of displays, *Sketchpad*, the mouse, and early microprocessors.
2. **Early Phase (1980s-early 2000s):** The rise of the personal computer, *GUI*, *WYSIWYG*, and the World Wide Web.
3. **Pre-Modern Phase (late 1990s-2000s):** Development of mobile personal devices like the *Palm Pilot* and *Android*.
4. **Modern Phase (Ongoing):** The shift toward *ubiquitous computing* and *interconnected devices* (IoT and Cyber-Physical Systems), where computers become invisible parts of daily life.

This lecture provides an introduction to the concept of **usability** within the context of designing *Human-Computer Interfaces* (HCI).

**Key concepts covered in this lecture:**
* **Human-Computer Interaction (HCI):** Defined as the discipline concerned with the design, evaluation, and implementation of interactive computing systems for human use (2:45). It emphasizes incorporating human factors, needs, and expectations into the design process.
* **User Classification:** To design effectively, users are often categorized to better match system features to their needs. A common categorization includes **novice**, **intermittent**, and **expert** users (11:20). For example, providing both menu options and keyboard shortcuts (hotkeys) caters to different user groups (12:05).
* **Defining Usability:** The lecture references the *ISO 9241-210:2009* standard, which defines usability based on effectiveness, efficiency, and satisfaction for specific users, goals, and contexts (20:01). It notes that *Jacob Nielsen* distinguished between **usability** and **utility**—where usability is the ease of use, and utility is the functionality provided—to determine if a product is truly useful (23:15).
* **Nielsen's Five Measures of Usability:** To provide a precise evaluation, the lecture focuses on five quality components: **learnability**, **efficiency**, **memorability**, **errors** (rate, severity, and recovery), and **satisfaction** (24:39).
* **User-Centered Design (UCD):** Coined by *Ben Shneiderman* in 1986, this approach seeks to increase product usability through the active or passive involvement of end-users throughout the development lifecycle (29:42). It is closely related to terms like *participatory*, *cooperative*, and *human-centered design* (30:52).

This lecture, part of the *Design and Implementation of Human-Computer Interfaces* course, focuses on **engineering for usability** through systematic software development lifecycles (SDLCs).

**Core Concepts:**
* **Usability as a Design Goal:** The primary objective is to build systems that cater to the needs and expectations of *layman users* (2:43).
* **Importance of SDLCs:** Using a structured, step-by-step approach—illustrated by the example of designing a mobile calendar app (5:25)—helps manage complexity and compare alternative designs effectively (12:04).

**SDLC Models Discussed:**
1. **Waterfall Model:** A fundamental, stage-wise approach including **feasibility study**, **requirement gathering**, **design**, **coding/testing**, and **deployment/maintenance** (14:11). It can be implemented as a classical or *iterative* model to handle feedback (17:35).
2. **Spiral Model:** A meta-model involving multiple iterations across four quadrants: **identifying objectives**, **risk assessment/mitigation**, **prototype development**, and **customer evaluation/planning** (18:53). This model is particularly useful for managing risks and progressively building complex systems (23:42).

**Conclusion:**
While traditional models provide structure, they can become "messy" when frequent iterations are required to incorporate user feedback for interactive systems (25:06). The next lecture will explore alternative models better suited for this purpose (26:22).

This lecture introduces a **user-centric life cycle** model for developing interactive software, explaining why traditional models like the *waterfall model* are often insufficient for creating usable interfaces.

**Key Takeaways:**

* **Limitations of the Waterfall Model:** While useful for building efficient systems, the linear waterfall model (1:43) struggles with user-centered design because it doesn't naturally incorporate the iterative feedback loops required to ensure software is truly usable (3:51).
* **The Proposed Interactive Life Cycle (5:59):** This model replaces the linear flow with iterative stages to better accommodate user feedback:
    * **Requirement Gathering (8:53):** Focuses on capturing end-user needs through techniques like contextual inquiry and ethnographic studies.
    * **Design-Prototype-Evaluate Cycle (9:33):** An iterative loop of designing, building prototypes, and performing early evaluations to refine the interface until the design stabilizes.
    * **Coding & Implementation (13:26):** Translates the finalized interface design into code; iterations here are internal to the design team.
    * **Empirical Study (14:16):** A final, systematic usability test with end-users, occurring after code testing to verify the product meets usability requirements.
* **Design vs. Code Iteration (12:43):** The lecturer highlights that there are two distinct iterative cycles: one for the **interface** (involving users) and one for the **code** (brainstorming within the development team).
* **Cost Management (15:29):** The model emphasizes that usability testing is resource-intensive; therefore, early-stage design iterations are critical to prevent costly, late-stage code modifications.

This lecture provides an introduction to **usability requirements** within the software development life cycle for interactive systems. Prof. Samit Bhattacharya emphasizes that gathering these requirements is a crucial stage (4:26) for ensuring that software is effectively designed for **layperson users** rather than just technical convenience.

**Key concepts covered:**

*   **System-Centered vs. User-Centered Design:** The lecture contrasts traditional system-centered development—which prioritizes developer expertise and platform constraints (13:40)—with user-centered design, which focuses on user abilities, goals, and the context of use (14:47).
*   **Defining Usability Requirements:** The professor clarifies that common developer questions regarding programming languages, platforms, or storage (like RDBMS) are often related to **feasibility** or **system design** phases rather than usability requirement gathering (19:54).
*   **Non-Functional Requirements (NFRs):** Usability requirements are categorized as a type of non-functional requirement (24:18). These are quality attributes that cannot be expressed as simple input/output functions. He breaks NFRs into five categories (26:39):
    *   **Performance:** Reliability, security, and response time.
    *   **Operating Constraints:** Physical size, personnel, and skill sets.
    *   **Economic Considerations:** Cost for design and maintenance.
    *   **Life Cycle Requirements:** Maintainability, enhanceability, and portability.
    *   **Interface Issues:** Includes both technical system interfacing and user usability (31:31).

**Consequences of Neglecting NFRs:**
Failing to specify these requirements early leads to significant risks, including **unsatisfied users and developers**, **inconsistent software**, and severe **time and cost overruns** during later stages (35:34).

(Week 2 haha se start kana hai)
