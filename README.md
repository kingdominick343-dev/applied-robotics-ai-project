# C-RAM Desktop Camera Tracker

An educational, C-RAM-inspired desktop camera-tracking demonstrator for the Applied Robotics and AI Project. The planned outcome is a two-axis camera platform that follows a demonstration object. Scope is camera tracking only, with no projectile-launching mechanism.

## Current status
Planning and workspace setup, 20 October 2026. The repository and Trello board are established. No working tracker, firmware, mechanical assembly or hardware test has yet been verified.

Confirmed direction: use the laptop webcam first; purchase and evaluate an ESP32-CAM later. The project discussion identifies an existing ESP32 and 3D printer. Other hardware remains to be confirmed.

## Development stages
1. **Laptop webcam prototype:** verify camera capture, choose a demonstration object, and develop on-screen tracking with Python and OpenCV.
2. **Hardware preparation:** confirm the ESP32 model, servo specifications, power requirements and mounting arrangement; test the mechanics separately.
3. **Desktop platform:** design and print the frame, integrate the ESP32 with two positional pan/tilt servos, and document measured results.
4. **ESP32-CAM upgrade:** purchase the camera board later, verify its video feed, and evaluate mounting and integration.
5. **Evaluation:** record tracking reliability, frame rate, latency, object-loss behavior and limitations with repeatable tests.

The built-in laptop webcam is fixed: rotating a separate platform does not rotate the webcam or center its image. Stage 1 therefore demonstrates tracking on screen. Camera-following experiments require a camera mounted on the moving platform. The planned vision-processing host remains the laptop; adding an ESP32-CAM does not automatically make processing standalone.

## Hardware planning
| Item | Status |
| --- | --- |
| Laptop and built-in webcam | First-stage camera and processing host |
| ESP32 | Available according to project discussion; exact board to confirm |
| 3D printer | Available according to project discussion |
| Two positional servos | Planned; MG996R was suggested, selection unverified |
| Separate regulated servo supply | Planned; rating to verify against selected components |
| Servo driver | PCA9685 was suggested; optional candidate |
| Frame, mounting hardware, cables and connectors | Inventory and design pending |
| ESP32-CAM | Later purchase and upgrade; exact module/programmer to confirm |

The earlier shopping suggestions are candidates, not a validated bill of materials. Record actual purchases and specifications before hardware integration. Detector choice is also pending; YOLO was discussed as an option, not an installed dependency.

## Project management
[Trello project board](https://trello.com/b/itvwndWJ/applied-robotics-and-ai-project)

Use To Do for planned tasks, In Progress for active work (maximum two cards), and Done for verified results. Add acceptance criteria and link commits or pull requests to cards. Keep genuine dated test records and short retrospectives; today's setup cannot establish earlier continuous use.

## Git setup and workflow
```sh
git clone https://github.com/kingdominick343-dev/c-ram-desktop-tracker.git
cd c-ram-desktop-tracker
git switch -c docs/workspace-demo
# Edit and save README.md.
git status
git diff
git add README.md
git diff --staged
git commit -m "Record verified project progress"
git push -u origin docs/workspace-demo
```
Configure your Git author identity and GitHub authentication before local commits and pushes. These commands are a guide, not a record of completed terminal work.

**Add** selects changes for the staging area. **Commit** records the staged snapshot locally. **Push** sends local commits to GitHub. Add and Commit can work offline; Push requires remote access. Uncommitted changes are not pushed.

Keep `main` as the reviewed baseline. Use descriptive task branches, review changes in pull requests, and link them to Trello. The existing `docs/assignment-01` branch is a workspace demonstration branch.

## Assignment 1
[Written Git discussion and demonstration checklist](Assignment_01_Git_Discussion.txt)

The video must demonstrate Trello and Git, including Clone, Edit, Add, Commit, Push and branching. Lecturer access, recording, and course submission remain to be confirmed. The assignment deadline is 20 October 2026, 11:30 pm Singapore time; this is not the completion deadline for the entire tracker.
