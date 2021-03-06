# Task Specification

## Abstract

This documents specifies the set of properties, their description, the order in which they should be positioned and the requirement level of each property.  

The key words  
"MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT",  
"SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL"  
in this document are to be interpreted as described in RFC 2119.

The words "LABEL" or "TAG" are to be interpreted as a string of characters naming the PROPERTY they represent.

All key words in this document will appear capitalized.
This document can be read as a text file but it was written using github flavored markdown.  
Any compatible markdown visualizer is RECOMMENDED.

## Property Specification

1. TASK, DESCRIPTION and DUE DATE must appear only once per task.
2. TASK MUST be present, denotes the title/brief description of the task itself.
3. TASKS SHOULD NOT distinguish between states beyond what could be derived from the START STRINGS list in [section 1 of Tasks](###Tasks).
   1. What any specific START STRING represents is left at the discretion of the implementation.
4. DESCRIPTION is an OPTIONAL LABEL, adds aditional context or information for the TASK.
5. DUE DATE is an OPTIONAL LABEL representing the date by which the TASK must be completed.
6. LABELS MUST be case insensitive when parsing.
7. Any LABEL involving time must be compliant with [ISO 8601](https://www.w3.org/TR/NOTE-datetime).
   1. LABELS involving time SHOULD follow [ISO 8601](https://www.w3.org/TR/NOTE-datetime) "Complete date plus hours and minutes" specification (YYYY-MM-DDThh:mm).
8. Additional LABELS MAY be defined at discretion of the developper as SWITCHES, meaning their presence or lack there of acts respectively as a true or false condition.
    1. these kind of LABELS MUST NOT contain values.
9. Additional LABELS MAY be defined at discretion of the developper as arbitrary PROPERTIES
    1. these kind of LABELS MUST be followed with a value.
10. Every TASK and related properties MUST be written on a single line on a file.
    1. TASKS SHOULD NOT have aditional characters to indicate their end.
    2. Lines are REQUIRED to follow Unix new line style.
      1. Lines MUST be separated with a line return character. ('/n')
      2. Lines MUST NOT have a carriage return character. ('/r')
11. TASKS MUST NOT repeat LABELS

## Style

### Tasks

1. TASKS MUST be preceded with one START STRING prefix.
   1. The character '-'. (DASH)
   2. The string '[ ]'. (CHECK BOX)
   3. The string '[x]'. (MARKED CHECK BOX)
      1. the 'x' in MARKED CHECK BOX SHALL be case insensitive.
2. TASKS MUST NOT have a space character between them and their START STRING.

### Properties

1. Every PROPERTY MUST indicate their LABEL.
   1. TASKS are the ONLY PROPERTY excempt of this rule. For TASK it MUST be absent.
2. PROPERTIES MUST be prefixed by the '@' character. (e.g. DESCRIPTION => @Description:Foo)
3. PROPERTIES MUST have a separator character to differentiate between diferent properties.
   1. The RECOMMENDED character is ';'
4. PROPERTIES  SHOULD have a suffix to separate LABELS from value.
   1. It is RECOMMENDED that they are separated with the character ':'.
   2. PROPERTIES MUST NOT have a blank space separating the LABEL, the SUFFIX nor the VALUE. 
5. PROPERTIES MUST have a LABEL after the prefix.
   1. PROPERTIES MUST NOT have a space/blank character between the prefix and their LABEL.

### Switches

1. SWITCHES are a special  kind of PROPERTY
2. SWITCHES MUST be prefixed by the character '+'. (e.g. +isRepeatable)
3. SWITCHES MUST NOT have a space between their prefix and their LABEL
