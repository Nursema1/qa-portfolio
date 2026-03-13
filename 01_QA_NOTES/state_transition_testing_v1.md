# State Transition Testing

State transition testing verifies how a system behaves when moving from one state to another.

Example: Login system

States:
- Logged Out
- Logged In
- Locked

Transitions:
- valid login → Logged In
- logout → Logged Out
- multiple failed attempts → Locked

Purpose:
Detect incorrect behaviour during state changes.
