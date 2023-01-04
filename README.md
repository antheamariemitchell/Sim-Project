# Sim-Project
Explanation and files for Georgia Tech's group simulation project on infectious disease. Arena file written by Anthea Mitchell, project included two other members for analysis and output processing.

Includes .doe file and screenshots of simulation.

The Arena model was constructed to simulate an influenza outbreak scenario and was built on a framework of variables, attributes, and conditional decision branches. These all functioned within a system of time kept by “hour” entities created and disposed of in a separate work stream parallel to the main branch.

A student is infectious on all three days that they are sick, after which they become immune.

● Immunity follows an infection and lasts for a lifetime.

● Tommy interacts with all students in the classroom on each day that he is infectious.

● All students interact with each other in a classroom.

● If a student interacts with one student who is infectious they have a p 0.02 chance of getting sick, and they will inevitably interact with every student, e.g. if there are five sick students, each healthy student will have a 2x(5) = 10% chance of getting sick.


Immunity Definition

Rules around immunity were assumed to be simplistic. No previous immunity would be introduced apart from patient zero, who comes into the simulation already infectious. There was to be no immunity by degrees (as in the case with a partially effective flu shot) and all students were considered fully susceptible or fully immune. A student would be considered fully immune immediately at the time of infection. This consideration was created on the assumption that the student would not be able to get infected with the flu while already sick, and would not be able to catch the flu again after recovering
because the student would gain immunity to the virus.

All students were assumed to interact with every other student insofar as they are present within a small enough space to come in contact with aerosolized virions, or fomites from surrounding surfaces. It follows that 5 infectious students would give any single susceptible student a 10% chance of being infected that day.

Sick Status vs. Infectious Status

A status of “sick” versus “infectious” was used to differentiate between students who got sick on day t, but would not be infectious until day t+1. Attendance was assumed regardless of status, that is a student would attend school for all 3 Days that they were infectious.
