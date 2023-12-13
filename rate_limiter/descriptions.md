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

# Viable Options
- token bucket algorithm
  - good at refining bursting incoming traffics to a fixed rate
  - difficult to measure the sufficient size of the bucket 
  - question: how to handle rejected requests?
- leaky bucket algorithm
  - good at refining bursting incoming traffics to a fixed rate
  - time-demanding requests may take longer than SLA to process 
- fixed window counter
  - susceptable to bursting incoming traffics
- sliding window counter
  - good at assuring a long term maximum traffic rate
  - bursting traffics may cause a denial of service within the window unit
