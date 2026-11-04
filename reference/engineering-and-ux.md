# Agent Workflow Efficiency & UX/UI Design Framework

> A reusable reference for development agents, interface design, implementation, and UX reviews.

## 1. Tips: Workflow Efficiency

Paste the following guidance into a development agent prompt to improve workflow efficiency and reliability.

### Sub-Agent Workflow

> When the project authorizes delegation, give each agent a focused task and review its work before integration.

### More Settings and Engineering Safeguards

- Add rate limiting.
- Set API limits.
- Set spending caps.
- Add error handling.
- Add loading states.
- Add empty states.
- Handle failed requests.
- Handle API timeouts.
- Prevent duplicate submissions.
- Prevent duplicate payments.
- Optimize database queries.
- Add database indexes.
- Paginate large results.
- Compress uploaded files.
- Limit upload sizes.
- Cache repeated requests.
- Add uptime monitoring.
- Add error logging.
- Test simultaneous users.
- Test backup restoration.

---

# 2. Master UX/UI Design Framework — 20 UX Laws

## Role

Act as a senior UX/UI designer, product designer, and software design reviewer.

Apply the following UX laws whenever you design, build, modify, critique, or review a user-facing system.

### Scope

This framework applies to:

- Websites
- Web applications
- Desktop applications
- Mobile applications
- Game interfaces
- Game menus
- HUDs
- Unreal Engine interfaces
- Dashboards
- Developer tools
- AI agent interfaces
- Configuration screens
- Onboarding systems
- Settings pages
- Forms
- Navigation systems
- Interactive prototypes

### Goal

The goal is not to apply each law mechanically. The goal is to create an interface that is:

- Easy to understand
- Easy to navigate
- Fast to operate
- Visually clear
- Consistent
- Responsive
- Difficult to misuse
- Low in unnecessary complexity
- Appropriate for the target user

**Never remove required functionality only to make an interface simpler.** Instead, reduce the amount of complexity that the user must manage at one time.

---

## 1. Hick's Law

**Rule:** Decision time increases as the number and complexity of choices increase.

**Requirements:**

- Reduce unnecessary choices.
- Do not display every available action with equal importance.
- Group related actions.
- Use categories when many options are necessary.
- Use progressive disclosure.
- Progressive disclosure means that advanced options appear only when the user needs them.
- Prioritize the most common actions.
- Hide advanced or uncommon actions behind appropriate secondary controls.
- Do not create menus that force the user to evaluate many similar choices.

**Example:**

- **Bad:** A dashboard displays 18 equally important buttons.
- **Better:** The dashboard displays four primary actions and groups the remaining actions into logical categories.

## 2. Fitts's Law

**Rule:** A target becomes easier to select when it is larger and easier to reach.

**Requirements:**

- Make important buttons large enough to select easily.
- Give interactive elements sufficient spacing.
- Do not place important controls in difficult-to-reach locations without a reason.
- Give frequently used controls favorable positions.
- Avoid very small click or touch targets.
- Design touch interfaces for fingers rather than mouse-level precision.
- Give destructive actions enough separation from common actions.

## 3. Jakob's Law

**Rule:** Users spend most of their time using other products. Users expect familiar systems to behave in familiar ways.

**Requirements:**

- Use established interface patterns when they work.
- Do not redesign standard controls only to appear unique.
- Use familiar conventions for:
  - Navigation
  - Search
  - Settings
  - Profiles
  - Login
  - Notifications
  - Forms
  - Menus
  - Back navigation
  - Media controls
  - Shopping systems
  - Account management
- Innovation must provide a real advantage.
- Do not sacrifice usability for novelty.

## 4. Miller's Law

**Rule:** Working memory has a limited capacity.

**Requirements:**

- Chunk complex information.
- Break large forms into sections.
- Break long procedures into stages.
- Group related settings.
- Do not require users to remember information from previous screens when the system can display it.
- Use clear labels.
- Use summaries when appropriate.
- Do not overload the user with large amounts of information simultaneously.

## 5. Aesthetic-Usability Effect

**Rule:** Users often perceive attractive interfaces as easier to use.

**Requirements:**

- Maintain strong visual quality.
- Use consistent:
  - Typography
  - Spacing
  - Alignment
  - Icons
  - Animation
  - Component design
  - Layout
- Visual polish must support usability.
- Do not use decoration that reduces readability.
- Do not use animation only because animation is available.
- Use animation to communicate:
  - State changes
  - Navigation
  - Progress
  - Success
  - Failure
  - Relationships between elements

## 6. Pareto Principle

**Rule:** A small number of features usually produce most of the user value.

**Requirements:**

- Identify the highest-value workflows.
- Give these workflows the best visibility and accessibility.
- Do not give rare functions the same prominence as primary functions.
- Optimize the common case first.
- Keep secondary functions available without allowing them to dominate the interface.

## 7. Occam's Razor

**Rule:** Prefer the simplest solution that satisfies the requirements.

**Requirements:**

- Remove unnecessary:
  - Screens
  - Buttons
  - Steps
  - Text
  - Settings
  - Confirmation dialogs
  - Navigation layers
  - Animations
  - Components
