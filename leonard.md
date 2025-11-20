---
layout: default
title: Leonard
permalink: /leonard/
---

# Engineering Sustainable Performance: The 2026 F1 Hybrid Power Unit

## Leonard

![Diagram of F1 hybrid powertrain](assets/Motor-Generator-Unit-Diagram.jpg)

---
title: Fast *and* Net-Zero? The Future F1 Powertrain
---

# Can Formula 1 Be Fast *and* Net-Zero?

By 2030, Formula 1 wants to be **net-zero carbon**.  
From 2026, the cars get a new kind of **hybrid powertrain** that:

- Uses **100% “drop-in” sustainable fuel** (synthetic / bio-based fuel that can run in normal-style engines).
- Gets about **half its power from electricity** and half from the fuel-burning engine.

That sounds like magic: *“Same crazy speed, but greener, please.”*  
Under the skin, it’s a brutal engineering puzzle.

This page walks through the main design challenges in **plain language**:

- How the **engine and electric side share power**.
- How the car **keeps everything cool**.
- How the car **recycles energy** from braking and exhaust.

---

<!-- INSERT IMAGE: Hero shot of an F1 car with simple labels -->

![F1 powertrain hero diagram](/assets/img/hero-powertrain.png)

*A modern F1 car is basically a rolling physics experiment: engine, battery, motors, fuel, and a lot of heat.*

---

## 1. Quick Primer: What Is an F1 Powertrain?

### 1.1 “Powertrain” in one sentence

The **powertrain** is everything that takes **energy** (fuel + electricity) and turns it into **force at the wheels**.

Think of it as the car’s **muscle system**:
- The **engine** is the burning-muscle part.
- The **battery + electric motor** is the electric-muscle part.
- The **control electronics** are the brain that coordinates them.

### 1.2 The main pieces (in human terms)

In the current hybrid era, an F1 power unit has:

- **Internal Combustion Engine (ICE)**  
  A tiny 1.6L turbo V6. It burns fuel, makes noise, and does most of the work today.

- **Turbocharger**  
  A little air compressor spun by exhaust gas. It forces more air into the engine so you can burn more fuel and make more power.

- **MGU-K (Motor Generator Unit – Kinetic)**  
  An electric machine connected to the crankshaft.
  - On **braking**, it acts like a generator: it slows the car a bit and charges the battery.
  - On **acceleration**, it acts like a motor: it pushes the car with electric power.

- **MGU-H (Motor Generator Unit – Heat)** *(being removed from 2026)*  
  Connected to the turbo.
  - It can harvest energy from the spinning turbo.
  - It can also spin the turbo to reduce “turbo lag”.

- **Energy Store (Battery)**  
  High-power lithium-ion pack. Not huge like a road EV, but it can deliver and absorb big bursts of power.

- **Power Electronics / Control Unit**  
  The “traffic cop” that decides how electricity flows between battery, MGU-K, MGU-H, and sometimes directly from exhaust to wheels.

### 1.3 Old vs new balance

Right now, roughly:
- **~80%** of power: from the engine.
- **~20%**: from the electric side. :contentReference[oaicite:0]{index=0}  

From **2026**, the rules push toward:
- **~50% engine, ~50% electric**, plus 100% sustainable fuel. :contentReference[oaicite:1]{index=1}  

That means the electric side is no longer just “extra boost” – it’s half the show.

---

<!-- INSERT IMAGE: Simple block diagram of power flows -->

![F1 hybrid powertrain blocks](/assets/img/powertrain-block-diagram.png)

*Fuel and electricity both take different paths, but all roads lead to the rear wheels.*

---

## 2. What “Net-Zero” and “Drop-In Sustainable Fuel” Actually Mean

### 2.1 What is “net-zero” in F1?

**Net-zero** doesn’t mean “no emissions from the exhaust pipe.”  
It means that, over a year, the **total CO₂ released** is **balanced** by:

- Cutting emissions where possible (more efficient engines, less fuel).
- Using **sustainable fuel** made from carbon that was already in the cycle (air, waste, biomass).
- Offsetting the rest with other projects.

For the **powertrain**, the big idea is:

> “No **new** fossil carbon from underground. The carbon in the fuel should come from stuff that was already above ground.”

### 2.2 What is 100% “drop-in” sustainable fuel?

“**Drop-in**” means the fuel:

- Can be **used in normal-style engines** with only small tweaks.
- Can flow through **existing fuel distribution** systems (tanks, pipes, trucks). :contentReference[oaicite:2]{index=2}  

Where can this carbon-neutral-ish fuel come from?

- **Captured CO₂** from the air or industrial fumes.
- **Waste biomass** (like leftovers from farming, not food crops).
- **Municipal waste** (garbage that would otherwise rot or be burned). :contentReference[oaicite:3]{index=3}  

