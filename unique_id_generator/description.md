# Unique ID Generator

# Requirements

- generate unique ids in the context

# Questions

- what is the throughput number?
- how to handle collisions?
- define the context: 
  - is it a program, a machine (where multiple programs share), or a cloud?
- define uniqueness according to the context
  - are IDs need to be unique within the service, or the whole production env?
- define ID
  - is it digit-only? or alphanumeric?
  - minimum and maximum length
- define the lifetime
  - is unique ID always valid? or is it temporary?

# Viable Options
- UUID
  - 128-bit alphanumeric
  - low possibility of collision (but not zero)
  - id length may impact performance in terms of indexing, sorting, etc

- snowflake
  - 64-bit numeric
  - able to handle multiple generator instance
  - depends on system clock

- (what else?)