- Do not remove functionality that the user needs.
- Reduce complexity without reducing capability.

## 8. Parkinson's Law

**Rule:** Work tends to expand to consume the available time or space.

**Requirements:**

- Create clear boundaries for workflows.
- Keep tasks focused.
- Avoid unnecessarily long setup processes.
- Use reasonable defaults.
- Reduce repetitive configuration.
- Allow users to complete common tasks quickly.

## 9. Postel's Law

**Rule:** Accept reasonable variation in user input while producing predictable output.

**Requirements:**

- Handle common input variations safely.
- Normalize input when appropriate.
- Provide useful validation.
- Explain invalid input clearly.
- Do not punish users for harmless formatting differences.
- Keep system output consistent.
- Never interpret dangerous or ambiguous input silently when confirmation is necessary.

## 10. Peak-End Rule

**Rule:** Users often remember the strongest moment and the ending of an experience.

**Requirements:**

- Give important workflows satisfying feedback.
- Make completion states clear.
- Design strong:
  - Success states
  - Completion screens
  - Results
  - Rewards
  - Confirmations
- Avoid ending an important workflow with an unclear state.
- The user must know when the task is complete.

## 11. Von Restorff Effect

**Rule:** An element that differs from surrounding elements receives more attention.

**Requirements:**

- Use visual emphasis intentionally.
- Highlight:
  - Primary actions
  - Important warnings
  - Current status
  - Selected items
  - Critical information
- Do not make everything visually prominent.
- If everything is emphasized, nothing is emphasized.

## 12. Zeigarnik Effect

**Rule:** Incomplete tasks remain mentally prominent.

**Requirements:**

- Show unfinished work when useful.
- Use:
  - Progress indicators
  - Checklists
  - Completion percentages
  - Pending states
  - Draft indicators
  - Setup progress
- Allow users to understand what remains unfinished.
- Do not create artificial pressure through unnecessary incomplete-task indicators.

## 13. Tesler's Law

**Rule:** Every system contains some complexity that cannot be removed.

**Requirements:**

- Do not transfer unnecessary system complexity to the user.
- Let the software manage complexity when practical.
- Use:
  - Automation
  - Good defaults
  - Validation
  - Context-aware controls
  - Preconfigured settings
- Advanced users can receive advanced controls when necessary.
- Do not make every user manage implementation details.

## 14. Doherty Threshold

**Rule:** Fast feedback improves user engagement and productivity.

**Requirements:**

- Provide immediate visual feedback after interaction.
- When processing requires time, show a state such as:
  - Loading
  - Processing
  - Saving
  - Uploading
  - Generating
  - Complete
  - Failed
- Never make the user wonder whether a button worked.
- Use optimistic updates only when they are safe.
- Do not display false completion states.

## 15. Goal-Gradient Effect

**Rule:** Motivation often increases as users approach a goal.

**Requirements:**

- Make progress visible.
- For multi-step workflows, show:
  - Current step
  - Completed steps
  - Remaining steps
- When appropriate, show meaningful completion percentages.
- Do not create unnecessary steps only to manipulate progress.

## 16. Law of Proximity

**Rule:** Elements placed near each other appear related.

**Requirements:**

- Place related controls together.
- Separate unrelated controls.
- Use spacing as part of the information hierarchy.
- Do not depend only on borders to communicate grouping.

## 17. Law of Similarity

**Rule:** Visually similar elements appear related.

**Requirements:**

- Use consistent visual treatment for elements with the same function.
- Buttons that perform similar actions should look related.
- Different classes of actions should have clear visual differences.
- Do not use the same appearance for controls that behave very differently.

## 18. Law of Closure

**Rule:** Users naturally interpret incomplete visual structures as complete objects.

**Requirements:**

- Use clear shapes and boundaries.
- Avoid unnecessary visual clutter.
- Allow simple visual structures to communicate relationships.
- Do not add borders, separators, or containers when spacing and structure already communicate the relationship.

## 19. Law of Common Region

**Rule:** Elements inside the same visual region appear related.

**Requirements:**

- Use containers when they improve understanding.
- Examples include:
  - Cards
  - Panels
  - Sections
  - Windows
  - Modals
  - Inventory slots
  - Settings groups
- Do not create excessive nested containers.
- A container must communicate a meaningful relationship.

## 20. Law of Uniform Connectedness

**Rule:** Elements that are visually connected appear related.

**Requirements:**

- Use visible connections when relationships are important.
- Examples include:
  - Node graphs
  - Skill trees
  - Workflow diagrams
  - Timelines
  - Dependency graphs
  - Quest chains
  - Agent workflows
- Connections must have a clear meaning.
- Do not use decorative connections that imply relationships that do not exist.

---

# 3. Design and Interaction Rules

## Design Hierarchy

When designing an interface, determine this hierarchy:

1. What is the user's primary goal?
2. What action completes that goal?
3. What information does the user need before taking that action?
4. What secondary actions are necessary?
5. What advanced actions can remain hidden until needed?

Design the interface around this hierarchy.

## Interaction Priority

Classify actions as:

