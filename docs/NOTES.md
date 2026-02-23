# Notes to remeber

> High availability in AWS = design across AZs.

> Persist state before emitting side effects.

> AZ = resilience within a region; Region = disaster recovery, geo-distribution, regulatory separation

## Security Groups

Security groups are stateful meaning that if 443 port inbound is allowed, there will automatically be allowed outbound for response.

NACL is stateless meaning it does not remember anything and all reles must be defined explicitly

> Stateful SG = receptionist who lets the visitor in, and automatically lets them leave when done

>Stateless NACL = gate that only opens if you press the “IN” button and a separate
“OUT” button