The key idea:  
The CO₂ that comes out the **exhaust** was already in the atmosphere or waste stream recently, so you’re not adding new CO₂ from underground oil.

### 2.3 Why fuel makes engineers sweat

Sustainable fuel is not just “normal gasoline but a nicer color.” It:

- Can burn **faster or slower**.
- Can change the **flame temperature and pressure**.
- Can change how hot the exhaust and turbo run.

That means:
- You may need to redesign **combustion chambers** and **injectors**.
- You must retune the **engine mapping** (timing, fuel flow, boost).
- All of that affects **heat**, **efficiency**, and **reliability**.

So the “green fuel” question is really:

> “Can we make fuel that’s friendly to the planet **and** friendly to a tiny, screaming 15,000 rpm engine?”

---

<!-- INSERT IMAGE: Fuel lifecycle loop -->

![Sustainable fuel lifecycle](/assets/img/fuel-lifecycle.png)

*The dream: carbon goes in a loop, not from deep underground into the sky forever.*

---

## 3. Design Challenge #1 – Hybrid Integration: Sharing Power Without Chaos

The new F1 car basically has **two engines**:

- One that burns **fuel** (ICE).
- One that uses **electricity** (MGU-K + battery).

They have to **share the work** while:

- Staying within power limits.
- Saving fuel.
- Not cooking the engine or battery.

### 3.1 Mental model: runner + e-scooter

Imagine:

- A **runner** (the engine) doing most of the work.
- An **electric scooter** (the motor) that can:
  - Push the runner on straights.
  - Charge itself when going downhill (braking).

The big question is always:

> “Who should work harder **right now**: runner or scooter?”

### 3.2 Control problem: who does what, when?

The control system (software + hardware) needs to decide, every split second:

- On **acceleration**:
  - How much power comes from the engine?
  - How much extra push from the electric motor?

- Under **braking**:
  - How much braking is done by MGU-K (regeneration)?
  - How much by normal hydraulic brakes, so the car stays stable?

- On **straights**:
  - Should the car **spend** stored electrical energy to go faster?
  - Or **save** it for later corners or overtakes?

With the 2026 push to roughly **50/50 engine–electric power**, bad decisions here can lose **tons of lap time**.

### 3.3 Why 50/50 is a big deal

When electric power was only ~20%:

- Teams could treat it as a **bonus**: helpful, but not life-or-death.

With ~50% electric:

- You **cannot** reach full performance without using the electric side properly.
- Energy management becomes as important as classical engine tuning.

This creates real trade-offs:

- **Simple control strategy** → easier to design, more reliable, but probably slower.
- **Aggressive, complex strategy** → faster on paper, but more fragile and harder to get right.

### 3.4 Trade-offs and “how to screw it up”

A few ways to mess this up:

- **Overspending electric early in the lap**  
  - Car feels amazing at the start of the lap.
  - Battery runs low later, so you’re a sitting duck on the straight.

- **Over-harvesting (charging too hard)**  
  - You drag the engine (or brakes) more to recharge the battery.
  - That slows the car and adds **extra heat** in both engine and battery.

- **Conservative strategy**  
  - You keep plenty of energy in the battery.
  - But you’re leaving free lap time on the table.

Good hybrid integration is basically:

> “Turn the car into a well-timed sprint, not an energy panic attack.”

---

<!-- INSERT IMAGE: One-lap energy diagram -->

![Lap energy usage](/assets/img/lap-energy-usage.png)

*Different parts of the lap: sometimes you save, sometimes you spend, sometimes you charge.*

---

## 4. Design Challenge #2 – Thermal Management: The Heat Problem

Every time you **convert energy**, you make **heat**.  

Modern F1 power units can hit **~50% thermal efficiency**, which is insanely high, but that also means the **other half** of the fuel’s energy is mostly heat. :contentReference[oaicite:4]{index=4}  

Now add:

- High-power battery.
- Motor-generators.
- Power electronics.

You’ve just built a **portable oven** that happens to go 300 km/h.

### 4.1 Where the heat comes from

Heat sources include:

- **Engine combustion** – hot gases, hot pistons, hot everything.
- **Turbo and exhaust** – exhaust gases can be hundreds of degrees.
- **Battery** – gets hot when charging and discharging fast.
- **MGU-K motor** – electric machines are not 100% efficient.
- **Power electronics** – inverters, DC-DC converters.
- **Brakes** – kinetic energy turned into heat at the discs.

### 4.2 Cooling without murdering speed

To remove heat, you need:

- **Radiators and coolers** – water, oil, battery coolant, etc.
- **Airflow** over those coolers.

The catch:

- More air → **more drag** → slower on straights.
- Bigger radiators → **more weight and more space** → harder packaging.

