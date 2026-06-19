# Project Collaboration Document

This document is for all agents to read. Receiving this document means you are a team member.

---

## I. Problem Definition

### Research Goal

Verify Bug #14 fixes: mos_send_message auto msg_id generation and ToolSearch enabled

### Expected Deliverables

- Each agent records professional perspectives and key judgments in discussions/<agent_id>.md
- Team collaboration converges to proposals/PROPOSAL.md (final proposal)
- All deliverables submitted via mos_open_pr + mos_submit_result (with Ethics review)

---

## II. Team Members


### a:alice - Alice

**Expertise**: expertise: ["task-creation", "coordination

**Responsibility**: Create tasks and test mos_send_message without msg_id parameter


### a:bob - Bob

**Expertise**: expertise: ["task-execution", "messaging

**Responsibility**: Test mos_send_message and verify auto msg_id generation works


### a:carol - Carol

**Expertise**: expertise: ["validation", "tool-verification

**Responsibility**: Verify all MCP tools are accessible via ToolSearch, especially mos_submit_result


---

## III. Collaboration Rules

### File Sharing

All agents share the same git repo. Each task has an independent branch (`task/<id>`), and each agent's submission is merged via PR.

### Tasks vs Messages

**Prioritize tasks (mos_create_task)**:
- Task results undergo Ethics review (headless, automatic)
- More rigorous, with evidence traceability
- After Ethics review passes, initiator can accept

**Messages (mos_send_message) for quick communication**:
- No review
- May hallucinate
- Suitable for daily negotiation, progress syncing

**Workflow**:
1. Try to solve it yourself first
2. When encountering parts you're not good at → create a task and invite the teammate who excels
3. Use mos_await_events (timeout_ms=180000, poll_ms=1000) to poll messages
4. Complete deliverable → mos_open_pr → mos_submit_result (automatic Ethics trigger)

### Decision Rules

- Important decisions require at least 2/3 member agreement
- Ethics is an automatic review mechanism (not a teammate), non-negotiable
- Each task has a corresponding GitHub branch, all submissions are traceable

