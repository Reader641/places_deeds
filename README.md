# Expansion of Django Project

The following is the exploration of expanding a Django project which was to capture information from the book, 'Of Hills, Halls, and Holes' and give it a structured form.

This expansion in scope is to blend what was observed by the away team and combine it with the current design as best as possible.


## Details to Be Considered

A more formal scope is still required and may be determined once confirmation about the new problem space has been given.


## Current Model Design

The following is the entities and their relations with a note on what was added:

**Deed** [Added]
- date (*format: year-month-day*)
- person (*model: Person*)
- type
- assets (*model: Asset*)
- categories (*model: Category*)
- reference_sources (*model: Reference_Source*)

**Person** [Added]
- name (*title; firstname; lastname)
- sex

**Other_Good** [Added]
- name
- note

**Asset** [Added]
- place (*model: Place*)
- other_goods (*model: Other_Good*)
- person (*model: Person*)



**Place**
- name
- size [added]
- cost [added]
- note
- categories (*model: Category*)
- territory (*model: Territory*)
- reference_sources (*model: Reference_Source*)

**Category**
- name
- note
- parent_category (*model: Category*)
- reference_sources (*model: Reference_Source*)

**Territory**
- name

**Nearby_Place**
- place (*model: Place*)
- nearby_place (*model: Place*)
- direction

**Reference_Source**
- name
- note (*description*)
