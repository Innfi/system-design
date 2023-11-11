# Rate Limiter

# Requirements

- refine or limit external traffic to fixed rate traffic per given amount of time

# Questions

- what's the TPS? 
- is it burstable? (burst threshold ratio?)
- how to handle limited traffics?
  - discard and forget
  - backlog queue (for logging? or delayed handling)
- consistency
  - traffic rate should be consistent
- availability
  - single instance should be sufficient? or multiple instances are needed?
  - how to handle one instance per one request?
  - how to manage database for requests?
