---
layout: default
title: "FSM States & Transitions"
parent: "Enemy AI & Pluggable FSM"
nav_order: 1
---

# FSM States & Transitions

The AI core is orchestrated by `BaseStateMachine.cs`, `State.cs`, and `Transition.cs`.

---

## State Structure

A `State` contains two primary arrays:
- `FSMAction[] actions`: Operations executed every frame (`DoActions`).
- `Transition[] transitions`: Condition checks evaluated every frame (`CheckTransitions`).

```csharp
[CreateAssetMenu(menuName = "AS1/AI/State")]
public class State : ScriptableObject
{
    public FSMAction[] actions;
    public Transition[] transitions;

    public void UpdateState(BaseStateMachine controller)
    {
        DoActions(controller);
        CheckTransitions(controller);
    }

    private void DoActions(BaseStateMachine controller)
    {
        for (int i = 0; i < actions.Length; i++)
            actions[i].Act(controller);
    }

    private void CheckTransitions(BaseStateMachine controller)
    {
        for (int i = 0; i < transitions.Length; i++)
        {
            bool decisionSucceeded = transitions[i].decision.Decide(controller);
            if (decisionSucceeded)
                controller.TransitionToState(transitions[i].trueState);
            else
                controller.TransitionToState(transitions[i].falseState);
        }
    }
}
```
