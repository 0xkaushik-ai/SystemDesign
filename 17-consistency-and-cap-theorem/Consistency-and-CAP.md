# Consistency and CAP Theorem

Consistency describes what value a reader sees after a write. Strong consistency returns the latest committed value; eventual consistency allows temporary differences that converge later.

CAP says that during a network partition, a distributed system must choose between consistency and availability. Partition tolerance is unavoidable in a distributed network.

Do not choose consistency blindly. Account balances and order state need stronger guarantees than likes, analytics, or cached recommendations.
