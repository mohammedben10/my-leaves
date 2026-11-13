🌿 My-Leaves — Distributed Plant Leaf Disease Detection System

A distributed deep learning application designed to detect and classify plant leaf diseases in real time. Built with a microservices architecture separating the web gateway from the AI inference engine via gRPC (protos), this system enables fast, scalable agricultural diagnostics.

🏗️ System Architecture

The project is structured into decoupled services communicating over high-performance RPC protocols:

ai_service/: Deep Learning inference service powered by a Convolutional Neural Network (CNN) responsible for image preprocessing, disease classification, and confidence scoring.

protos/: Protocol Buffers (.proto) definitions and generated gRPC stubs ensuring strict, low-latency communication between the gateway and the AI model.

web_gateway/: User-facing web application and admin dashboard allowing users to upload leaf images, visualize diagnostic results, and monitor system activity.

PROJECT_ANALYSIS.md: Detailed technical breakdown of the architecture, model fixes, and UI/UX workflows.

run_project.bat: Automated startup script for launching all services locally on Windows.

🛠️ Tech Stack

Deep Learning & Computer Vision: Python, TensorFlow / Keras (CNN), OpenCV, NumPy

Distributed Communication: gRPC, Protocol Buffers (protobuf)

Backend & Web Gateway: Python (FastAPI / Flask) / Web Frontend (HTML, CSS, JS)

Automation & Tooling: Batch scripting, Git / GitHub

🚀 Getting Started

Prerequisites

Python 3.9+

pip package manager

Installation & Execution

Clone the repository:

git clone https://github.com/mohammedben10/my-leaves.git
cd my-leaves


Install dependencies:

pip install -r ai_service/requirements.txt
pip install -r web_gateway/requirements.txt


Run the distributed system:
On Windows, execute the automation script to start both the gRPC AI server and the web gateway:

run_project.bat


(Alternatively, start ai_service and web_gateway manually in separate terminals).

📊 Workflow

Image Upload: The user submits a leaf image through the web_gateway interface.

gRPC Request: The gateway serializes the image payload using the contract defined in protos/ and sends it to ai_service.

Inference: The CNN model processes the normalized image and predicts the plant species and potential disease class.

Response & Dashboard: The prediction and confidence score are returned to the user and logged in the admin interface.

👥 Contributors

Mohammed Benkharraz (@mohammedben10)

Abdessamad Jamed (@AbdessamadJamed)

Houcine Aberhache (@Houcineaberhache)

Sara Daoudi (@Sara-Daoudi)
