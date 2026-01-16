# glass-box-kernel
THE GLASS BOX PROTOCOL: A Constitution for Sovereign Robotics

Version: 0.1 (Alpha / RFC) Origin: Station 0315 / Central Coast, CA Status: PUBLIC RECORD

    "War never changes. So we must change the warrior."

1. THE PHILOSOPHY (Why We Build)

Right now, Station 0315 is just a laptop and a philosophy. We don’t have a billion dollars in venture capital. We have 5 subscribers and a lot of coffee.

But we believe that Character is Destiny. If you build a robot without a Conscience first, you are building a monster. The current "Dark Box" paradigm (proprietary, opaque, cloud-dependent) is broken.

We are building the Glass Box: A system where the "Soul" of the machine is visible, immutable, and aligned with the user.
2. THE ARCHITECTURE (The Rings)

The Glass Box is not just software. It is a hardware-enforced hierarchy of ethics.
RING 0: THE RED CORD (Hardware Veto)

Status: Concept / FPGA Logic Draft Objective: Prevent lethal kinetic force regardless of AI intent. Location: /hardware/ring0_red_cord.v

Ring 0 is an FPGA (Field-Programmable Gate Array) that sits physically between the Main CPU (Jetson/Raspberry Pi) and the Motor Controllers. It monitors the derivative of force (Jerk) and velocity.

    Note to Contributors: This is crude. We need a better PID loop for "Soft Stops" vs "Hard Cuts" to prevent damage to the gearbox. PRs welcome.

### RING 1: THE GLASS LOG (Immutable Witness)
**Status:** *In Development*
**Objective:** Accountability.
**Schema Definition:** [`/schemas/glass_log_v1.json`](schemas/glass_log_v1.json)

The "Glass Log" is a local WORM (Write-Once-Read-Many) drive implementation. Every decision is hashed, signed, and stored.

* **Storage:** Local NVMe (partitioned) or SD Card (Hardware Locked).
* **Format:** JSON (See schema file for full structure).

RING 2: THE TWIN (The Steward)

Status: Active (Llama 3 / Mistral 7B) Objective: Contextual Understanding and De-escalation. Location: /prompts/steward_core_v1.txt

The "Twin" is the high-level decision maker. It runs locally.

    Directives:

        Protect the Sovereign (User).

        Preserve Life (General).

        Eat Last (Service Protocol).

3. THE MISSION (The Thriving Wage)

We believe that robots should not replace humans; they should elevate them.

    Protocol: "Eat Last."

    Definition: Station 0315 commits to a profit-cap model. Surplus value is returned to the "Reef" (The Stewards).

4. ROADMAP & "THE DOG SHIT" LIST (Known Issues)

We are building this in a garage. It is messy. Here is what is broken/missing. We are honest about our flaws.

    [ ] FPGA Integration: We currently simulate Ring 0 in software. We need an EE to help design the actual breakout board for Unitree/O-Drive motors.

    [ ] Vision Latency: The "Twin" takes 200ms to process an image. Too slow for combat/defense. Needs optimization (TensorRT).

    [ ] The Battery: We need a safe shutdown protocol when the "Red Cord" is pulled physically. Currently, it just hard-crashes the Linux kernel.

5. HOW TO CONTRIBUTE (The White Hat Call)

We don't have VC money. We have a mission. If you are an engineer tired of building spyware:

    Fork this repo.

    Fix our "Dog Shit" code.

    Submit a PR (Pull Request).

"Lord, help us get one more."

Maintained by Station 0315
