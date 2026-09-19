# Packet-Level-Network-Intrusion-Detection-with-Machine-Learning
Multi-class attack detection and VPN / non-VPN classification on 20M+ packets, with an adversarial robustness analysis.
A complete ML-based Network Intrusion Detection System (NIDS) pipeline: raw .pcap / .pcapng captures are converted to a labelled dataset with Tshark, preprocessed, and used to train tree-based ensemble models (Random Forest, XGBoost). The trained models are then stress-tested with synthetic traffic and three adversarial attack strategies.

part of dataset from https://www.unb.ca/cic/datasets/vpn.html

Highlights
20,715,742 packets extracted from raw PCAP files and labelled automatically from filenames
9 traffic classes: 6 attack types plus VPN, non-VPN and unknown traffic
17 engineered features after preprocessing
Random Forest: 99.9998 % accuracy, XGBoost: 99.9977 % accuracy on held-out data
Adversarial analysis: a greedy hill-climb attack flips 74.2 % of attacked predictions

Random Forest 3-fold cross-validation (500,000-sample subset): 0.99992 ± 0.00001
XGBoost's weaker macro scores come from the two rarest classes: mitm (F1 ≈ 0.93) and unknown (F1 ≈ 0.88).
Most important Random Forest features: frame.time_epoch (0.336), ip.proto = ICMP (0.150), frame.len (0.108), udp.dstport (0.095).
