# VMAP
VMAP: Vehicular Misbehavior Detection Analysis and Evaluation Platform
VMAP is an extensible platform for detecting and reacting to misbehavior in vehicular ad-hoc networks (VANETs), built on [F2MD](https://github.com/josephkamel/F2MD)'s Basic Safety Message (BSM) attack/detection framework on top of [Veins](https://veins.car2x.org/).

VMAP combines trust-based detection at both the local (per-vehicle) and central authority levels, with the central authority additionally supporting machine-learning-based detection. The central authority is reachable over a real simulated wireless channel (802.11p), with generation and decision timestamps recorded for latency and decision-time analysis. The platform also includes new plausibility checks beyond stock F2MD, and resource-monitoring instrumentation at both the local and central levels for evaluating the practical cost of running detection at each layer.

## New features

- [] Local/Decentralized per-vehicle trust-based detection 
- [] Central trust authority over the real 802.11p wireless channel
- [] Local-vs-central decision-making toggle, switchable per scenario
- [] Generation/decision timestamps for latency and decision-time analysis
- [ ] New Trained ML-based detection at the central authority
- [ ] New plausibility checks
- [ ] Resource-monitoring instrumentation (local and central)
- [ ] Randomness (On-off Behaviour) added to attacks for simulating an Intelligent attacker


Code will be published soon.



Both local-only and central-authority modes are switchable per scenario via `.ini` configuration (`UseCentralAuthority = true/false`), with local-only remaining the default so existing scenario behavior is unaffected unless explicitly opted in.


VMAP would not exist without:

- [Veins](https://veins.car2x.org/) — the VANET simulation framework (SUMO + OMNeT++) this project runs on
- [F2MD](https://github.com/josephkamel/F2MD) — the original misbehavior attack/detection framework for the Basic Safety Message (BSM), including its local per-vehicle plausibility checks and `TrustApp`

## License

VMAP is derived from F2MD/Veins and is licensed under the GNU General Public License v2 (GPLv2). Original copyright notices in inherited source files are preserved; new files carry their own copyright notices.
