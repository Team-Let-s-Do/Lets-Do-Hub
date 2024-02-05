name: 🐞 Bug
description: File a bug/issue
title: "[BUG] <title>"
labels: ["Bug", "Needs Triage"]
body:
- type: dropdown
  attributes:
      label: What mod appears to be problematic?
      multiple: false
      options:
        - 🌲 BloomingNature
        - 🧀 Meadow
        - 🥥 Beachparty
        - 🍷 Vinery
        - 🍵 HerbalBrews
        - 🍖 Candlelight
        - 🍞 Bakery
        - 🍺 Brewery
  validations:
    required: true
- type: checkboxes
  attributes:
    label: Is there an existing issue for this?
    description: Please search to see if an issue already exists for the bug you encountered.
    options:
    - label: I have searched the existing issues
      required: true
- type: checkboxes
  attributes:
    label: Is the mod running in an unstable environment?
    options:
    - label: I am using a supported modloader (Forge, Fabric, Quilt)
      required: true
    - label: I have self built the mod
      required: false
    - label: This is running in a dev environment
      required: false
- type: textarea
  attributes:
    label: Current Behavior
    description: A concise description of what you're experiencing.
  validations:
    required: false
- type: textarea
  attributes:
    label: Expected Behavior
    description: A concise description of what you expected to happen.
  validations:
    required: false
- type: textarea
  attributes:
    label: Steps To Reproduce
    description: Steps to reproduce the behavior.
    placeholder: |
      1. In this environment...
      1. With this config...
      1. Run '...'
      1. See error...
  validations:
    required: false
- type: textarea
    id: logs
    attributes:
      label: Relevant log output
      description: Please copy and paste any relevant log output. This will be automatically formatted into code, so no need for backticks.
      render: shell
- type: dropdown
  attributes:
      label: What modloader are you running the mod on?
      multiple: false
      options:
        - Forge
        - Fabric
        - Quilt
  validations:
    required: true
- type: textarea
  attributes:
    label: Anything else?
    description: |
      Links? References? Anything that will give us more context about the issue you are encountering!
  
      Tip: You can attach images or log files by clicking this area to highlight it and then dragging files in.
  validations:
    required: false
