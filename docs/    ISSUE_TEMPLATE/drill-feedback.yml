name: Drill feedback
description: Give short feedback on a drill’s clarity, realism, and result quality
title: "[DRILL] "
labels:
  - feedback
  - beta
  - drill
body:
  - type: markdown
    attributes:
      value: |
        Use this form for drill feedback.

        Keep it short. We care about:
        - clarity
        - realism
        - whether the guidance helped
        - whether the debrief matched what happened

  - type: dropdown
    id: drill
    attributes:
      label: Drill
      options:
        - quickstart
        - vsag
        - phaseerr
        - overcurrent
        - stuck
        - combined
    validations:
      required: true

  - type: dropdown
    id: result
    attributes:
      label: Result
      options:
        - Completed
        - Failed by trip
        - Failed by timeout
        - Could not understand what to do
        - Could not complete because of bug
    validations:
      required: true

  - type: dropdown
    id: clarity
    attributes:
      label: Guidance clarity
      options:
        - Clear
        - Mostly clear
        - Mixed
        - Confusing
    validations:
      required: true

  - type: dropdown
    id: realism
    attributes:
      label: Realism
      options:
        - Feels realistic
        - Mostly realistic
        - Acceptable abstraction
        - Feels off
    validations:
      required: true

  - type: textarea
    id: strongest
    attributes:
      label: What worked well?
      placeholder: Guidance made it obvious what I needed to correct before closure.
    validations:
      required: true

  - type: textarea
    id: weakest
    attributes:
      label: What felt weak or confusing?
      placeholder: The phase drill still felt hard to read on mobile.
    validations:
      required: true

  - type: textarea
    id: suggestion
    attributes:
      label: One suggested improvement
      placeholder: Add a clearer blocker line when phase is the only thing preventing sync.
    validations:
      required: false
