---
layout: default
title: Leonard
permalink: /leonard/
---

# Engineering Sustainable Performance: The 2026 F1 Hybrid Power Unit

## Leonard

# Can Formula 1 Be Fast *and* Net-Zero?

# Can Formula 1 Be Fast *and* Net-Zero?

By 2030, Formula 1 wants to be **net-zero carbon** (Formula 1, 2024; Baldwin, 2024).  
From 2026, the cars get a new kind of **hybrid powertrain** that (Fédération Internationale de l'Automobile, 2024; Racecar Engineering, 2024; Red Bull Racing, 2024):

- Uses **100% “drop-in” sustainable fuel** (synthetic / bio-based fuel that can run in normal-style engines) (Baldwin, 2024; Stepien, 2025).
- Gets about **half its power from electricity** and half from the fuel-burning engine (Fédération Internationale de l'Automobile, 2024; Aston Martin F1 Team, 2025).

This page walks through the main design challenges explained in **plain English** (Vasudev, 2025; Stepien, 2025):

- How the **engine and electric side share power**.
- How the car **keeps everything cool** (Vasudev, 2025).
- How the car **recycles energy** from braking and exhaust (Vasudev, 2025).

---


![Cool Sketch of Mercedes Car from Mercedes-AMG Petronas F1 Team](/assets/Cool-Mercedes-F1-Car-Sketch.jpg)

> Sketch of the F1 Mercedes-AMG from official Mercedes-AMG social media page
---

## 1. What Is an F1 Powertrain?

### 1.1 “Powertrain” in one sentence

The **powertrain** is everything that takes **energy** (fuel + electricity) and turns it into **force at the wheels** (Vasudev, 2025).

Think of it as the car’s **muscle system**:
- The **engine** is the burning-muscle part.
- The **battery + electric motor** is the electric-muscle part.
- The **control electronics** are the brain that coordinates them (Vasudev, 2025).

### 1.2 The main pieces

In the current hybrid era, an F1 power unit has (Vasudev, 2025; Stepien, 2025):

- **Internal Combustion Engine (ICE)**  
  A tiny 1.6L turbo V6. It burns fuel, makes noise, and does most of the work today (Red Bull Racing, 2024).

- **Turbocharger**  
  A little air compressor spun by exhaust gas. It forces more air into the engine so you can burn more fuel and make more power (Vasudev, 2025).

- **MGU-K (Motor Generator Unit – Kinetic)**  
  An electric machine connected to the crankshaft.
  - On **braking**, it acts like a generator: it slows the car a bit and charges the battery.
  - On **acceleration**, it acts like a motor: it pushes the car with electric power (Vasudev, 2025; Stepien, 2025).

- **MGU-H (Motor Generator Unit – Heat)** *(being removed from 2026)*  
  Connected to the turbo.
  - It can harvest energy from the spinning turbo.
  - It can also spin the turbo to reduce “turbo lag” (Fédération Internationale de l'Automobile, 2024; Racecar Engineering, 2024).

- **Energy Store (Battery)**  
  High-power lithium-ion pack. Not huge like a road EV, but it can deliver and absorb big bursts of power (Vasudev, 2025).

- **Power Electronics / Control Unit**  
  Decides how electricity flows between battery, MGU-K, MGU-H, and sometimes directly from exhaust to wheels (Vasudev, 2025).

### 1.3 Old vs new balance

Right now, roughly:
- **~80%** of power: from the engine.
- **~20%**: from the electric side. 

From **2026**, the rules push toward:
- **~50% engine, ~50% electric**, plus 100% sustainable fuel (Fédération Internationale de l'Automobile, 2024; Formula 1, 2024; Aston Martin F1 Team, 2025). 

That means the electric side is no longer just “extra boost” – it’s half the show.


---

![F1 V6 powertrain diagram with labels](/assets/V6-Powertrain.jpg)

> V6 Powertrain by Honda
---

## 2. What “Net-Zero” and “Drop-In Sustainable Fuel” Actually Mean

### 2.1 What is “net-zero” in F1?

## 2. What “Net-Zero” and “Drop-In Sustainable Fuel” Actually Mean

### 2.1 What is “net-zero” in F1?

**Net-zero** doesn’t mean “no emissions from the exhaust pipe.”  
It means that, over a year, the **total CO₂ released** is **balanced** by:

- Cutting emissions where possible (more efficient engines, less fuel) (Baldwin, 2024; Fédération Internationale de l'Automobile, 2024).
- Using **sustainable fuel** made from carbon that was already in the cycle (air, waste, biomass) (Stepien, 2025; Vasudev, 2025).
- Offsetting the rest with other projects (Formula 1, 2024).

For the **powertrain**, that means:

> “No **new** fossil carbon from underground. The carbon in the fuel should come from stuff that was already above ground” (Stepien, 2025; Aston Martin F1 Team, 2025).

### 2.2 What is 100% “drop-in” sustainable fuel?

“**Drop-in**” means the fuel:

- Can be **used in normal-style gasoline engines** with only small tweaks (Aston Martin F1 Team, 2025; FIA, 2024).
- Can flow through **existing fuel distribution** systems (tanks, pipes, trucks) (Red Bull Racing, 2024).

Where can this carbon-neutral fuel come from?

- **Captured CO₂** from the air or industrial fumes (Stepien, 2025).
- **Waste biomass** (like leftovers from farming, not food crops) (Vasudev, 2025).
- **Municipal waste** (garbage that would otherwise rot or be burned) (Stepien, 2025).

The CO₂ that comes out the **exhaust** was already in the atmosphere or waste stream recently, so you’re not adding new CO₂ from underground oil (Formula 1, 2024; Stepien, 2025).

### 2.3 Why fuel makes engineers sweat

Sustainable fuel is not just “normal gasoline but a nicer color.” It:

- Can burn **faster or slower** (Vasudev, 2025).
- Can change the **flame temperature and pressure** (Vasudev, 2025; Racecar Engineering, 2024).
- Can change how hot the exhaust and turbo run (Racecar Engineering, 2024).

That means:
- You may need to redesign **combustion chambers** and **injectors** (Fédération Internationale de l'Automobile, 2024; Aston Martin F1 Team, 2025).
- You must retune the **engine mapping** (timing, fuel flow, boost) (Vasudev, 2025; Red Bull Racing, 2024).
- All of that affects **heat**, **efficiency**, and **reliability** (Vasudev, 2025; Racecar Engineering, 2024).

So the “green fuel” question is really:

> “Can we make fuel that’s friendly to the planet **and** friendly to a tiny, screaming 15,000 rpm engine?” (Baldwin, 2024; FIA, 2024).

---

## 3. Design Challenge #1 – Hybrid Integration: Sharing Power Without Chaos

The new F1 car basically has **two engines**:

- One that burns **fuel** (ICE).
- One that uses **electricity** (MGU-K + battery) (Vasudev, 2025; Fédération Internationale de l'Automobile [FIA], 2024).

They have to **share the work** while:

- Staying within power limits (FIA, 2024; Formula 1, 2024).
- Saving fuel (Stepien, 2025).
- Not cooking the engine or battery (Vasudev, 2025).

### 3.1 Mental model: runner + e-scooter

Imagine:

- A **runner** (the engine) doing most of the work.
- An **electric scooter** (the motor) that can:
  - Push the runner on straights.
  - Charge itself when going downhill (braking) (Vasudev, 2025; Racecar Engineering, 2024).

The big question is always:

> “Who should work harder **right now**: runner or scooter?”

### 3.2 Control problem: who does what, when?

The control system (software + hardware) needs to decide, every split second:

- On **acceleration**:
  - How much power comes from the engine?
  - How much extra push from the electric motor? (FIA, 2024; Aston Martin F1 Team, 2025)

- Under **braking**:
  - How much braking is done by MGU-K (regeneration)?
  - How much by normal hydraulic brakes, so the car stays stable? (Vasudev, 2025)

- On **straights**:
  - Should the car **spend** stored electrical energy to go faster?
  - Or **save** it for later corners or overtakes? (Baldwin, 2024; Red Bull Racing, 2024)

With the 2026 push to roughly **50/50 engine–electric power**, bad decisions here can lose **tons of lap time** (Baldwin, 2024; Formula 1, 2024).

### 3.3 Why 50/50 is a big deal

When electric power was only ~20%:

- Teams could treat it as a **bonus**: helpful, but not life-or-death.

With ~50% electric:

- You **cannot** reach full performance without using the electric side properly (FIA, 2024; Aston Martin F1 Team, 2025).
- Energy management becomes as important as classical engine tuning (Vasudev, 2025).

This era also adds a new element: **manual electric boost** for the driver (Red Bull Racing, 2024).

Under the new rules, the driver can activate a temporary, extra-power electric “overtake” mode. This gives a burst of acceleration for defending or attacking another car. However, the driver does not directly control how much power comes from the battery — they only request it. The car’s control system still decides the exact power flow to protect the battery, manage temperature, and stay within regulations (FIA, 2024; Aston Martin F1 Team, 2025).

### 3.4 Trade-offs

A few ways to mess this up:

- **Overspending electric early in the lap**  
  - Car feels amazing at the start of the lap.
  - Battery runs low later, so you’re a sitting duck on the straight (Vasudev, 2025; Baldwin, 2024).

- **Over-harvesting (charging too hard)**  
  - You drag the engine (or brakes) more to recharge the battery.
  - That slows the car and adds **extra heat** in both engine and battery (Vasudev, 2025).

- **Conservative strategy**  
  - You keep plenty of energy in the battery.
  - But you’re leaving free lap time on the table (Stepien, 2025; Red Bull Racing, 2024).


---


![F1 hybrid powertrain blocks](/assets/ERS-Austria-Qualifying-Lap.jpg)

> Energy Recovery of Austria Qualifying Lap

---

## 4. Design Challenge #2 – Thermal Management: The Heat Problem

Every time you **convert energy**, you make **heat** (Vasudev, 2025).  

Modern F1 power units can hit **~50% thermal efficiency**, which is insanely high, but that also means the **other half** of the fuel’s energy is mostly heat (Vasudev, 2025; Stepien, 2025).  

Now add:

- High-power battery.
- Motor-generators.
- Power electronics (Vasudev, 2025; Federation Internationale de l'Automobile [FIA], 2024).

You’ve just built a **portable oven** that happens to go 300 km/h (Racecar Engineering, 2024).

### 4.1 Where the heat comes from

Heat sources include:

- **Engine combustion** – hot gases, hot pistons, hot everything (Stepien, 2025).
- **Turbo and exhaust** – exhaust gases can be hundreds of degrees (Baldwin, 2024; Racecar Engineering, 2024).
- **Battery** – gets hot when charging and discharging fast (Vasudev, 2025).
- **MGU-K motor** – electric machines are not 100% efficient (Vasudev, 2025; FIA, 2024).
- **Power electronics** – inverters, DC-DC converters (Vasudev, 2025).
- **Brakes** – kinetic energy turned into heat at the discs (Stepien, 2025).

### 4.2 Cooling without sacrificing speed

To remove heat, you need:

- **Radiators and coolers** – water, oil, battery coolant, etc. (Racecar Engineering, 2024).
- **Airflow** over those coolers (Formula 1, 2024).

The catch:

- More air → **more drag** → slower on straights (Formula 1, 2024; Aston Martin F1 Team, 2025).
- Bigger radiators → **more weight and more space** → harder packaging (Red Bull Racing, 2024).

### 4.3 New challenges with more electric + new fuel

- More **electric power** → more **battery current** → more battery heat (Vasudev, 2025; FIA, 2024).
- More **regenerative breaking** → more hot brakes, more hot MGU-K, more hot electronics (Vasudev, 2025).
- **Sustainable fuel** may change:
  - Exhaust temperature.
  - How heat is distributed between engine, turbo, and exhaust (Stepien, 2025; Baldwin, 2024). 

That means:

- You might need more or different **cooling circuits** (Racecar Engineering, 2024).
- You might have to rethink how hot air leaves the car so it doesn’t **reheat** other components (Aston Martin F1 Team, 2025).

### 4.4 The cooling–drag–weight triangle

You can picture a three-way tug-of-war:

- **Cooling** – bigger radiators, more airflow (Formula 1, 2024).
- **Drag** – smooth, tight bodywork wants less airflow and smaller openings (Red Bull Racing, 2024).
- **Weight** – more radiators, more fluid, more structure (FIA, 2024).

You can’t maximize all three (Aston Martin F1 Team, 2025). Typical trade-offs:

- Add cooling:
  - ✅ safer temperatures  
  - ❌ more drag and weight → slower lap (Racecar Engineering, 2024).
- Reduce cooling:
  - ✅ less drag, more top speed  
  - ❌ risk of overheating – car has to back off or breaks (Vasudev, 2025).

### 4.5 What happens if they get it wrong?

Symptoms of bad thermal management:

- Driver gets messages like “cool the car” → must lift off the throttle and coast (Baldwin, 2024).
- Engine power gets reduced automatically to protect hardware (FIA, 2024).
- Battery temp goes high → power output or regenerative breaking gets limited (Vasudev, 2025).
- In worst cases: **DNF** (engine/battery failure) and millions of dollars go poof (Racecar Engineering, 2024).


---


## 5. Design Challenge #3 – Energy Recovery: Recycling Speed

Before talking about batteries or motors, here is the simple physical idea.

When any car slows down, it is throwing away energy.

That moving car contains **kinetic energy** (the energy of motion). In a normal car, braking turns almost all of that energy into **useless heat** in the brake pads and rotors.

Formula 1 tries to steal some of that “wasted” energy back (Vasudev, 2025).

It does this using an electric machine that can work in reverse (Vasudev, 2025).

### 5.1 What is regenerative braking? 

An electric motor can also act as a **generator**.

- As a motor → it uses electricity to spin the wheels.
- As a generator → it resists the wheels and creates electricity.

So when the driver hits the brakes, part of the braking force in an F1 car does NOT come from brake pads.

Instead, it comes from the electric motor “pushing back” against the wheels and turning that motion into **stored electrical energy in the battery** (Vasudev, 2025; Fédération Internationale de l'Automobile, 2024).

This is called **regenerative braking (regen)**.

Think of it like: Instead of grinding away speed as heat, the car is trying to store that speed for later.

---

### 5.2 The critical problem: regen acts on the REAR wheels only

The regenerative motor (called the **MGU-K**) is connected to the engine and drivetrain, which drive the **rear wheels** (Fédération Internationale de l'Automobile, 2024).

That means:
- Front wheels: slow down using brake pads only
- Rear wheels: slow down using **brake pads + electric motor resistance**

This creates an imbalance during braking.

The physics shows:

When you brake hard, the car’s weight shifts **forward**.
This means:
- Front tires get **more grip**
- Rear tires get **less grip**

So you now have a dangerous situation:

The tires with **the least grip** (rear tires)
are being asked to **do the most braking** (pads + regen motor).

If the motor resists even a little too much:
- Rear wheels slow down faster than the front
- Rear tires lose grip
- The back of the car starts to slide or spin

That is why regen is risky in a race car because **it only acts on the weakest end of the car during braking** (Vasudev, 2025).

This is why “brake blending” is so critical (Vasudev, 2025; Racecar Engineering, 2024).

---

### 5.3 What is brake blending? (And why it’s insanely hard)

The driver presses **one brake pedal**.

But the car is actually doing two different types of braking:

1) Regular hydraulic brakes (pads and discs)
2) Electric regenerative braking (MGU-K)

The computer must blend them perfectly so the driver feels:
One smooth, predictable stopping force (Vasudev, 2025).

If the blend is even a little bit off:
- Braking feels weird
- Rear slides, locks, or steps out
- Driver loses confidence
- Lap time dies (or wall is introduced to side of car)

This blending has to be adjusted constantly based on:
- Tire grip
- Speed
- Battery charge
- Temperature
- Track surface
- Driver input

That is why dozens of engineers obsess over this system (Racecar Engineering, 2024; Aston Martin F1 Team, 2025).

---

### 5.4 The machines that do the energy recovery

Here are the parts that do it regen:

![Diagram of F1 hybrid powertrain](assets/Motor-Generator-Unit-Diagram.jpg)

- **MGU-K (Motor Generator Unit – Kinetic)**  
  Connected to the drivetrain and rear wheels.
  - On braking → it becomes a generator and charges the battery
  - On acceleration → it becomes a motor and boosts the car (Fédération Internationale de l'Automobile, 2024)

- **MGU-H (Motor Generator Unit – Heat)** *(used in current system, removed in 2026)*  
  Connected to the turbo.
  - It harvests energy from hot exhaust
  - It can send energy:
    - to the battery, or
    - directly to the MGU-K (skipping the battery and reducing losses) (Baldwin, 2024; Formula 1, 2024)

This is why F1 is so special:  
It is stealing energy from **both** braking **and** exhaust heat — two places normal cars completely waste (Stepien, 2025).

---

### 5.5 How much energy can actually be recovered?

On a typical lap:

- The MGU-K can recover about **20% of the car’s braking energy** on average (Vasudev, 2025; Stepien, 2025)
- Some tracks allow more (lots of slow corners and opportunities to brake)
- Some tracks allow less (fast flowing corners or longer straights)

But recovery is always limited by:

- Tire grip (too much regen = spin risk)
- Battery temperature and capacity
- Rules set by the FIA (Fédération Internationale de l'Automobile, 2024)
- Overall balance of the car

---

### 5.6 The strategy problem: harvest, save… or smash the boost button

The harvested energy is stored in the battery. That stored energy is the car’s **secret weapon** (Aston Martin F1 Team, 2025).

It can be used to:

- Boost out of corners
- Defend a position
- Attack for an overtake
- Reduce fuel use by backing off the engine

Under the new rules, the driver has access to a **manual electric boost button** (often called “overtake” mode) (Formula 1, 2024; Red Bull Racing, 2024). 

The important part is:
The driver does NOT directly control how much power comes from the battery.  
They only **request it**. The car’s computer still decides the exact amount, based on:

- How full the battery is
- How hot the battery and motor are
- What the rules allow (Fédération Internationale de l'Automobile, 2024)
- Whether giving full boost is safe

So the driver’s role becomes **strategic**, not technical.

They have to decide things like:

- Do I use boost now to pass this car?
- Or do I save it for the long straight in Sector 3?
- Do I defend my position, or gamble it for later?

Meanwhile, the system is deciding:

- Do we recover MORE energy into the battery right now?
- Or do we reduce regen to protect rear grip and stability? (Vasudev, 2025)
- Do we allow maximum boost?
- Or do we limit it because the battery is too hot?

This turns energy recovery into a **resource management game** shared between:
- The driver (when to use it)
- The engineers (how it’s programmed)
- The car’s computer (how it’s executed) (Aston Martin F1 Team, 2025; Stepien, 2025)

---


![Jeddah Corniche Circuit in Saudi Arabia](/assets/Saudi-Arabia-Circuit.jpg)

> Jeddah Corniche Circuit in Saudi Arabia

---

## 6. Putting It All Together: System-Level Trade-Offs

### 6.1 Scenario 1 – Hot race, twisty track

Imagine:

- A very hot day.
- A twisty street circuit with lots of slow corners and heavy braking.

What happens?

- Lots of braking → lots of energy recovery → **battery and MGU-K heat up** (Vasudev, 2025).
- Brakes also get hotter (Vasudev, 2025).
- Engine runs hot because air temps are high (Vasudev, 2025).

To keep things safe, engineers might:

- **Open up the cooling** (bigger air inlets, different bodywork) (Formula 1, 2024; Racecar Engineering, 2024):
  - ✅ Lower temperatures.
  - ❌ More drag → slower on straights (Racecar Engineering, 2024).

- **Harvest a bit less energy**:
  - ✅ Less battery and brake heat (Vasudev, 2025).
  - ❌ Less electric boost later → slower lap times (Vasudev, 2025).

So they have to decide:

> “Do we want *maximum* performance for a few laps, or *very high* performance for the whole race without cooking the car?”

### 6.2 Scenario 2 – Qualifying lap vs race stint

- **Qualifying** (one or two flying laps):
  - Use **aggressive hybrid strategy** (Aston Martin F1 Team, 2025).
  - Spend more battery, accept higher temperatures for a short time (Vasudev, 2025).
  - Maybe run tighter bodywork for less drag, gambling that the car won’t overheat in just a few laps (Formula 1, 2024).

- **Race stint** (dozens of laps):
  - Dial back power slightly (Aston Martin F1 Team, 2025).
  - Use **more conservative energy recovery and boost** (Vasudev, 2025).
  - Run more cooling to keep things in a safe window (Racecar Engineering, 2024).

Same hardware, completely different settings because the **time horizon** is different.

### 6.3 Big-picture trade-offs

You can think of three big sliders:

1. **Speed vs Efficiency**
   - Go flat-out → burn more fuel, run hotter, use more battery cycles (Vasudev, 2025).
   - Drive slightly under the limit → save fuel, keep temps in check, maybe have more power at the end (Stepien, 2025).

2. **Complexity vs Reliability**
   - Super advanced control software → brilliant when it works, but harder to calibrate and debug (Vasudev, 2025; FIA, 2024).
   - Simpler strategies → more robust, but might miss the last few tenths (Aston Martin F1 Team, 2025).

3. **Performance vs Sustainability goals**
   - F1 wants:
     - Net-zero carbon (Stepien, 2025).
     - Engines and fuels that teach us something useful for road tech (Stepien, 2025; FIA, 2024).
   - But fans expect:
     - Ridiculous lap times (Baldwin, 2024).
     - Wheel-to-wheel racing (Formula 1, 2024).
     - Reliability good enough that championships aren’t decided by random explosions (Red Bull Racing, 2024).

The engineering question is:

> “Can we design a powertrain that helps the planet **and** still scares the driver a little on every lap?”

---

## 7. Why This Matters Beyond F1

F1 is an extreme, expensive sandbox. But the lessons don’t stay on the track (Baldwin, 2024; Fédération Internationale de l'Automobile [FIA], 2024).

### 7.1 Lessons for road cars

Things that can trickle down:

- **Better hybrid strategies**  
  - Smarter software that decides when to use engine vs electric (Vasudev, 2025; Stepien, 2025).
  - Smoother blending of regen and hydraulic brakes (Aston Martin F1 Team, 2025).

- **Thermal management tricks**  
  - Compact, efficient coolers (Vasudev, 2025).
  - Smarter coolant routing and control (Vasudev, 2025; Racecar Engineering, 2024).

- **Sustainable fuels**  
  - If F1 proves that truly high-performance engines can run on **drop-in sustainable fuel**, that’s a big data point for aviation, shipping, and legacy cars that can’t easily go full EV (Stepien, 2025; Red Bull Racing, 2024; Formula 1, 2024). 

### 7.2 F1 as a “lab on wheels”

Why do car companies care?

- They get to test ideas in **the harshest possible environment** (FIA, 2024; Aston Martin F1 Team, 2025):
  - Tiny engines making huge power (Baldwin, 2024).
  - Massive power density in batteries and motors (Vasudev, 2025).
  - High vibration, high temperature, long races (Racecar Engineering, 2024).

If it survives **here**, it might be overbuilt (in a good way) for your daily commute (Formula 1, 2024).

### 7.3 Is “net-zero and fast” actually realistic?

Honest answer:

- The **fuel side** can be net-zero-ish if the whole production chain is truly green, but it’s expensive and hard to scale (Stepien, 2025; Red Bull Racing, 2024). 
- The **electrification** push clearly helps efficiency (Vasudev, 2025; FIA, 2024).
- The rest of F1’s carbon footprint (freight, flights, factories) also matters a lot (Stepien, 2025).

So “net-zero and fast” is:

- Not pure marketing (Formula 1, 2024).
- Not magically solved (FIA, 2024).
- A **huge optimization problem** across technology, cost, and rules (Racecar Engineering, 2024; Aston Martin F1 Team, 2025).

The same tools F1 uses to shave tenths off a lap — simulations, control algorithms, energy models — are the tools we need to squeeze waste out of the whole energy system (Vasudev, 2025; Stepien, 2025).

---

# References
Baldwin, A. (2024, June 6). F1 unveils ‘nimble’ car for new era starting in 2026. Reuters. https://www.reuters.com/sports/formula1/f1-unveils-nimble-car-new-era-starting-2026-2024-06-06/

Vasudev, R. (2025). Hybrid power unit efficiency in Formula 1: Thermal management, energy recovery strategies and performance optimization. IJFMR, 7(4), 1–9. https://www.ijfmr.com/papers/2025/4/53663.pdf

Stepien, Z. (2025). The pro-ecological evolution of powertrains and fuels in Formula 1. Energies, 18(22), 6013. https://www.mdpi.com/1996-1073/18/22/6013

Fédération Internationale de l'Automobile. (2024, June 11). 2026 Formula 1 power unit technical regulations (Issue 7). https://www.fia.com/sites/default/files/fia_2026_formula_1_technical_regulations_pu_-_issue_7_-_2024-06-11_1.pdf

Formula 1. (2024, June 6). FIA unveils Formula 1 regulations for 2026 and beyond featuring more agile cars and active aerodynamics. https://www.formula1.com/en/latest/article/fia-unveils-formula-1-regulations-for-2026-and-beyond-featuring-more-agile.75qJiYOHXgeJqsVQtDr2UB

Aston Martin F1 Team. (2025, May 8). The road to 2026 — F1’s new era and regulations explained. https://www.astonmartinf1.com/en-GB/news/feature/the-road-to-2026-f1s-new-era-and-regulations-explained

Red Bull Racing. (2024). Formula One: New rules and regulations for the 2026 season. https://www.redbull.com/us-en/f1-new-rules-regulations

Racecar Engineering. (2024, June 6). FIA announces details of 2026 Formula 1 technical regulations. https://www.racecar-engineering.com/articles/f1/fia-announces-details-of-2026-formula-1-technical-regulations/



