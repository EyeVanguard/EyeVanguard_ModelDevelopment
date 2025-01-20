# Model Development 🧠📈

This repository focuses on developing and deploying machine learning models for the AI-Powered Glaucoma Detection Platform, **EyeVanguard**. Here, we aim to create robust, scalable, and efficient models to analyze FUNDUS images and provide accurate glaucoma detection. This repository also includes MLOps integration for seamless development, deployment, and monitoring of AI models.

---

## 📂 **Project Structure**

```
modeldevelopment/
├── data/                     # Dataset storage and preprocessing scripts
│   ├── raw/                  # Raw dataset files
│   ├── processed/            # Preprocessed datasets
│   ├── preprocess.py         # Script for data cleaning and transformation
├── models/                   # Trained AI models and training scripts
│   ├── glaucoma_detection.py # Model architecture and training pipeline
│   ├── evaluate.py           # Model evaluation script
│   ├── saved_models/         # Directory for saved models
├── pipelines/                # MLOps pipelines for CI/CD
│   ├── train_pipeline.yml    # Pipeline for training and evaluating models
│   ├── deploy_pipeline.yml   # Pipeline for model deployment
├── tests/                    # Unit tests for models and preprocessing
│   ├── test_preprocess.py    # Test cases for data preprocessing
│   ├── test_model.py         # Test cases for model performance
├── scripts/                  # Utility scripts for various tasks
│   ├── inference.py          # Script for running inference with trained models
│   ├── upload_to_db.py       # Script for pushing model results to the database
├── database/                 # PostgreSQL integration for model outputs
│   ├── schema.sql            # Database schema for storing analysis results
│   ├── queries.sql           # SQL queries for accessing and updating data
├── Dockerfile                # Docker configuration for containerizing model development
├── docker-compose.yml        # Docker Compose for integrating services
├── requirements.txt          # Python dependencies
├── .env                      # Environment variables for the project
├── README.md                 # Documentation for the repository (you are here!)
└── .gitignore                # Git ignore rules
```

---

## 🚀 **Features**

- **Glaucoma Detection Model**: State-of-the-art AI model for analyzing FUNDUS images.
- **Data Preprocessing**: Robust scripts for cleaning and preparing datasets.
- **MLOps Pipelines**: Automating model training, testing, and deployment using CI/CD.
- **PostgreSQL Integration**: Save and manage detection results in a relational database.
- **Docker Support**: Containerization for consistent development and deployment.

---

## 📦 **Getting Started**

### 🖥️ **Prerequisites**

Ensure you have the following installed:

- **Python 3.x** and **pip**
- **Docker** and **Docker Compose**
- **PostgreSQL** (for the database)

### 🛠️ **Setup Instructions**

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/EyeVanguard/modeldevelopment.git
    cd modeldevelopment
    ```

2. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **Set Up Environment Variables**:
    Create a `.env` file with the following keys:
    ```env
    DATABASE_URL=postgresql://username:password@localhost:5432/glaucoma_db
    ```

4. **Run Preprocessing**:
    ```bash
    python data/preprocess.py
    ```

5. **Train the Model**:
    ```bash
    python models/glaucoma_detection.py
    ```

6. **Run Unit Tests**:
    ```bash
    pytest tests/
    ```

---

## 📊 **MLOps Integration**

This repository includes CI/CD pipelines to streamline the development and deployment process:

- **Training Pipeline**: Automatically trains and evaluates models on new datasets.
- **Deployment Pipeline**: Deploys the best-performing model to production.
- **Monitoring**: Tracks model performance and database updates.

### 🛠️ **Run Pipelines Locally**

To test pipelines locally, use the following commands:

```bash
# Train pipeline
docker-compose -f pipelines/train_pipeline.yml up

# Deploy pipeline
docker-compose -f pipelines/deploy_pipeline.yml up
```

---

## 📚 **Documentation**

- **Model Development**: Refer to [models/glaucoma_detection.py](models/glaucoma_detection.py) for detailed implementation.
- **Preprocessing**: See [data/preprocess.py](data/preprocess.py) for dataset preparation steps.
- **Database**: SQL schemas and queries are available in the `database/` folder.

---

## 🔮 **Future Enhancements**

- **Hyperparameter Optimization**: Automate hyperparameter tuning for better performance.
- **Advanced Models**: Incorporate ensemble learning for improved accuracy.
- **Model Monitoring**: Implement tools like Prometheus and Grafana for monitoring model performance.

---

## 🙌 Contributors

This project is developed collaboratively under the EyeVanguard GitHub organization.

---
