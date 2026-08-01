# Password-Strength-Checker-pcheckV2-

An end-to-end, terminal-native Python security toolkit designed to evaluate credential complexity, generate high-entropy deterministic passwords, and query globally leaked credential databases securely via **k-Anonymity**[cite: 1].

---

## Executive Summary

Modern authentication mechanisms heavily rely on text-based passwords. However, human cognitive constraints often yield predictable, low-entropy credentials vulnerable to brute-force, dictionary, and credential-stuffing attacks. 

`pcheckV2` provides a lightweight, three-tier security environment directly inside your CLI to audit, build, and verify password integrity without exposing cleartext credentials or full hash signatures to external networks.

---

## Features

-  Heuristic Password Strength Evaluator**: Audits input strings across a 5-point complexity matrix (Length, Uppercase, Lowercase, Numbers, and Special Characters).
- High-Entropy Password Generator**: Generates cryptographically varied pseudo-random password tokens with strict default overrides (enforcing a minimum 12-character fallback on short/invalid inputs).
-  Anonymized Breach Scanner (HIBP API Integration)**: Queries the *Have I Been Pwned* REST API using **k-Anonymity** (partial SHA-1 hashing) to check if credentials have been compromised in known data leaks.
-  Cross-Platform Terminal UI**: Features custom ANSI color coding and screen management compatible with Windows (`cls`) and Linux/macOS (`clear`).

---

##  System Architecture & k-Anonymity Model

To preserve absolute privacy during data breach checks, `pcheckV2` implements the **k-Anonymity Privacy Model**:
