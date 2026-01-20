#- SYSTEM_ONTOLOGY_DEFINITION
#- PROJECT: CROSSFIT_PROGRAMMING_SYNTHESIS
#- VERSION: 1.0

#- SECTION: VARIABLE_INPUT_VECTORS
    # DEFINITION: These are the immutable and mutable inputs required to instantiate a User Profile.

    #- PARAMETER: AGE_BRACKET
        # LOGIC: Dictates recovery curve and joint loading tolerance.
        - VALUE: OPEN (18-34) -> [Recovery factor: 1.0] [Volume Cap: 100%]
        - VALUE: MASTERS_A (35-44) -> [Recovery factor: 0.85] [Volume Cap: 90%]
        - VALUE: MASTERS_B (45-54) -> [Recovery factor: 0.70] [Volume Cap: 75%] [Constraint: No back-to-back heavy flexion]
        - VALUE: MASTERS_C (55+) -> [Recovery factor: 0.50] [Volume Cap: 60%] [Constraint: Extended warm-up protocols]

    #- PARAMETER: COMMITMENT_LEVEL
        # LOGIC: Dictates the depth of the session (Single vs. Multi-modal).
        - VALUE: LOW (0-5 Hours) -> [Structure: Warmup + WOD + Cooldown]
        - VALUE: MED (6-10 Hours) -> [Structure: Strength + WOD + Accessory]
        - VALUE: HIGH (11-15+ Hours) -> [Structure: AM Session (Cardio) + PM Session (Strength + Metcon)]

    #- PARAMETER: FITNESS_ARCHETYPE
        # LOGIC: Determines the bias of the base cycle.
        - VALUE: STRENGTH_BIASED -> [Logic: Maintenance Strength / High Metcon Volume]
        - VALUE: ENGINE_BIASED -> [Logic: Hypertrophy & Strength Focus / Maintenance Aerobic]
        - VALUE: BALANCED -> [Logic: Linear Periodization across domains]
        - VALUE: NOVICE -> [Logic: Skill Acquisition > Intensity]

    #- PARAMETER: GENDER_PHYSIOLOGY
        # LOGIC: Hormonal cycle and strength-to-weight loading adjustments.
        - MALE -> [Standard Load References]
        - FEMALE -> [Load scaling: ~70% of Male] [High Volume Gymnastics Tolerance: +10%]

#- SECTION: PERSONA_GENERATION_MATRIX
    # DEFINITION: Synthesis of input vectors into distinct programming tracks.

    #- PERSONA_ID: "THE_COMPETITIVE_MASTER" (Derived from Jim Royce Data)
        - INPUTS: [Male] + [Masters_B] + [High_Commitment] + [Strength_Biased]
        - BASE_PROGRAM:
            - Frequency: 5 days on, 2 days active recovery.
            - Bias: Engine Capacity & Gymnastics Efficiency.
            - Constraint: Heavy Spinal Loading capped at 2x/week.
        - SUCCESS_METRIC: Maintenance of Strength numbers + 5% increase in VO2 Max metrics.

    #- PERSONA_ID: "THE_SCALED_OPEN"
        - INPUTS: [Female/Male] + [Open] + [Med_Commitment] + [Novice]
        - BASE_PROGRAM:
            - Frequency: 4 days on, 3 days off.
            - Bias: Skill Progression (E.g., Pull-up -> C2B).
            - Constraint: Intensity capped until mechanics are consistent.

    #- PERSONA_ID: "THE_EFFICIENT_EXECUTIVE"
        - INPUTS: [Male/Female] + [Masters_A] + [Low_Commitment] + [Balanced]
        - BASE_PROGRAM:
            - Frequency: 3-4 days (45 min hard cap).
            - Bias: High Intensity Interval Training (HIIT) + Compound movements only.
            - Constraint: No isolation work (inefficient use of time).

#- SECTION: SUBSTITUTION_PROTOCOL_LOGIC
    # DEFINITION: Rules for modifying Rx (Prescribed) movements based on Limitation or Equipment.

    #- SUB_CATEGORY: INJURY_LIMITATION
        # LOGIC: Preserve the Stimulus (energy system), change the Movement Pattern.
        - CASE: "SHOULDER_IMPINGEMENT" (Cant go overhead)
            - IF RX: Handstand Pushups -> SUB: Heavy Dumbbell Bench Press (Push Horizontal).
            - IF RX: Snatch -> SUB: Heavy Clean + Plyo Jump.
        - CASE: "LUMBAR_ISSUE" (No spinal compression)
            - IF RX: Heavy Back Squat -> SUB: Belt Squat or Heavy Sled Push (Leg hypertrophy without compression).
            - IF RX: Deadlift -> SUB: Glute Ham Raise + Farmer Carry.

    #- SUB_CATEGORY: EQUIPMENT_LIMITATION
        # LOGIC: Preserve the Time Domain and Muscle Group.
        - CASE: "NO_MONOSTRUCTURAL_MACHINES" (No Row/Bike/Ski)
            - IF RX: 500m Row (2:00 duration) -> SUB: 400m Run OR 20 Burpees.
        - CASE: "LOW_CEILING" (No Box Jumps/Wall Balls)
            - IF RX: Wall Balls -> SUB: Thrusters (Empty Bar).
            - IF RX: Box Jumps -> SUB: Broad Jumps or Step-Ups.

#- SECTION: RECALIBRATION_TRIGGER_EVENTS
    # DEFINITION: If Input X occurs, Execute Logic Y.

    - TRIGGER: "SPOTTY_RESULTS" (Missed >20% of sessions in 7 days)
        - ACTION: Downgrade COMMITMENT_LEVEL by one tier for next 2 weeks.
    - TRIGGER: "STRENGTH_PLATEAU" (3 consecutive failed heavy sessions)
        - ACTION: Switch Strength Block from "Linear Progression" to "Deload/Volume" phase.
    - TRIGGER: "HIGH_FATIGUE_SCORE" (Self-reported soreness > 8/10)
        - ACTION: Convert next "For Time" workout to "EMOM" (forced rest intervals).