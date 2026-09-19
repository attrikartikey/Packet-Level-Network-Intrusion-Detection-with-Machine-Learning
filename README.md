# Packet-Level-Network-Intrusion-Detection-with-Machine-Learning
Multi-class attack detection and VPN / non-VPN classification on 20M+ packets, with an adversarial robustness analysis.
A complete ML-based Network Intrusion Detection System (NIDS) pipeline: raw .pcap / .pcapng captures are converted to a labelled dataset with Tshark, preprocessed, and used to train tree-based ensemble models (Random Forest, XGBoost). The trained models are then stress-tested with synthetic traffic and three adversarial attack strategies.