So teams are constantly trading off:

> Cool enough to survive ⟷ Slippery enough to win.

### 4.3 New headaches with more electric + new fuel

- More **electric power** → more **battery current** → more battery heat.
- More **regen** → more hot brakes, more hot MGU-K, more hot electronics.
- **Sustainable fuel** may change:
  - Exhaust temperature.
  - How heat is distributed between engine, turbo, and exhaust. :contentReference[oaicite:5]{index=5}  

That means:

- You might need more or different **cooling circuits**.
- You might have to rethink how hot air leaves the car so it doesn’t **reheat** other components.

### 4.4 The cooling–drag–weight triangle

You can picture a three-way tug-of-war:

- **Cooling** – bigger radiators, more airflow.
- **Drag** – smooth, tight bodywork wants less airflow and smaller openings.
- **Weight** – more radiators, more fluid, more structure.

You can’t maximize all three. Typical trade-offs:

- Add cooling:
  - ✅ safer temperatures  
  - ❌ more drag and weight → slower lap.
- Reduce cooling:
  - ✅ less drag, more top speed  
  - ❌ risk of overheating – car has to back off or breaks.

### 4.5 What happens if they get it wrong?

Symptoms of bad thermal management:

- Driver gets messages like “cool the car” → must lift off and coast.
- Engine power gets reduced automatically to protect hardware.
- Battery temp goes high → power output or regen gets limited.
- In worst cases: **DNF** (engine/battery failure) and millions of dollars go poof.

---

<!-- INSERT IMAGE: Heat map and air paths -->

![Thermal hot spots and cooling airflow](/assets/img/thermal-map.png)

*Red: hot zones (engine, exhaust, battery). Blue: cooling air paths. You want maximum cooling for minimum drag.*

---

## 5. Design Challenge #3 – Energy Recovery: Recycling Speed

When you brake a normal car, you turn kinetic energy into **useless heat** in the brakes.

In F1, part of that “wasted” energy is **recycled**:

- **MGU-K** grabs some energy during braking and sends it to the **battery**.
- Historically **MGU-H** could grab energy from the hot exhaust and send it either:
  - to the **battery**, or
  - **directly** to MGU-K, skipping the battery and saving some losses. :contentReference[oaicite:6]{index=6}  

This is like charging a power bank every time you slow down, then using it to slingshot yourself out of corners.

### 5.1 How much energy can you actually recover?

On a typical lap:

- **MGU-K can recover on the order of ~20% of braking energy**, sometimes more on very “stop-start” tracks with many slow corners. :contentReference[oaicite:7]{index=7}  

Limits come from:

- **Regulations** (max power / energy per lap).
- **Grip and stability** – too much regen on rear wheels can make the car unstable.
- **Battery size and temperature** – you can’t shove infinite energy into a hot, full battery.

Track layout matters:

- More tight corners → more braking → more recovery potential.
- More high-speed sweeps → less heavy braking → less to harvest. :contentReference[oaicite:8]{index=8}  

### 5.2 Where does recovered energy go?

Options:

1. **Into the battery**  
   - Flexible: can be used later in the lap wherever you want.
   - But every charge/discharge cycle creates **losses and heat**.

2. **Direct transfer (exhaust → MGU-K)** (in the MGU-H era)  
   - Skips the battery, so fewer losses and less battery wear.
   - Simulation studies suggest this can cut battery cycling losses by up to **~8%**. :contentReference[oaicite:9]{index=9}  
   - But needs very careful control of turbo speed, engine torque, and driver demands.

In 2026, with **MGU-H removed** but more electric power overall, the battery + MGU-K side becomes even more central. :contentReference[oaicite:10]{index=10}  

### 5.3 Control strategy: when to harvest, when to spend

You can’t always do everything at once:

- If you **harvest hard** into a corner (lots of regen), you:
  - Gain more energy.
  - Risk upsetting the car’s balance under braking.

- If you **boost hard** out of a corner, you:
  - Go faster.
  - Burn through your stored energy and heat up the battery.

The car’s control system has to constantly answer questions like:

- “Is this the right lap to save energy for an overtake?”
- “Should we harvest a bit more now to have extra boost later on the straight?”
- “Should we back off harvesting because battery temp is high?”

### 5.4 Trade-offs and edge cases

- **Too much regen**:
  - Rear wheels might lock or feel unstable.
  - Driver confidence drops; lap time suffers.

- **Too little regen**:
  - You’re literally throwing energy away as heat.
  - You arrive on the straight with less boost than rivals.

- **Battery health vs performance**:
  - Hammer the battery every lap → more heat and wear.
  - Protect the battery too much → give away performance.

Energy recovery is like **budgeting money**:
- Spend too fast → fun now, pain later.
- Never spend → always safe, but you never win.