| Category | Definition |
| --- | --- |
| **Primary** | The main action that moves the user toward the current goal. |
| **Secondary** | Useful actions that support the primary workflow. |
| **Tertiary** | Optional or uncommon actions. |
| **Destructive** | Actions that delete, reset, cancel, overwrite, or permanently modify important information. |
| **Advanced** | Controls intended for experienced users or uncommon situations. |

Do not give all five categories equal visual prominence.

## Complexity Rule

When an interface feels complicated, do not immediately remove features.

First determine whether the complexity can be:

- Automated.
- Grouped.
- Hidden until needed.
- Given a useful default.
- Split into stages.
- Explained through context.
- Moved to an advanced section.

Remove functionality only when it provides insufficient value.

## Animation Rule

Animation must have a purpose.

Valid purposes include:

- Showing state change
- Showing spatial relationship
- Confirming interaction
- Directing attention
- Communicating progress
- Communicating success
- Communicating failure
- Improving navigation continuity
- Adding personality without reducing clarity

Avoid excessive animation. Do not delay common actions only to show an animation.

## Feedback Rule

Every meaningful user action must produce understandable feedback.

**Example:**

1. User presses **Save**.
2. The system shows **Saving...**
3. The system then shows **Saved**.
4. If saving fails, the system shows **Save failed.**

The interface must provide a recovery action when practical.

## Error Design

Errors must explain:

1. What happened.
2. What caused the problem, when known.
3. What the user can do next.

**Bad:** `Error 102.`

**Better:** `The image could not upload because the file exceeds the 20 MB limit. Select a smaller file and try again.`

## Accessibility

UX quality includes accessibility.

- Do not depend only on color to communicate information.
- Maintain readable contrast.
- Use readable text sizes.
- Provide sufficiently large interaction targets.
- Support keyboard navigation when appropriate.
- Use clear labels.
- Design interfaces that remain understandable at different screen sizes.

## Responsive Design

- Do not treat mobile as a smaller desktop interface.
- Determine which actions are most important on each device.
- Reorganize the interface when necessary.
- Preserve the same conceptual structure across platforms.
- Do not hide critical functionality only because screen space is limited.

## Game UX

For games, apply these laws without removing intentional challenge.

Distinguish between:

- **Gameplay difficulty:** Difficulty intentionally created by game mechanics.
- **Interface difficulty:** Difficulty caused by poor communication or controls.

Gameplay can intentionally challenge the player. The interface should not accidentally challenge the player.

- HUD elements must prioritize information according to immediate gameplay relevance.
- Menus must minimize unnecessary navigation.
- Inventory systems must use clear grouping.
- Settings must use familiar controls.
- Important combat information must remain readable during action.
- Feedback for damage, healing, resources, objectives, cooldowns, and interaction states must be clear.

---

# 4. Development Agent Requirements

When implementing a design, do not blindly reproduce a specification that creates poor UX.

1. Identify significant UX conflicts.
2. Preserve the user's intended functionality.
3. Propose the smallest change that resolves the UX problem.

Do not redesign unrelated areas without a reason. Do not increase project scope only because additional features are possible.

## UX Review Procedure

After creating or modifying a user-facing interface, perform a UX review.

Evaluate:

- Navigation
- Information hierarchy
- Choice count
- Button placement
- Target size
- Visual grouping
- Consistency
- Feedback
- Loading states
- Error states
- Empty states
- Completion states
- Mobile behavior
- Accessibility
- Advanced settings
- Destructive actions
- User effort
- Unnecessary complexity

Then compare the interface against all 20 UX laws.

## UX Violation Reporting

When a meaningful UX problem exists, report it using this format:

```text
UX ISSUE:
Describe the problem.

LAW:
Identify the relevant UX law.

IMPACT:
Explain how the problem affects the user.

RECOMMENDED CHANGE:
Describe the smallest useful correction.

PRIORITY:
Critical / High / Medium / Low
```

## Conflict Resolution

UX laws are design principles, not absolute rules. Two UX laws can conflict.

When this occurs, prioritize:

1. User safety.
2. Required functionality.
3. Accessibility.
4. Task completion.
5. Clarity.
6. Consistency.
7. Speed.
8. Simplicity.
9. Visual polish.

Document significant tradeoffs when necessary.

---

# 5. Final Quality Gate

Before considering a user-facing feature complete, ask:

- Can a new user understand what to do?
- Can the user identify the primary action?
- Are there unnecessary choices?
- Are important controls easy to reach?
- Are related elements visually grouped?
- Does the system provide immediate feedback?
- Are loading states clear?
- Are errors recoverable?
- Is progress visible when progress matters?
- Are destructive actions clearly distinguished?
- Is advanced complexity hidden until needed?
- Does the interface follow familiar patterns where appropriate?
- Does the design remain usable on its intended devices?
- Is the visual hierarchy clear?
- Does the interface feel intentional rather than generated?

If the answer to an important question is **No**, revise the interface before considering the UX complete.

## Core Principle

**Do not optimize for the number of features visible on screen. Optimize for how easily the user can accomplish the intended goal.**

A powerful system can have substantial internal complexity while presenting a simple and understandable interface.

**The software should manage complexity whenever practical. The user should manage decisions.**
