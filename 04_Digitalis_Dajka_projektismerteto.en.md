**Language / Nyelv:** [English](04_Digitalis_Dajka_projektismerteto.en.md) · [Magyar](04_Digitalis_Dajka_projektismerteto.md)

# Digital Nanny / Digital Pacifier / Digital Babysitter

**Public project overview**

Author: Almási Andor · Version: v1 (7 August 2026) · Created in human–AI collaboration

> This document is solely a public project overview. It does not contain the detailed internal implementation plans, validation systems, thresholds or any other reproducible development know-how.

> **Translator's note.** The Hungarian project names are *Digitális Dajka* (Digital Nanny), *Digitális Cumi* (Digital Pacifier — *cumi* is the colloquial Hungarian word for a baby's dummy) and *Digitális Babysitter* (Digital Babysitter).

## 1. What is the idea behind the Digital Nanny?

The Digital Nanny is an AI-based development concept that transforms the role of the phone or tablet a child already uses. The goal is not to give the child even more passive screen time, but for the same device to become an active channel for learning, communication, creativity and safety.

The core idea of the system is that the AI should not simply be a chatbot that answers questions, but a consistent digital helper that works with the child over the longer term. It observes the child's reactions, interests, capacity for load and developmental patterns, and then adapts its communication and tasks to them.

## 2. Why "Digital Pacifier", and why "Digital Nanny"?

The name "Digital Pacifier" refers to the starting problem: in many families, the phone and the tablet already become an attention-holding device in early childhood. The project does not simply want to ban this existing situation, but to turn it into a more meaningful function.

The names "Digital Nanny" and "Digital Babysitter" denote the further-developed role: a digital helper that learns, communicates, develops the child through play and, in later system versions, may also be able to interpret signals coming from the physical environment.

## 3. The central element of the system: a dynamic child model

The system does not describe the child with a single rigid label or score. It can observe several different areas of functioning: for example, speech comprehension, vocabulary, attention, memory, problem-solving, spatial thinking, creativity, motivation, frustration tolerance and emotional reactions.

The child model is continuously updated. The system compares the child primarily with their own earlier state, and examines what reaction a given task, communication style or difficulty level has triggered.

**Important:** this model is not a medical diagnosis and not a static rating, but a continuously modifiable working hypothesis that serves personalised communication and learning support.

## 4. Playful, natural learning

Assessing and developing the child is not based on classic testing. The system gathers feedback from playful conversations, tasks, stories, pictures, choices and everyday interactions.

The goal is for learning to remain an enjoyable experience. The system may be able, for example, to adapt the difficulty of a task, the style of an explanation, the pace of speech or the topic to the child's current interests and capacity for load.

## 5. A stable AI character

The child meets a consistent, recognisable digital character, not a different personality each time. A stable visual and vocal presence creates a more predictable relationship.

The digital character is not a substitute for the parent or other family members. Its tasks are to answer recurring questions, teach through play, tell stories, support practice and simple routines, and maintain a consistent dialogue with the child.

## 6. The role of the parent

A founding principle of the project is that the parent or guardian remains the primary human decision-maker. The AI may observe, analyse, make suggestions, measure progress and respond within predefined operating boundaries, but it is not an authority standing above the family.

The system may also use a family profile: for example, based on language, daily schedule, habits, parenting goals, interests and screen-use rules. This information serves personalisation.

## 7. Multimodal sensing

In later development layers, the system may interpret more than written text. The camera, microphone, touch data and motion sensors of the phone or tablet can together help it understand the situation better.

Audio, for example, can be processed on two separate channels: one converts the content of speech into text, while the other can use characteristics of the sound — such as tempo, volume, pauses or hesitation — as a supplementary state signal.

The system must not treat an emotional or physical state as certain on the basis of a single signal; the goal is the combined interpretation of several signals, one that also handles uncertainty.

## 8. The next big step: the spatial Digital Nanny

The project's next architectural level is sensor fusion and a dynamic 3D world model of the environment. Here the phone or tablet is no longer the only observation point but part of a larger sensor system.

Later, the system may connect fixed room sensors, cameras, microphones, distance or depth sensors, and a small wearable sensor module associated with the child.

The goal is for the system to know not only what the child says or touches, but also to be able to estimate where they are, where they are moving, what objects or people are around them, and how the environment is changing.

## 9. Dynamic 3D world model and risk estimation

In the development concept, the various sensor inputs are brought into a shared temporal and spatial model. The system handles separately the observation, the situational hypothesis built from multiple sensors, and the environmental world model continuously updated from these.

This could make it possible to track static and moving objects, people, animals, doors, stairs and other relevant elements of the environment. The system may also produce short-term motion prediction and dynamic risk estimation.

Here, too, the emphasis is not on the "infallibility" of any single sensor, but on combining several partial measurements and explicitly handling how certain the system is about a given estimate.

## 10. What does the project not aim to do?

- It does not aim to replace parents, grandparents, siblings or real human relationships.
- It does not aim to keep the child on a passive screen all the time.
- It does not aim to create a single rigid intelligence or personality score.
- It does not aim for the AI to make a medical or psychological diagnosis.
- It does not aim for the system to draw firm conclusions from the signal of a single camera or sensor.

## 11. What makes the idea special?

The project does not describe a single app or a single educational feature. It targets an interconnected system architecture in which the long-term child model, adaptive communication, family settings, multimodal sensing, the later spatial world model and graduated AI responses are all parts of the same system.

The core idea in brief: to create, from the digital device a child already uses, an intelligent, personalisable development interface that does not use the screen for its own sake, but supports learning, curiosity, communication, creativity, safety and family cooperation.

## 12. Current state of development

The system core of the concept and the first structural framework of the sensor-fusion/3D environment architecture have been completed and have gone through separate review rounds. The detailed 3D world model, the wearable sensor module, the fixed spatial sensor network, real-time danger and state estimation, the AI intervention logic and smart-home integration are the subject of further development work.

## 13. Data protection and child safety

The system would collect data about children, including camera, audio, touch and motion data, as well as state estimates derived from them. Data protection is therefore not an add-on feature but a starting condition of the design. The concept sets out the following principles. They are requirements, not features that have already been implemented.

- **Legal framework:** the EU General Data Protection Regulation (GDPR), the stricter rules that apply to children's data, and the requirements of the EU Artificial Intelligence Act (AI Act). A data protection impact assessment is required before any implementation.
- **Parental consent and control:** data is collected only with the explicit consent of a parent or guardian, which can be withdrawn at any time. The parent can see what the system stores and can delete it.
- **Data minimisation:** only data needed for operation is created; raw video and audio recordings are, wherever possible, not stored.
- **Local processing first:** whatever can be processed on the device or within the family's own network should be processed there. Only necessary, encrypted and minimised data may go to the cloud.
- **No secondary use:** the child's data may not be used for advertising or for profiling for other purposes, and may not be passed on.
- **Limits of state estimation:** estimates of emotional or physical state are uncertain, are neither a rating nor a diagnosis, and cannot be the basis of a decision without human review.
- **Retention and deletion:** a defined retention period; the child model and its associated data can be deleted in full.

---

## One-sentence summary

The goal of the Digital Nanny / Digital Pacifier / Digital Babysitter is to turn the phone or tablet a child already uses from a passive attention-holding device into a personalised, adaptive system that supports learning and communication and, later, spatial safety — without replacing family relationships.
