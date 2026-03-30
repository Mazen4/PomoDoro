# Sequential Presentation Timer (PomoDoro)

## Overview
The **Sequential Presentation Timer** is a lightweight, standalone HTML application designed to optimize time management and maintain high engagement levels during technical training sessions. Built as a single-file solution, it requires no installation, making it ideal for Senior Pre-Sales Solutions Architects to use in diverse client environments where third-party software restrictions may apply.

The tool streamlines session delivery by providing a visual, automated timeline of training modules, ensuring that complex technical topics remain digestible for semi-technical audiences.

---

## Key Features

### 1. Dynamic Session Timeline
* **Visual Agenda**: The application visualizes the entire training agenda as a vertical timeline.
* **Status Tracking**: Each item displays its current status, whether it is Pending, Active, Completed, or Skipped.
* **Time Allocation**: Each task explicitly shows its specific time allotment in minutes.

### 2. Real-Time Progress Tracking
* **Active Task Monitoring**: A large, high-visibility countdown timer displays the remaining time for the current module.
* **Granular Progress Bars**: Each timeline item features an individual progress bar that fills in real-time as the session proceeds.
* **Overall Completion Metric**: A persistent header bar calculates the total project progress, accounting for both completed and skipped tasks.

### 3. Adaptive Session Control
* **Intelligent Skipping**: Allows the presenter to skip modules on the fly if the audience is moving faster than anticipated.
* **Automated Logic**: The timer automatically advances to the next scheduled task upon completion or when a skip is triggered.
* **Auto-Scroll UI**: The interface automatically scrolls to keep the active task in focus, ensuring the presenter never loses track of the schedule while demonstrating technical content.
* **Session Management**: Includes flexible controls to pause for unplanned deep-dive questions or to reset the entire training session.

---

## Technical Structure
The tool is built using a modern, responsive stack within a single file:
* **CSS3**: Utilizes CSS variables for consistent branding and a clean, professional "Card" UI.
* **Vanilla JavaScript**: Handles all timer logic, progress calculations, and DOM updates without external dependencies.
* **Responsive Design**: Optimized for different screen sizes, ensuring visibility on laptops or large conference room displays.

---

## Configuration
The training schedule is defined within the `schedule` array in the `<script>` section. You can easily customize the session by modifying the `name` and `minutes` properties for each object:

```javascript
const schedule = [
    { name: "Explain", minutes: 15, skipped: false },
    { name: "Practice", minutes: 5, skipped: false },
    { name: "Check In", minutes: 5, skipped: false },
    // Add additional modules here
];
