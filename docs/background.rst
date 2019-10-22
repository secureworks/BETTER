Background
==========

Problem
-------

As network bandwidth increases, attack methodologies expand, malicious
traffic patterns fluctuate, and IDS ruleset sizes grow, the ability
to programmatically understand the taxonomic and teleological
characteristics of each IDS rule becomes invaluable. The decades-old
practices of maintaining a rigid classification.config file and
segregating rules into distinct files is onerous, not scalable, and, in
many deployments, inviable for accurate ruleset tuning.
Simply enabling all available IDS rules is rarely wise, prudent, or
feasible for those concerned about rule performance, false-positives,
volume, and value. There needs to be an easy way to "slice and dice"
large rulesets so that they can be customized for each particular
deployment.

Solution
--------

Embed metadata key-value pairs in each rule that can be programmatically
consumed to enable powerful ruleset optimization.

