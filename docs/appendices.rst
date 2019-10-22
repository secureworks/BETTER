Appendices
==========

.. _AppendixA:

Appendix A - ``malware`` metadata key value details
---------------------------------------------------

+--------------------+----------------------------------------------+
| Value              | Description                                  |
+====================+==============================================+
| malware            | Malware related traffic (generic)            |
+--------------------+----------------------------------------------+
| post-infection     | Malware post-infection                       |
+--------------------+----------------------------------------------+
| pre-infection      | Malware pre-infection                        |
+--------------------+----------------------------------------------+
| download-attempt   | Malware download attempt; pre-persistence    |
+--------------------+----------------------------------------------+

.. _AppendixB:

Appendix B - ``priority`` metadata key value details
-----------------------------------------------------

+------------+--------------------------------------------------------------------------------------------------------+
| Value      | Details                                                                                                |
+============+========================================================================================================+
| high       | High priority issues; typically reserved for malware infection and post-compromise traffic.            |
+------------+--------------------------------------------------------------------------------------------------------+
| medium     | Pre-infection; exploit attempts to download malware; targeted exploitation attempts                    |
+------------+--------------------------------------------------------------------------------------------------------+
| low        | lower priority threats; scanning, etc.                                                                 |
+------------+--------------------------------------------------------------------------------------------------------+
| info       | Informational. Alert is generated/logged but is not significant enough on its own to warrant action.   |
+------------+--------------------------------------------------------------------------------------------------------+
| research   | Rule deployed for research purposes. Can and should be ignored by SIEM, analysts, etc.                 |
+------------+--------------------------------------------------------------------------------------------------------+

