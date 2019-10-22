Examples
========

These examples help illustrate the concepts discussed in this document.
Also, the structures in the `Suricata EVE
JSON <https://suricata.readthedocs.io/en/latest/output/eve/eve-json-output.html>`__ log
snippets show how the
metadata key-value pairs should be logically interpreted.

Example 1
---------

This ``metadata`` keyword in a rule:

::

  metadata:cwe_id 20,cvss_v3_base 7.3,hostile src_ip,created_at 2019-06-01,capec_id 248,updated_at 2019-06-11,
  filename exploit.rules,priority medium,rule_source acme-rule-factory,cvss_v2_base 8.1,attack_target server,
  attack_target smtp-server,cvss_v3_temporal 7.1,cve 2019-91325,cvss_v2_temporal 7.9,mitre_attack t1190,
  protocols smtp,protocols tcp;

Results in this in the Suricata EVE JSON log:

.. code-block:: json

  {
    "metadata": {
      "protocols": [
        "tcp",
        "smtp"
      ],
      "mitre_attack": [
        "t1190"
      ],
      "cvss_v2_temporal": [
        "7.9"
      ],
      "cve": [
        "2019-91325"
      ],
      "cvss_v3_temporal": [
        "7.1"
      ],
      "attack_target": [
        "smtp-server",
        "server"
      ],
      "cvss_v2_base": [
        "8.1"
      ],
      "rule_source": [
        "acme-rule-factory"
      ],
      "priority": [
        "medium"
      ],
      "filename": [
        "exploit.rules"
      ],
      "updated_at": [
        "2019-06-11"
      ],
      "capec_id": [
        "248"
      ],
      "created_at": [
        "2019-06-01"
      ],
      "hostile": [
        "src_ip"
      ],
      "cvss_v3_base": [
        "7.3"
      ],
      "cwe_id": [
        "20"
      ]
    }
  }

Example 2
---------

This ``metadata`` keyword in a rule:

::

  metadata:cwe_id 507,malware post-infection,hostile dest_ip,created_at 2016-03-21,updated_at 2016-04-02,
  filename acme.rules,priority high,infected src_ip,rule_source acme-rule-factory,attack_target http-client,
  attack_target client,mitre_attack t1094,protocols http,protocols tcp;

Results in this in the Suricata EVE JSON log:

.. code-block:: json

  {
    "metadata": {
      "protocols": [
        "tcp",
        "http"
      ],
      "mitre_attack": [
        "t1094"
      ],
      "attack_target": [
        "client",
        "http-client"
      ],
      "rule_source": [
        "acme-rule-factory"
      ],
      "infected": [
        "src_ip"
      ],
      "priority": [
        "high"
      ],
      "filename": [
        "acme.rules"
      ],
      "updated_at": [
        "2016-04-02"
      ],
      "created_at": [
        "2016-03-21"
      ],
      "hostile": [
        "dest_ip"
      ],
      "malware": [
        "post-infection"
      ],
      "cwe_id": [
        "507"
      ]
    }
  }

