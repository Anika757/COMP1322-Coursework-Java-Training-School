# COMP1322-Coursework-Java-Training-School
Object-oriented Java simulation with dynamic course scheduling, instructor assignment, student progression, and save/load functionality

An object-oriented simulation of a Java training school, built for COMP1322 Programming II at the University of Southampton. Marked at 97.4% (coursework worth 30% of the module)

# What it does
Simulates a school day by day. The school creates courses for its subjects, assigns instructors according to their specialisms, and enrols free students onto courses they haven't yet completed. Courses run for a fixed duration and issue certificates on completion — or get cancelled if they start with no instructor or students. An Administrator drives the simulation: probabilistically admitting new students and instructors each day, advancing the school, and reporting the full state after every day.

# Key features
Inheritance and polymorphism — a Person base class extended by Student and an abstract Instructor, with Teacher, Demonstrator, OOTrainer and GUITrainer subclasses implementing canTeach() against subject specialisms
Simulation rules — courses cap at three students and exactly one instructor; students and instructors each take at most one course at a time
External configuration — initial state (school, subjects, students, instructors) parsed from a text config file with validation
Save and resume — full runtime state (courses, enrolments, assignments, timing) written to a .save.txt file and reconstructed on load, so a simulation can be paused and continued
Exception handling — custom exceptions and defensive checks for malformed config lines, non-numeric fields, unknown instructor types and illegal operations (e.g. enrolling on a course that has already started)

# Design
Modelled with UML use case, class and sequence diagrams produced as part of the submission.
