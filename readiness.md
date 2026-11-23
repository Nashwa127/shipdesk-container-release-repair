# ShipDesk release readiness

- Author: Nashwa Arshad
- Candidate: 1.1.0
- Local image ID (not merely image tag): sha256:c9c9cc87870db328c7f25e420fd7a66c567acb707a2d9685b49e3f5549c1b41e
- Local /health and /config result: {"status": "ok"} {"service": "ShipDesk", "mode": "production", "version": "1.1.0"}
- Scope: LOCAL VALIDATION ONLY; approval NOT REQUESTED; NOT DEPLOYED to production.
- Hypothetical incident decision and two supplied signals: rollback . Rollback is chosen because request failures rose from 0.2% to 30% over ten minutes and most readiness checks failed, while previous release 1.0.0 is hhealthy and compatible with the current data/schema.
- Proposed post-recovery checks: After hypothetical recovery , verify /health and /config endpoint responses , confirm container healthlogs and reduced error rates , and check schema/data compatibility.

Final commit, annotated tag identity, successful Actions URL and matching
hosted commit go in submitted PDF AFTER this file is committed. Do not edit
this file to insert its own commit hash, avoiding a circular commit identity.
