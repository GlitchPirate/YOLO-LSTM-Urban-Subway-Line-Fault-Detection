# YOLO-LSTM-Urban-Subway-Line-Fault-Detection
Code framework, for reference only.

1. 5 faults/detects：
1) Connectivity Issues:
√ Refers to poor or interrupted connections between lines
√ May be caused by temporary station closures, partial line suspensions, or transfer passage failures
√ Such issues can prevent passengers from completing their journeys as expected, increasing travel time
2) Capacity Bottlenecks:
√ Refers to situations where passenger flow exceeds the designed capacity of lines or stations
√ Common during peak hours or large events
√ These problems can lead to overcrowding, queue delays, and increased safety hazards
3) Signal Failures:
√ Refers to abnormalities in the signaling system that controls train operations
√ May result in reduced train speeds and extended intervals between trains
√These issues significantly impact overall operational efficiency and punctuality
4) Track Wear:
√ Refers to physical wear or damage to track facilities.
√ Usually related to the age of use, frequency of use, and quality of maintenance.
√ May cause increased train noise, decreased comfort, and potentially serious safety risks.
5) Transfer Obstacles:
√ Refers to issues with transfer facilities between different lines.
√ Includes excessively long transfer distances, unclear signage, and elevator/escalator failures.
√ Such problems can increase the time and difficulty of transfers for passengers, reducing the travel experience.

These types cover the most common issues in the subway system, including hardware facility problems (such as track wear), operational management issues (such as capacity bottlenecks), and systemic problems (such as signal failures). In practical applications, the system can expand to include more detailed fault types based on specific needs, such as:
√ Power supply failures
√ Ventilation system abnormalities
√ Safety monitoring equipment malfunctions
√ Platform door failures
√ Ticketing system anomalies, etc.
These fault types can be detected by analyzing data from various sources, such as passenger flow data, train operation data, equipment status data, and historical maintenance records, combined with deep learning models for predictive maintenance and fault warning.


2. Structure：
1) Spatial Feature Extraction of Subway Network (YOLO) - Using bit masks to store multi-line information for stations, with each line represented by a separate channel, effectively controlling computational complexity.
2) Temporal Feature Extraction (LSTM) - Supports independent feature extraction for each line, including line-specific maintenance, fault, and passenger flow information.
3) Feature Fusion and Line Obstacle Detection - Integrates spatial and temporal features to provide independent defect predictions for each line while supporting analysis of inter-line interactions.


3. Other:
1) Bit Masks for Storing Line Information: Efficiently represents a station's association with multiple lines using binary bit operations.
2) Multi-Channel Representation: Each line uses a separate channel, maintaining distinction between lines.
3) Line-Specific Temporal Features: Each line models its maintenance history and fault patterns independently.
4) Integrated Defect Detection: Capable of constructing independent models for each line as well as a unified integrated model.
