# Phase 1 – Hardware Selection & Procurement

> **Status:** ✅ Completed

## Overview

Every HomeLab starts with the same question:

**Which hardware should I buy?**

Instead of purchasing an expensive enterprise server or a brand-new Mini PC, I wanted to build a reliable and energy-efficient HomeLab while keeping the overall budget as low as possible.

Rather than buying the first device that looked attractive, I wanted to go through a realistic selection process. My goal was to compare different systems, talk to multiple sellers, verify the hardware before purchasing, and safely buy a second-hand Mini PC that could become the foundation of my HomeLab.

---

# Budget & Requirements

Before I started searching, I set myself a strict maximum budget of **250 €**.

Having a fixed budget helped me stay focused on finding the best value instead of chasing higher specifications that I didn't actually need.

I also created a simple framework that every candidate had to meet.

Minimum requirements:

- Low power consumption (24/7 operation)
- Hardware virtualization support
- AMD Ryzen 5 or Intel Core i5 (or better)
- Minimum 16 GB RAM
- Minimum 512 GB SSD
- Dual Gigabit Ethernet (preferred)

This prevented me from making impulsive buying decisions whenever I saw an attractive listing.

---

# Market Research

For about a week, I monitored the German second-hand market on **Kleinanzeigen**.

Every day I checked newly listed Mini PCs and compared them based on:

- CPU performance
- RAM capacity
- SSD size
- Power consumption
- Upgradeability
- Network interfaces
- Price
- Seller reliability

Whenever I found a promising device, I contacted the seller before making any decision.

---

# Communicating with Sellers

Before buying any second-hand computer, I always tried to collect as much technical information as possible.

Some of the questions I regularly asked were:

- Is the BIOS password protected?
- Has the computer ever been repaired?
- Could you send BIOS screenshots?
- Could you send a CPU screenshot from Task Manager?
- Could you send a CrystalDiskInfo screenshot showing the SSD health?
- Do you have the original invoice or proof of purchase?
- Is the device fully functional?
- Are you willing to sell using Kleinanzeigen Buyer Protection ("Sicher bezahlen")?

I noticed that honest sellers usually had no problem answering these questions or providing additional photos.

---

# Learning to Avoid Risks

This phase also taught me several important lessons.

One seller had a Mini PC that I really liked, but he only accepted a normal PayPal payment and refused to use Buyer Protection.

Although the hardware looked good, I decided not to continue because protecting my money was more important than getting the device.

Another seller suddenly stopped responding to my messages.

About a day later, Kleinanzeigen itself sent me a warning recommending that I should not purchase anything from that seller.

That experience confirmed that being patient is much safer than rushing into a purchase.

---

# Final Decision

After comparing multiple Mini PCs and talking to several sellers, I finally decided to purchase the following system:

| Component | Specification |
|-----------|---------------|
| Model | ACE MAGICIAN AM06PRO |
| CPU | AMD Ryzen 5 7430U (6 Cores / 12 Threads) |
| Memory | 16 GB DDR4 |
| Storage | 512 GB SSD |
| Network | Dual Gigabit Ethernet |
| Purchase Price | **200 €** |

I purchased the Mini PC using **Kleinanzeigen Buyer Protection (Sicher bezahlen)** so that the payment would remain protected until I had verified that everything matched the seller's description.

*(PHOTO)*

---

# Delivery

The Mini PC arrived about four days later.

The packaging was excellent and the device was well protected during shipping.

*(PHOTO)*

Because my long-term goal is to manage this server remotely, I didn't buy a dedicated keyboard, mouse, or monitor.

Instead, I temporarily connected the keyboard, mouse, and monitor that I normally use with my MacBook.

---

# Hardware Acceptance Test

Before doing anything else, I wanted to verify that the hardware really matched the seller's description.

The first thing I did was enter the BIOS and verify:

- CPU
- RAM
- SSD

Everything matched the advertised specifications.

*(BIOS PHOTO.)*

---

# Windows & SSD Verification

The Mini PC came with a reset Windows installation.

After completing the initial Windows setup, I installed **CrystalDiskInfo** to check the SSD.

The results were excellent.

- SSD Health: Good
- Power-On Hours: 23
- Power Cycles: 39
- No bad blocks detected

*(CrystalDiskInfo PHOTO.)*

---

# Functional Testing

Before confirming the purchase, I wanted to make sure that the system was stable.

I performed several basic tests, including:

- Watching 4K YouTube videos
- Opening multiple applications
- Checking general responsiveness
- Listening for unusual fan noise
- Looking for freezes or crashes

The Mini PC remained quiet, responsive, and completely stable throughout the testing process.

Once I was satisfied that everything was working correctly, I confirmed the delivery in Kleinanzeigen and released the payment to the seller.

This officially completed the procurement phase.

---

# Lessons Learned

This first phase taught me several valuable lessons.

- Define your budget before you start looking at hardware.
- Compare multiple devices instead of buying the first attractive option.
- Ask sellers for technical evidence before purchasing.
- BIOS screenshots and CrystalDiskInfo are extremely useful.
- Always use Buyer Protection whenever possible.
- Verify the hardware yourself before trusting the seller's description.
- A little patience can save both money and unnecessary problems.

---

The hardware procurement phase was successfully completed.

The Mini PC is now ready for the next step:

➡️ **Installing Proxmox VE**
