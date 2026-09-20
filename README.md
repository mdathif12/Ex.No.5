# EXP 5 – Comparing Prompting Techniques Through Engineering Problem-Solving Scenarios

## Register No:212223220058
________________________


# Aim

To compare different prompting techniques and evaluate their effectiveness
in solving a real-world engineering problem by using a problem selected
from the student's final-year project.

The experiment analyzes how different prompt structures affect the relevance,
accuracy, completeness, clarity, feasibility, and usefulness of AI-generated
solutions.


# AI Tools Required

1. ChatGPT
2. Google Gemini
3. Microsoft Copilot


# EXPERIMENT OVERVIEW

In this experiment, a genuine engineering problem from the final-year
project is selected.

The same engineering problem is provided to AI systems using different
prompting techniques. The generated responses are then compared based on:

- Relevance
- Accuracy
- Completeness
- Clarity
- Feasibility
- Technical usefulness

The objective is to understand how prompt engineering affects the quality
of AI-generated solutions.


# PROJECT TITLE

## Adaptive User Interface Design Using Artificial Intelligence Based Eye Tracking Towards Personalized and Intelligent Human–Computer Interaction


# PROJECT PROBLEM STATEMENT

Traditional user interfaces provide the same layout and content to every
user regardless of their attention, interaction pattern, or cognitive state.

The project aims to develop an AI-based adaptive user interface that uses
webcam-based eye tracking to estimate the user's gaze position and adapt
the interface dynamically.

The system uses facial and eye landmarks to estimate gaze coordinates.
A machine learning model can then analyze gaze behavior and help determine
which parts of the interface require greater visual emphasis.

Based on the user's interaction and gaze behavior, the interface can
adapt elements such as:

- Content visibility
- Layout
- Visual emphasis
- Component size
- Information complexity
- Task-related controls


# SELECTED ENGINEERING SCENARIO

## Problem

Develop a method for estimating a user's screen gaze position using a
webcam and eye-tracking features so that the user interface can
dynamically adapt based on the user's visual attention.


# Engineering Requirements

The proposed solution should:

1. Capture video using a webcam.
2. Detect facial landmarks.
3. Extract eye-region information.
4. Preprocess the eye images.
5. Estimate gaze coordinates.
6. Map gaze information to screen coordinates.
7. Detect attention patterns.
8. Adapt the user interface accordingly.
9. Work in near real time.
10. Maintain user privacy by processing data locally where possible.


# STEP 1 – BASE / NAÏVE PROMPT

The following simple prompt is used without any advanced prompting
technique.

