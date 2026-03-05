🧬 SeedGenomics: Neural Morphological Classifier
SeedGenomics is an AI-driven analytical suite designed for the automated taxonomic classification of pumpkin seed varieties (Çerçevelik and Ürgüp Sivrisi). By transitioning from subjective manual sorting to objective Quantitative Morphological Analysis, this system ensures industrial-grade precision in seed phenotyping.

💎 Key Highlights
Core Logic: Utilizes a Random Forest Ensemble learner to map non-linear relationships between seed geometry and genetic variety.

The Interface: A bespoke Glassmorphic Dashboard featuring a "Split-Pane" architecture—merging a high-contrast dark-mode analytics engine with a clean user input terminal.

Performance: Ultra-low latency inference engine (Sub-20ms) powered by a Flask-optimized micro-backend.

Data Integrity: Integrated MinMaxScaler pipeline ensures that feature magnitude (e.g., Area vs. Solidity) doesn't bias the classification outcome.

🛠️ The Architecture
Tech Stack
Intelligence: Scikit-learn, NumPy, Pandas (Random Forest Regressor/Classifier)

Infrastructure: Python 3.x & Flask WSGI Server

Frontend: Modern CSS3 (Glassmorphism), Vanilla JS (Interactions), HTML5

Project Topology
Plaintext
SeedGenomics/
├── static/css/style.css       # Glassmorphism UI Logic & Keyframe Animations
├── templates/
│   ├── index.html            # Primary Analytic Dashboard
│   └── predict.html          # Dynamic Result Verification Card
├── app.py                    # Flask Gateway & Model Wrapper
├── model_building.ipynb      # Feature Engineering & Hyperparameter Tuning
├── model.pkl                 # Serialized Random Forest Model
├── scaler.pkl                # Pre-fitted Feature Normalization Pipeline
└── Pumpkin_Seeds_Dataset.xlsx# Primary Morphological Dataset
🧠 Algorithmic Workflow
The system processes data through a four-stage pipeline to ensure the 98.8% accuracy threshold is maintained:

Normalization: Input vectors (Area, Perimeter, etc.) are transformed using the saved scaler.pkl to align with the training distribution.

Ensemble Inference: The Random Forest model aggregates votes from multiple decision trees to minimize variance and prevent overfitting.

Visual Processing: The frontend initiates a "Geometry Computation" pulse, providing immediate UX feedback while the backend calculates the result.

Classification: The output is decoded from binary (0/1) to the specific biological variety and rendered on the results card.

🚀 Deployment & Usage
1. Environment Setup
Bash
pip install flask scikit-learn pandas numpy openpyxl
2. Model Initialization
Run all cells in model_building.ipynb to execute the Grid Search optimization and generate your local .pkl binaries.

3. Launching the Engine
Bash
python app.py
Access the dashboard at: http://127.0.0.1:5000/

🔭 Roadmap
Vision 2.0: Integration of Computer Vision (CNNs) for direct image-to-classification processing.

Edge Computing: Conversion to TFLite for deployment on IoT sorting hardware.

Global Expansion: Expanding the dataset to include Hulled and Styrian varieties.

Artificial Intelligence Internship Program | Project Portfolio
Developed by Abhishek Magdum