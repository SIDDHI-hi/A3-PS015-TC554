# NERVE
### Network Evidence, Reasoned Verification & Explanation

> **Explainable Home & Last-Mile Connectivity Diagnosis**

NERVE is an evidence-driven network diagnostic system designed to help users understand **where a connectivity problem is occurring, what evidence supports it, and whether a recommended fix actually worked.**

Instead of blindly running every network test or making unsupported guesses, NERVE uses **adaptive testing, deterministic reasoning, and verification** to build a defensible diagnosis.

---

## 🚨 The Problem

When someone says:

> **"My internet is slow."**

What does that actually mean?

The problem could be:

- Local Wi-Fi or interface issues
- Gateway / router problems
- DNS failures
- Packet loss or latency on a network path
- Congestion under load
- Endpoint-specific connectivity issues

Traditional speed tests mainly report **symptoms** such as bandwidth or latency. They do not explain **where the problem is, why it is happening, or whether a fix actually improved the situation**.

This creates a cycle of:

**Measure → Guess → Restart → Hope**

NERVE replaces this with:

**Measure → Reason → Test → Verify → Explain**

---

# 💡 Our Solution

NERVE treats network diagnosis as an **evidence-based reasoning problem**.

The system:

1. Captures the user's symptom and network context.
2. Runs targeted initial measurements.
3. Builds competing hypotheses from the evidence.
4. Uses deterministic rules to evaluate those hypotheses.
5. Selects the **next-best diagnostic test** when evidence is insufficient.
6. Stops when sufficient evidence exists.
7. Reports **Inconclusive** when the available evidence cannot support a reliable conclusion.
8. Verifies whether a recommended intervention actually improved the measured condition.

### The Core Idea

> **Don't run every test. Run the test that the evidence demands.**

---

# 🔄 NERVE Diagnostic Pipeline

```text
┌─────────────┐
│    SENSE    │
│ User symptom│
│ + context   │
└──────┬──────┘
       ↓
┌─────────────┐
│   MEASURE   │
│ Network     │
│ observations│
└──────┬──────┘
       ↓
┌─────────────┐
│   REASON    │
│ Hypotheses  │
│ + Rules     │
└──────┬──────┘
       ↓
   Evidence
   sufficient?
     ↙   ↘
   YES    NO
    ↓      ↓
 Finding  Next-best
    │       test
    │        │
    │        └───────┐
    ↓                │
┌─────────────┐      │
│   VERIFY    │◄─────┘
│ Confirm     │
│ diagnosis   │
└──────┬──────┘
       ↓
┌─────────────┐
│   REPORT    │
│ Evidence +  │
│ Explanation │
└─────────────┘
