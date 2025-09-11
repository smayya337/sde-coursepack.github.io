---
Title: Course Materials
---

# Course Materials

{: .no_toc }

This page broadly describes the course material. If you are an instructor wishing to use materials/assignments/exams from this course, you can reach out to Prof. Rich Nguyen at (nn4pj at virginia dot edu). Please email from a verifiable institution or organization email address.

---

## Contents

{: .no_toc }

- TOC
{:toc}

---

<!-- TODO: we don't have a central repo for this... do we make one? -->
<!-- ## Public Course Materials

Public course materials from Fall 2023 (including syllabus, schedule, slides, homeworks, and assigned readings) [can be found here](https://drive.google.com/drive/folders/1PnTRphKY5adKNRX_XDCGI1djVgW68uwH?usp=share_link) - be aware that the website was incomplete during the Fall 2023 term, so some reading links are missing. -->

---

## Assignments

This course is intended to have 6 small-group (2-3 person teams) assignments. These assignments are each separate, and students do not carry their own code over between assignments. This is because while this course is designed to prepare students to work on projects, it is not itself a project course. The rationale for this decision is that in project courses, if students get behind earlier, then it can often because an unsalvageable situation. We wanted to avoid that, as this is typically a second-year (sophomore) course, and may be the first experience of group work a student has experienced.

### Assignments

The following are a listing of assignments used in the current offering of this course.

#### Homework 1 - Getting started

<!-- **Instructions:** [Homework 1 Part 1 - Congressional Apportionment](https://drive.google.com/drive/folders/1e1vZnONK2K6Iui_cOG5hDufWbbESYvXC?usp=share_link)
**Starter Code:** None -->
**Core skills:** Basic implementation of features using the Java programming language, version control via Git, command line arguments, file I/O, gradle build tools

This assignment was inspired by the following Stand-up Maths video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/GVhFBujPlVo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

This assignment is intended to get students acquainted with the idea of changing requirements. Very specifically, I tell the students that the second part of the assignment _will_ involve a change in the directions of Homework 1. Students also immediately begin using Git, as GitHub classroom was used for both group work and submission. Students are not given any starter code, and are left to their own devices to design and implement their system.

**[Homework 1 Part 2 - Responding to Change](https://drive.google.com/drive/folders/1uf3qMsiimUJNlDG9JcGnp3vElJdXOJin?usp=sharing)**
**Core skills:** - Responding to change, modifying existing code, using external libraries via gradle import.
Here, we make changes to the requirements, like using a different apportionment method and requiring support for an additional data source, and students have to change their code to accommodate these new demands. The goal of this assignment is for students to reflect on what design decisions in their initial work ended up making their code difficult to change, as well as recognizing that going back and reading your own code, even just a few days later, can be a difficult task if you don't take care to ensure your code is readable.

#### Homework 2 - Testing

<!-- **Instructions:** [Homework 2 - Testing](https://drive.google.com/drive/folders/1xi6STimSawEstbMaqq_YaIA1MpJQvWCK?usp=sharing)  
**Starter Code:** Request starter code by contacting Prof. McBurney - redacted for the time being, but will be made public again at a later date. -->
**Core Skills:** JUnit testing, black-box and white-box testing, debugging, test driven-development, enumerated types, reading and understanding existing code.

In this assignment, students debugged and finished implementing a command-line user interface of the popular game [Wordle](https://www.nytimes.com/games/wordle/index.html).

This assignment has 2 goals:

- Use JUnit testing to identify and fix an existing bug in the partially implemented Wordle game.
- Use test driven development with JUnit testing to finish implementing a command-line user interface version of Wordle.

The goal is to ensure students learn the syntax of JUnit testing, as well as how to construct effective test plans and utilize test-driven development.

#### Homework 3 - Using Polymorphism

<!-- **Instructions:** [Homework 3 - Refactoring and Polymorphism](https://drive.google.com/drive/folders/1ONT9mpY0qXppP9UM4ieZNSSLVB36q0k6?usp=share_link)
**Starter Code:** Request starter code by contacting Prof. McBurney - redacted because the assignment has a partial solution to Homework 1 -->
**Core skills:** Polymorphism, building from an existing design paradigm, changing existing code, Java Streams

This assignment uses the same Apportionment problem as Homework 1 while adding additional features and changed requirements. In this assignment, students began with **my** implementation of Homework 1, rather than their own, which uses some design techniques and patterns taught in class. For most students, they find the design that I give them was easier to modify and understand than their own designs (of course this isn't universally true, but students who already had strong designs of their own were likely already knowledgeable of many of the topics in our design unit.)

In this assignment, students reimplemented some features from Homework 1 within my starter code base, then add additional features, including a third apportionment method and displaying states in either alphabetical order or in an alternative order. In particular, the existing code base also features use of Java `Stream`s to give practice using functional programming.

#### Homework 4 - Mockito Testing and Refactoring

<!-- **Instructions:** [Homework 4 - Mockito, UML, and Design](https://drive.google.com/drive/folders/1WC67PfXlBG0sIluAzzVJhUylWhdkPS94?usp=sharing)
**Starter Code:** Request starter code by contacting Prof. McBurney - redacted for the time being, but will be made public again at a later date. -->
**Core skills:** Refactoring code to fix code smells, `mockito` testing, and documenting design via UML class diagrams

In this assignment, students are given code with a couple significant code smells:

1. One class, [(Course.java)](https://github.com/uva-cs3140-fa22/Homework-4-Starter/blob/main/src/main/java/edu/virginia/cs/hw4/Course.java), is far too large and loosely cohesive.
2. The [Student.java](https://github.com/uva-cs3140-fa22/Homework-4-Starter/blob/main/src/main/java/edu/virginia/cs/hw4/Student.java) class in particular violates the design principle of abstraction but directly manipulating fields of another class, as well as has multiple bugs

The first part of this assignment is for students to document the existing class structure using UML Class Diagrams, with an emphasis on noting the types of relationships between classes. The students then propose a decomposition of the Course class into several separate classes (correct answers usually had things like `Course`, `Section`, `Professor`, `Enrollment`, etc.)

The second part of this assignment is for Students to refactor and debug Student.java, using `mockito` to mock any Course objects (as, given the current state of the Course class, actually creating a Course object can be difficult).

Finally, students implement the class `RegistrationImpl.java` using test-driven development with `mockito` to mock any Student and Course objects.

#### Homework 5 - JSON and Database

<!-- **Instructions** - [Wordle GUI](https://docs.google.com/document/d/13QnUGj4tHoW_J3oHtPn9XNFfu79bZwEhVkLG8NgncO4/edit?usp=sharing)
**Starter Code** - Request starter code by contacting Prof. McBurney - redacted for the time being, but will be made public again at a later date. -->
**Core Skills** - Using JSON-based web-services, using JDBC with a SQLite database.

This assignment involves using a bus-routes webservice previously hosted by the University of Virginia. Students need to query that webservice to get information about bus-routes accessible to UVA students, and then store that information in a SQLite database. Students also must query that database for information like "What bus routes stop at Rice Hall"?

#### Homework 6 - "Final Project"

<!-- **Instructions** - [Homework 7 - Course Reviews](https://drive.google.com/drive/folders/15OLM4Ho-BvS2x2hMuGymoaME0t4W2GRS?usp=share_link)
**Starter Code** - None -->
**Core Skills**: Starting from scratch for the first time since Homework 1, students design and implement their own CRUD application for course reviews.

This assignment acts as a capstone on the course, where students must implement a three-layer architecture application for course reviews. The application must have:

- A graphical user interface using JavaFX
- A SQLite database to persist data between runs. Students were encouraged, but not required, to use Hibernate ORM to handle database interactions.
- An application that supports reviewing a class and viewing reviews for a class.
<!-- 
---

## Exams

The course typically has 3 exams. Each exam covers a certain subset of the course.

Generally, the tests break down as follows, as well as which modules are part of that exam:

- Exams 1 - Tools of the Trade
  - Intro
  - Java
  - Construction
  - First half of testing
  - Refactoring
- Exams 2 - Design
  - Design
  - Second half of Testing
  - Patterns
- Exams 3 - Front to Back
  - GUI
  - Data
  - Exam 3 is a cumulative final exam.

Exams are available upon request from instructors. Please email from a verifiable institution or organization email address. I will not be posting past exams publicly.

---

## Slides

I eventually plan to include slide decks related to course materials on each page. The slide decks are nearly finalized, but I am planning to edit/change/expand them for Fall 2023. However, you may contact me if you wish to see my current slide deck.

Slides from Fall 2023 are visible here: Public course materials from Fall 2023 (including slides, homeworks, and assigned readings) [can be found here](https://drive.google.com/drive/folders/1PnTRphKY5adKNRX_XDCGI1djVgW68uwH?usp=share_link)

---

## Lecture Videos

A long-term goal is to record videos for each lesson that will be embedded within the website for most articles. However, these videos will be intended to **supplement** the reading, **not replace the reading**. Students are warned that there will be content in the reading not covered in the videos that they will be responsible for.

Due to FERPA considerations, I cannot publicly upload class recordings from previous semesters. -->