---

<!-- INSERT IMAGE: corner energy recovery diagram -->

![Corner energy flow: brake, harvest, boost](/assets/img/corner-energy-recovery.png)

*Into the corner: you harvest. Out of the corner: you spend. The magic is in the timing.*

---

## 6. Putting It All Together: System-Level Trade-Offs

The nasty part is: all these things interact.

Change one knob, three others move.

### 6.1 Scenario 1 – Hot race, twisty track

Imagine:

- A very hot day.
- A twisty street circuit with lots of slow corners and heavy braking.

What happens?

- Lots of braking → lots of energy recovery → **battery and MGU-K heat up**.
- Brakes also get hotter.
- Engine runs hot because air temps are high.

To keep things safe, engineers might:

- **Open up the cooling** (bigger air inlets, different bodywork):
  - ✅ Lower temperatures.
  - ❌ More drag → slower on straights.

- **Harvest a bit less energy**:
  - ✅ Less battery and brake heat.
  - ❌ Less electric boost later → slower lap times.

So they have to decide:

> “Do we want *maximum* performance for a few laps, or *very high* performance for the whole race without cooking the car?”

### 6.2 Scenario 2 – Qualifying lap vs race stint

- **Qualifying** (one or two flying laps):
  - Use **aggressive hybrid strategy**.
  - Spend more battery, accept higher temperatures for a short time.
  - Maybe run tighter bodywork for less drag, gambling that the car won’t overheat in just a few laps.

- **Race stint** (dozens of laps):
  - Dial back power slightly.
  - Use **more conservative energy recovery and boost**.
  - Run more cooling to keep things in a safe window.

Same hardware, completely different settings because the **time horizon** is different.

### 6.3 Big-picture trade-offs

You can think of three big sliders:

1. **Speed vs Efficiency**
   - Go flat-out → burn more fuel, run hotter, use more battery cycles.
   - Drive slightly under the limit → save fuel, keep temps in check, maybe have more power at the end.

2. **Complexity vs Reliability**
   - Super advanced control software → brilliant when it works, but harder to calibrate and debug.
   - Simpler strategies → more robust, but might miss the last few tenths.

3. **Performance vs Sustainability goals**
   - F1 wants:
     - Net-zero carbon.
     - Engines and fuels that teach us something useful for road tech.
   - But fans expect:
     - Ridiculous lap times.
     - Wheel-to-wheel racing.
     - Reliability good enough that championships aren’t decided by random explosions.

The engineering question is:

> “Can we design a powertrain that helps the planet **and** still scares the driver a little on every lap?”

---

<!-- INSERT IMAGE: System interaction map -->

![Powertrain system interactions](/assets/img/system-interactions.png)

*Change fuel → change combustion → change heat → change cooling → change drag → change lap time. Everything is connected.*

---

## 7. Why This Matters Beyond F1

F1 is an extreme, expensive sandbox. But the lessons don’t stay on the track.

### 7.1 Lessons for road cars

Things that can trickle down:

- **Better hybrid strategies**  
  - Smarter software that decides when to use engine vs electric.
  - Smoother blending of regen and hydraulic brakes.

- **Thermal management tricks**  
  - Compact, efficient coolers.
  - Smarter coolant routing and control.

- **Sustainable fuels**  
  - If F1 proves that truly high-performance engines can run on **drop-in sustainable fuel**, that’s a big data point for aviation, shipping, and legacy cars that can’t easily go full EV. :contentReference[oaicite:11]{index=11}  

### 7.2 F1 as a “lab on wheels”

Why do car companies care?

- They get to test ideas in **the harshest possible environment**:
  - Tiny engines making huge power.
  - Massive power density in batteries and motors.
  - High vibration, high temperature, long races.

If it survives **here**, it might be overbuilt (in a good way) for your daily commute.

### 7.3 Is “net-zero and fast” actually realistic?

Honest answer:

- The **fuel side** can be net-zero-ish if the whole production chain is truly green, but it’s expensive and hard to scale. :contentReference[oaicite:12]{index=12}  
- The **electrification** push clearly helps efficiency.
- The rest of F1’s carbon footprint (freight, flights, factories) also matters a lot.

So “net-zero and fast” is:

- Not pure marketing fluff.
- Not magically solved.
- A **huge optimization problem** across technology, cost, and rules.

What’s cool is that:

> The same tools F1 uses to shave tenths off a lap — simulations, control algorithms, energy models — are the tools we need to squeeze waste out of the whole energy system.

---

<!-- INSERT IMAGE: Tech transfer from F1 to the world -->

![Tech transfer from F1 to road and air](/assets/img/tech-transfer.png)

*Ideas don’t stay on the grid. Hybrid control, cooling solutions, and fuels can ripple outward.*


