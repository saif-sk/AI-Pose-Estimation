pose estimation using TensorFlow Lite, OpenCV, and a MoveNet model for tracking keypoints in real-time. The code captures live video, processes it to estimate keypoints, and uses the angles between joints to track movements like curls (for counting repetitions).

Key features of the code:

TensorFlow Lite Interpreter: It loads the MoveNet single-pose Lightning model.
OpenCV Video Capture: The video feed is captured in real-time using cv2.VideoCapture(0).
Keypoint Detection: Keypoints of the body are detected, such as the shoulders, elbows, and wrists. These are used to calculate the angles between joints.
Angle Calculation: A custom function calculate_angle() computes the angle between three points (right shoulder, elbow, and wrist).
Curl Detection: Logic is applied to count the number of curls based on the angle between the elbow and other joints.
Drawing Keypoints and Connections: The code uses cv2.circle and cv2.line to display keypoints and connect them visually on the frame.
