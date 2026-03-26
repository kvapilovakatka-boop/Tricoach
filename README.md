<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# TriCoach AI

Building AI course project
Final project for the Building AI course

## Summary

TriCoach AI is a simple training assistant for triathletes. It estimates daily training readiness based on recovery, sleep, fatigue, and recent workload, and then recommends whether the athlete should do the planned session, reduce intensity, or prioritize recovery.
TriCoach AI is a simple decision-support tool for triathletes. It evaluates daily readiness based on sleep, fatigue, and training load, and recommends whether to train fully, reduce intensity, or rest.

## Background

Triathlon training combines swimming, cycling, and running, which makes fatigue management difficult. Athletes often struggle to decide whether they are truly ready for a hard session or whether they should reduce intensity and recover more.
Triathlon training combines multiple endurance disciplines, making fatigue management difficult. Athletes often struggle to decide whether they are ready for a hard session or need recovery.

This problem is common especially among amateur athletes who train alongside work or school. Poor decisions can lead to overtraining, injury, or reduced performance.

My motivation comes from my own interest in endurance sports. I want a simple system that helps make smarter daily training decisions.

This problem is common especially for amateur athletes who train around work, school, and daily stress. Poor decisions can lead to accumulated fatigue, lower performance, or even injury.
* difficulty managing fatigue across swim, bike, and run
* risk of overtraining or injury
* lack of simple decision tools for amateur athletes

My motivation comes from my own interest in endurance sports and triathlon. I would like to have a simple system that helps make better day-to-day training decisions instead of relying only on emotion or guilt.

## How is it used?

The user enters simple daily variables such as:
- sleep duration
- subjective fatigue
- muscle soreness
- resting heart rate or perceived readiness
- previous training load
- planned workout type
The user inputs simple daily data such as:
- hours of sleep
- fatigue level (1–5)
- muscle soreness (1–5)
- previous training intensity
- planned workout (swim, bike, run)

The AI processes this information and outputs one of three recommendations:
- GO (full training)
- LIGHT (reduced intensity)
- REST (recovery day)

The AI then gives one of three recommendations:
- do the planned training
- do a lighter version
- take a recovery / rest day
This solution can be used daily before training. It is useful for amateur triathletes and endurance athletes who want guidance without complex tools.

This tool would be useful for amateur triathletes, runners, cyclists, or coaches who want a simple readiness check before training.
This is how you create code examples:
def recommend_training(sleep, fatigue, soreness):
if sleep < 5 or fatigue > 4:
return “REST”
elif fatigue > 3 or soreness > 3:
return “LIGHT”
else:
return “GO”

print(recommend_training(6, 3, 2))

## Data sources and AI methods

The project could use small structured input data collected manually by the athlete, for example:
- hours of sleep
- previous day training duration
- previous day training intensity
- soreness score from 1 to 5
- fatigue score from 1 to 5
- resting heart rate compared to normal
- discipline planned for today (swim / bike / run)

Possible AI method:
The data is simple and can be collected by the user manually:
- sleep duration
- subjective fatigue and soreness
- previous training intensity

In a more advanced version, data could come from wearable devices (heart rate, HRV, etc.).

AI method:
- classification

The model would classify each day into one of three categories:
- ready
- caution
- recovery
The system classifies daily readiness into three categories (GO, LIGHT, REST). Initially, this can be implemented using simple rule-based logic, and later improved using machine learning methods such as decision trees or logistic regression.

At the beginning, the rules could be partly hand-made and later improved with real user data. A simple machine learning approach such as decision trees, logistic regression, or nearest neighbor classification could be enough.
| Input        | Example        |
|--------------|---------------|
| Sleep        | 6 hours       |
| Fatigue      | 3/5           |
| Soreness     | 2/5           |
| Output       | LIGHT         |

## Challenges

This project does not directly measure true physiological readiness. It only estimates it from available inputs.
This project does not measure true physical readiness, only estimates it.

Some limitations:
- subjective data may be inconsistent
- small personal datasets may be noisy
- readiness can be affected by stress, illness, hydration, or menstrual cycle, which may not always be included
- recommendations should not replace medical advice or professional coaching
Limitations:
- subjective inputs may be inaccurate
- small amount of data
- does not include all factors (stress, illness, nutrition)

Ethically, the tool should be transparent and should never pressure the athlete into overtraining. It should support safe decision-making, not punish missed sessions.
Ethical considerations:
- should not replace medical advice
- should not push athletes into overtraining
- must be transparent about its limitations

## What next?

In the future, the project could be expanded by:
- connecting to sports watches or training apps
- using HRV, resting heart rate, and pace data automatically
- adding weather conditions
- learning personal patterns over time
- suggesting which discipline is best for that day
- generating weekly adjustments for triathlon plans
The project could be expanded by:
- integrating data from sports watches
- tracking long-term performance trends
- personalizing recommendations over time
- adding weather and external conditions
- suggesting specific workouts

To move forward, I would need:
- more personal training data
- better understanding of feature selection
- basic app or dashboard design
- possible collaboration with endurance coaches or sports scientists
To improve this project, I would need:
- more real user data
- better understanding of machine learning models
- basic app or user interface development

## Acknowledgments

This idea was inspired by triathlon training practice, recovery-based coaching principles, and general AI methods for classification and decision support.
* inspired by triathlon training practices
* based on general AI classification concepts
* no external datasets or copyrighted material used
