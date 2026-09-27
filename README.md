# IT0123 DevNet Resource Validation Plan

## Student and Project

- Name: Klezzel Arvee S. Usana
- Section: TN37
- Repository name: `it0123-devnet-resource-plan`

## Purpose

Selecting the correct DevNet resource ensures developers choose an environment that matches their required access privileges, isolation level, and setup constraints. Using an unsuitable resource can lead to blocked administrative tasks in shared sandboxes or unnecessary wait times for basic API learning. Proper validation prevents credential leakage and ensures development starts in a safe, reproducible environment.

## Validated Resource Decisions

UC1: Quick read-only API explorationSelected Resource: always-on-sandbox Most Important Requirement: Immediate access to a shared environment for safe, read-only requests without waiting for provisioning. Official Cisco Evidence: Cisco DevNet Sandbox documentation https://developer.cisco.com/docs/sandbox/, which confirms Always-On sandboxes provide 24/7 shared access without requiring VPN setup or reservation wait times, but enforce restricted administrative access.

UC2: Private configuration testingSelected Resource: reservation-sandbox Most Important Requirement: Administrative access in an isolated, private environment to test configuration changes while accepting setup time and VPN usage. Official Cisco Evidence: Cisco DevNet Sandbox documentation \https://developer.cisco.com/docs/sandbox/, which specifies that Reservation Sandboxes provide dedicated, isolated environments with administrative control via VPN after a provisioning period.

UC3: Guided API concept practiceSelected Resource: learning-lab Most Important Requirement: Structured, step-by-step learning content and guided practice rather than unguided device administration. Official Cisco Evidence: Cisco DevNet Learning Labs documentation https://developer.cisco.com/learning, which establishes that Learning Labs offer modular, guided educational tutorials designed to teach concepts step by step.

UC4: Reusable automation exampleSelected Resource: code-exchange Most Important Requirement: Access to community and Cisco-maintained sample repositories for an existing network-automation use case before building a new solution. Official Cisco Evidence: Cisco Code Exchange documentation
https://developer.cisco.com/codeexchange/)), which identifies Code Exchange as the central portal for discovering curated, open-source repositories and automation sample code.

## AI Evaluation

The AI initially recommended an Always-On sandbox for general API experimentation, but verification against official Cisco documentation confirmed that Always-On sandboxes do not permit administrative configuration changes. Consequently, UC2 required a Reservation Sandbox to obtain full administrative privileges and VPN connectivity.

## Validation Evidence

- Validator result:
  PS C:\FEU TECH\1TSY2627\CS0016 - NETWORK & COMMUNICATIONS 2A\S2\it0123-devnet-resource-plan> python validate_plan.py
  PASS: JSON file loaded
  PASS: student and AI disclosure completed
  PASS: all four scenario IDs present
  PASS: resource classifications match scenario requirements
  PASS: official Cisco evidence URLs supplied
  PASS: AI verification statuses are valid
  PASS: rationales are sufficiently detailed
  PASS: AI recommendations are summarized in the student's own words
  PASS: no credential-like fields detected

VALIDATION COMPLETE: 9/9 checks passed.

- Command used: python validate_plan.py

- Official Cisco pages reviewed:
  https://developer.cisco.com/docs/sandbox/getting-started/#always-on-sandboxes
  https://developer.cisco.com/learning/
  https://developer.cisco.com/codeexchange/

## Git Evidence

- Initial commit message: "Initial commit: set up workspace with starter files and README"
- Validation commit message: "Complete resource plan and pass validation"
- Output of `git log --oneline`:
  1ea5bf5 (HEAD -> master) Complete resource plan and pass validation
  b151f8a Initial commit: set up workspace with starter files and README

## AI-Use Disclosure

Gemini was used to verify scenario requirements against official DevNet definitions, and generate the sample JSON structure. All resource URLs, privileges, and sandbox constraints were cross-checked directly with official Cisco DevNet documentation.