```text
How can I detect a user's gaze using a webcam and use it to create
an adaptive user interface?
AI-Generated Output
A webcam-based gaze tracking system can be developed by capturing
the user's face and eyes using computer vision techniques.

The system can detect facial landmarks, extract eye regions, and use
a machine learning model to estimate the user's gaze direction.

The estimated gaze can then be mapped to screen coordinates.
The interface can respond by highlighting or resizing elements
based on where the user is looking.

Possible technologies include OpenCV, MediaPipe, and deep learning
models such as CNNs and LSTMs.
STEP 2 – STRAIGHTFORWARD PROMPT
Technique 1 – Direct / Straightforward Prompt
Suggest a method for developing a webcam-based eye-tracking system
that estimates screen gaze coordinates and dynamically adapts a
user interface.

Mention suitable computer vision techniques, machine learning models,
data preprocessing steps, and UI adaptation methods.
AI-Generated Output
A webcam-based eye-tracking system can use MediaPipe Face Mesh to
detect facial and eye landmarks.

The eye regions can be extracted and converted into grayscale images.
The images can be resized and normalized before being provided to a
CNN-LSTM model.

The model can predict screen-space gaze coordinates.

The predicted coordinates can be used to determine the interface
region currently being viewed.

The interface can then dynamically modify visual emphasis, component
size, content visibility, or layout based on the estimated gaze.

A local WebSocket connection can be used to communicate gaze data
between the eye-tracking system and the user interface.
STEP 3 – PERSONA PROMPT
Technique 2 – Persona Pattern
Act as an experienced computer vision and machine learning engineer
specializing in real-time eye-tracking and human-computer interaction.

Design a technical solution for my final-year project:

"Adaptive User Interface Design Using Artificial Intelligence Based
Eye Tracking Towards Personalized and Intelligent Human–Computer
Interaction."

The system should use a webcam to detect facial and eye landmarks,
extract eye features, estimate screen-space gaze coordinates, and
adapt the user interface according to the user's visual attention.

Explain:
1. Computer vision pipeline
2. Feature extraction
3. Data preprocessing
4. Model architecture
5. Training approach
6. Gaze-coordinate prediction
7. UI adaptation mechanism
8. Real-time implementation
9. Privacy considerations
10. Evaluation metrics
AI-Generated Output
Recommended Pipeline:

Webcam
   ↓
Face Detection
   ↓
Facial Landmark Detection
   ↓
Eye Region Extraction
   ↓
Image Preprocessing
   ↓
Feature Representation
   ↓
CNN Feature Extraction
   ↓
LSTM Temporal Modeling
   ↓
Gaze Coordinate Prediction
   ↓
Screen Coordinate Mapping
   ↓
Attention Estimation
   ↓
Adaptive UI

MediaPipe Face Mesh can be used to obtain facial landmarks.

Eye regions can be converted to grayscale, resized, normalized,
and provided to a CNN for spatial feature extraction.

An LSTM can model temporal information from consecutive frames.

The final model can predict screen-space coordinates such as:

X = horizontal gaze position
Y = vertical gaze position

The interface can use these coordinates to identify the currently
viewed region.

Possible adaptations include:

- Increasing visual emphasis
- Expanding selected content
- Displaying additional information
- Reducing unnecessary content
- Highlighting task-related components

The system should process data locally whenever possible to reduce
privacy risks.

Evaluation can include:

- Mean angular error
- Gaze prediction accuracy
- Response latency
- UI task completion time
- User satisfaction
- System usability
STEP 4 – ROLE + CONSTRAINT PROMPT
Technique 3 – Constraint-Based Prompt
Design a webcam-based AI eye-tracking solution for an adaptive
user interface.

Constraints:

- Use MediaPipe Face Mesh for facial landmarks.
- Use grayscale eye images.
- Resize and normalize eye crops.
- Use a CNN for spatial feature extraction.
- Use an LSTM for temporal information.
- Predict screen-space X and Y gaze coordinates.
- Support near real-time processing.
- Avoid cloud processing of webcam frames.
- Use a modular architecture.
- Explain how the system should be evaluated.

Provide the answer as:

1. System architecture
2. Processing pipeline
3. Model design
4. Training process
5. UI adaptation logic
6. Evaluation metrics
7. Limitations
AI-Generated Output
1. System Architecture

Webcam
   ↓
Frame Capture
   ↓
MediaPipe Face Mesh
   ↓
Eye Landmark Detection
   ↓
Eye Crop Extraction
   ↓
Grayscale + Resize + Normalization
   ↓
CNN
   ↓
LSTM
   ↓
Gaze X,Y Prediction
   ↓
Screen Coordinate Mapping
   ↓
Attention Analysis
   ↓
Adaptive UI


2. Processing Pipeline

Each webcam frame is captured and processed locally.

MediaPipe Face Mesh identifies facial landmarks.

The eye landmarks are used to crop the left and right eye regions.

The eye images are converted to grayscale and resized to a fixed
input resolution.

The normalized eye images are passed to the CNN.

The CNN extracts spatial features.

The LSTM processes a sequence of features to capture temporal
changes in eye movement.

The model predicts screen-space X and Y coordinates.


3. UI Adaptation

If the user repeatedly looks at a particular interface component,
the system can increase its visual emphasis.

For example:

High attention:
→ Highlight component
→ Expand information

Low attention:
→ Reduce visual emphasis
→ Collapse unnecessary details


4. Evaluation

The system can be evaluated using:

- Mean Angular Error
- Mean Absolute Error
- Prediction latency
- Frame processing rate
- Task completion time
- SUS usability score
STEP 5 – CHAIN-OF-THOUGHT / STRUCTURED REASONING PROMPT
Technique 4 – Structured Problem-Solving Prompt
Analyze the following engineering problem systematically:

A webcam-based eye-tracking system must estimate screen-space gaze
coordinates and dynamically adapt a user interface.

Break the solution into these stages:

1. Input acquisition
2. Facial landmark detection
3. Eye feature extraction
4. Image preprocessing
5. Spatial feature extraction
6. Temporal modeling
7. Gaze prediction
8. Screen mapping
9. Attention estimation
10. UI adaptation
11. Real-time optimization
12. Evaluation

For each stage, identify:
- Purpose
- Suitable technique
- Input
- Output
- Possible challenge
- Possible solution

Finally provide an integrated architecture.
AI-Generated Output
1. Input Acquisition

Purpose:
Capture the user's face and eyes.

Technique:
Webcam video capture.

Challenge:
Different lighting conditions.

Solution:
Image normalization and controlled preprocessing.


2. Facial Landmark Detection

Purpose:
Locate the face and eye regions.

Technique:
MediaPipe Face Mesh.

Challenge:
Head movement and occlusion.

Solution:
Use stable facial landmarks and temporal smoothing.


3. Eye Feature Extraction

Purpose:
Extract information related to gaze direction.

Technique:
Eye-region cropping using landmarks.

Challenge:
Different eye sizes and positions.

Solution:
Normalize the eye-region dimensions.


4. Image Preprocessing

Purpose:
Provide consistent model input.

Technique:
Grayscale conversion, resizing, normalization.

Challenge:
Noise.

Solution:
Filtering and preprocessing.


5. Spatial Feature Extraction

Purpose:
Extract visual patterns from eye images.

Technique:
CNN.

Output:
Feature vectors.


6. Temporal Modeling

Purpose:
Capture changes across consecutive frames.

Technique:
LSTM.

Output:
Temporal feature representation.


7. Gaze Prediction

Purpose:
Predict the user's gaze location.

Technique:
Fully connected regression layer.

Output:
Screen X and Y coordinates.


8. Screen Mapping

Purpose:
Convert model predictions into screen coordinates.

Technique:
Coordinate normalization and calibration.


9. Attention Estimation

Purpose:
Determine which interface area receives visual attention.

Technique:
Gaze fixation and dwell-time analysis.


10. UI Adaptation

Purpose:
Modify the interface according to user attention.

Examples:
- Highlight important elements
- Expand selected information
- Reduce irrelevant content


11. Real-Time Optimization

Use:
- Lightweight models
- Frame sampling
- Efficient preprocessing
- Local processing


12. Evaluation

Metrics:
- Angular error
- Coordinate error
- Latency
- FPS
- Task completion time
- Usability score
STEP 6 – FEW-SHOT PROMPT
Technique 5 – Few-Shot Prompting
You are designing an AI-based gaze estimation system.

Example 1:

Input:
Eye image sequence

Processing:
Eye preprocessing → CNN → LSTM

Output:
Screen gaze coordinates (X,Y)

Example 2:

Input:
User gaze repeatedly falls on a button

Processing:
Gaze coordinates → Dwell-time analysis

Output:
Button is visually emphasized

Now design a complete solution for:

A webcam-based eye-tracking system that estimates gaze coordinates
and adapts a web interface according to user attention.

Follow the same input → processing → output structure.
AI-Generated Output
Input:
Webcam video frames

Processing:
Face Mesh → Eye Landmark Detection → Eye Crop →
Grayscale → Resize → CNN → LSTM

Output:
Predicted screen coordinates (X,Y)


Input:
Sequence of gaze coordinates

Processing:
Fixation and dwell-time analysis

Output:
Focused UI component


Input:
Focused UI component

Processing:
Adaptive UI rules

Output:
Highlighted or expanded interface component


Complete Pipeline:

Webcam
→ Face Mesh
→ Eye Detection
→ Preprocessing
→ CNN
→ LSTM
→ Gaze Prediction
→ Coordinate Mapping
→ Attention Analysis
→ Adaptive UI
STEP 7 – COMPARISON OF PROMPTING TECHNIQUES
Technique	Prompt Type	Relevance	Accuracy	Completeness	Clarity	Feasibility	Usefulness
Naïve	Basic question	Medium	Medium	Low	Medium	Medium	Medium
Straightforward	Direct instructions	High	High	Medium	High	High	High
Persona	Expert role	High	High	High	High	High	High
Constraint-Based	Detailed constraints	Very High	High	Very High	High	Very High	Very High
Structured Reasoning	Step-by-step structure	Very High	High	Very High	Very High	Very High	Very High
Few-Shot	Examples provided	High	High	High	High	High	High
STEP 8 – RESPONSE QUALITY ANALYSIS
Naïve Prompt

The naïve prompt produced a general solution. It identified common
technologies but did not provide enough implementation details.

Observation
Quality:
Moderate

Accuracy:
Moderate

Depth:
Low to Moderate
Straightforward Prompt

The straightforward prompt produced a more focused response by clearly
specifying the required technologies and expected outputs.

Observation
Quality:
Good

Accuracy:
Good

Depth:
Moderate to High
Persona Prompt

The Persona Pattern generated a more technically detailed response by
assigning the role of an experienced computer vision and machine learning
engineer.

Observation
Quality:
High

Accuracy:
High

Depth:
High
Constraint-Based Prompt

The constraint-based prompt produced a more practical architecture
because the technologies and implementation requirements were explicitly
defined.

Observation
Quality:
Very High

Accuracy:
High

Depth:
Very High
Structured Reasoning Prompt

The structured prompt produced a detailed engineering pipeline and
identified challenges and solutions at each stage.

Observation
Quality:
Very High

Accuracy:
High

Depth:
Very High
STEP 9 – EVALUATION TABLE
Criteria	Naïve	Straightforward	Persona	Constraint	Structured
Relevance	3/5	4/5	5/5	5/5	5/5
Accuracy	3/5	4/5	4/5	5/5	4/5
Completeness	2/5	4/5	5/5	5/5	5/5
Clarity	3/5	4/5	5/5	5/5	5/5
Feasibility	3/5	4/5	4/5	5/5	5/5
Usefulness	3/5	4/5	5/5	5/5	5/5
STEP 10 – AI TOOLS COMPARISON

The same engineering problem can be tested using multiple AI tools.

Feature	ChatGPT	Google Gemini	Microsoft Copilot
Technical Explanation	High	High	High
Architecture Generation	High	High	High
Code Suggestions	High	High	High
Debugging Assistance	High	High	High
Prompt Following	High	High	High
Output Organization	High	High	High
STEP 11 – ANALYSIS AND OBSERVATIONS

The experiment demonstrates that prompt structure significantly affects
the quality of AI-generated engineering solutions.

The naïve prompt produced a general response because it provided very
little context.

The straightforward prompt improved the response by explicitly defining
the expected information.

The Persona Pattern provided a more specialized technical response.

The constraint-based prompt was useful when specific technologies,
requirements, and limitations had to be followed.

The structured reasoning prompt produced a detailed engineering workflow
by dividing the problem into individual stages.

Few-shot prompting helped the AI understand the expected input-processing-
output format through examples.

KEY OBSERVATIONS
1. Prompt clarity improves response relevance.
2. Additional project context improves technical completeness.
3. Persona prompts can produce domain-specific responses.
4. Constraints help prevent irrelevant solutions.
5. Structured prompts produce organized engineering workflows.
6. Few-shot examples help communicate the expected response format.
7. Different prompting techniques are useful for different requirements.
8. AI-generated engineering solutions still require technical validation.
FINAL SELECTED PROMPTING TECHNIQUE
Constraint-Based + Structured Prompting

For this engineering problem, a combination of constraint-based prompting
and structured problem-solving is used for the final prompt.

This combination explicitly defines the project requirements,
technologies, constraints, expected architecture, and evaluation criteria.

REFINED / FINAL PROMPT
Act as an experienced computer vision and machine learning engineer
specializing in real-time eye tracking and adaptive human-computer
interaction.

I am developing a final-year project titled:

"Adaptive User Interface Design Using Artificial Intelligence Based
Eye Tracking Towards Personalized and Intelligent Human–Computer
Interaction."

Engineering Problem:
Develop a webcam-based system that estimates a user's screen-space
gaze coordinates and dynamically adapts a user interface according
to visual attention.

Requirements:

1. Capture video using a standard webcam.
2. Use MediaPipe Face Mesh for facial landmark detection.
3. Extract the eye regions from facial landmarks.
4. Convert eye images to grayscale.
5. Resize and normalize the eye images.
6. Use a CNN for spatial feature extraction.
7. Use an LSTM to model temporal eye-movement information.
8. Predict screen-space X and Y gaze coordinates.
9. Map gaze predictions to screen coordinates.
10. Estimate visual attention using gaze behavior.
11. Dynamically adapt interface elements based on attention.
12. Support near real-time operation.
13. Prefer local processing to protect user privacy.

Provide the solution using the following structure:

A. System architecture
B. Data preprocessing pipeline
C. CNN-LSTM model architecture
D. Training methodology
E. Gaze-coordinate prediction
F. Screen calibration and coordinate mapping
G. Attention estimation
H. Adaptive UI mechanism
I. Real-time optimization
J. Evaluation metrics
K. Technical limitations
L. Engineering validation

For each major component, mention its purpose, input, output,
implementation approach, and possible challenges.

Do not assume that the AI-generated solution is automatically correct.
Identify aspects that require experimental validation.
ENGINEERING VALIDATION

The AI-generated solution must be validated experimentally before being
used in the final project.

Validation Areas
Area	Validation Method
Gaze Accuracy	Measure gaze-coordinate error
Model Performance	Evaluate validation/test data
Real-Time Performance	Measure FPS and latency
Calibration	Test different screen positions
Robustness	Test different lighting conditions
User Interaction	Conduct usability testing
UI Adaptation	Compare adaptive and static interfaces
Privacy	Verify local processing of webcam data
POSSIBLE EVALUATION METRICS
1. Mean Angular Error
2. Mean Absolute Error
3. Gaze Prediction Accuracy
4. Frame Rate (FPS)
5. Processing Latency
6. Calibration Error
7. Task Completion Time
8. System Usability Scale (SUS)
9. User Satisfaction
LIMITATIONS
1. Webcam-based gaze tracking may be affected by lighting.
2. Head movement can affect gaze estimation.
3. Individual eye characteristics can vary significantly.
4. Calibration may be required for different users.
5. Prediction accuracy may be lower than dedicated eye trackers.
6. AI-generated architecture must be experimentally validated.
7. Real-time processing requires computational resources.
CONCLUSION

This experiment demonstrated how different prompting techniques can be
used to solve a real-world engineering problem from a final-year project.

The same AI eye-tracking problem was provided using naïve,
straightforward, persona-based, constraint-based, structured reasoning,
and few-shot prompts.

The comparison showed that adding relevant context, constraints,
examples, and a clear output structure generally produced more detailed
and practically useful responses than a simple prompt.

The experiment also demonstrated that AI-generated solutions should be
treated as engineering assistance rather than automatically validated
solutions. Important components such as gaze accuracy, model performance,
real-time latency, calibration, usability, and privacy must be verified
experimentally.

OUTPUT
The selected final-year engineering problem was successfully analyzed
using multiple prompting techniques.

Different prompts produced different levels of relevance, accuracy,
completeness, clarity, feasibility, and usefulness.

The final refined prompt generated a structured engineering solution
covering the complete webcam-based eye-tracking and adaptive UI pipeline.
RESULT

The prompt-based experiment was successfully executed.

Different prompting techniques were applied to the selected final-year
engineering problem. The generated responses were compared and analyzed
based on relevance, accuracy, completeness, clarity, feasibility, and
usefulness.

The experiment demonstrated that appropriate prompt design can improve
the quality and depth of AI-generated engineering solutions.
