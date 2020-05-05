# Task Specification

## Abstract

This documents specifies the set of properties, their description, the order in which they should be positioned and the requirement level of each property.  

The key words  
"MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT",  
"SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL"  
in this document are to be interpreted as described in RFC 2119.

These and other key words will appear capitalized.
This document can be read as a text file but it was written using github flavored markdown.  
Any compatible markdown visualizer is RECOMMENDED.

## Properties

1. TASK MUST be present, denotes the title/brief description of the task itself.
2. TASKS SHOULD NOT distinguish between states beyond what could be derived from the START STRINGS list in [section 2 of Style](##Style).
3. DESCRIPTION is OPTIONAL, adds aditional context or information for the TASK.
4. Additional LABELS MAY be defined at discretion of the developper as switches, meaning their presence or lack there of acts respectively as a true or false condition.

## Style

1. Every TASK and related properties MUST be written on a single line on a file.
   1. Lines are REQUIRED to follow Unix new line style.
      1. Lines MUST be separated with a line return character. ('/n')
      2. Lines SHALL NOT have a carriage return character. ('/r')
2. TASKS MUST be preceded with one START STRING.
   1. The character '-'. (DASH)
   2. The string '[ ]'. (CHECK BOX)
   3. The string '[x]'. (MARKED CHECK BOX)
      1. the 'x' in MARKED CHECK BOX SHALL be case insensitive.
3. TASKS MAY have a space character between them and DASHES.
4. OPTIONAL PROPERTIES MUST be preceded by the '@' character. (i.e. DESCRIPTION)
5. OPTIONAL PROPERTIES MUST have a LABEL after the prefix.
   1. PROPERTIES MUST NOT have a space/blank character between the prefix and their LABEL
   2. These PROPERTIES MUST be case insensitive.
6. PROPERTIES MAY have a space character between the prefix character and the TASK or PROPERTY behind them
7. PROPERTIES  MAY add a suffix to separate LABELS from value
   1. It is RECOMMENDED that they are separated with the character ':'
