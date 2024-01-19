# Personal Development Pseudocode

## Constants
- `MAX_CONSECUTIVE_DISTRACTION_HOURS`: 2
- `GOAL_YEAR`: 2018

## State Variables
- `consecutive_distraction_hours`: 0
- `goal_year_reached`: False
- `capstone_completed`: False

## Main Loop
```python
while True:
    display_thoughts("Reflect on personal journey and goals")

    if consecutive_distraction_hours >= MAX_CONSECUTIVE_DISTRACTION_HOURS:
        acknowledge_distraction_issue()
        break

    if has_reached_goal_year():
        goal_year_reached = True

    if goal_year_reached:
        if not capstone_completed:
            analyze_capstone_progress()
            if user_ready_to_commit():
                commit_to_capstone()
                capstone_completed = True
            else:
                consecutive_distraction_hours += 1
        else:
            display_thoughts("Feel accomplished. Capstone completed.")
            break
    else:
        reflect_on_past_decisions()
