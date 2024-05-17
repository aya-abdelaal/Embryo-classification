# Embryo-classification


### Embryo Selection Backend (Flask & Xception)

This repository contains the backend code for an embryo selection model using Flask and the Xception architecture. It classifies embryos as "good" or "bad" to aid in the selection process.

**Key Features:**

- **Flask Framework:** The backend is built using Flask, a popular Python microframework that provides a lightweight and flexible foundation for web applications.
- **Xception Model:** Leverages the Xception deep learning model, noted for its efficiency and performance in image classification tasks.
- **Good/Bad Classification:** Classifies uploaded embryo images into two categories: "good" and "bad" to assist in selection.
- **`predict` Route:** The `/predict` route is the core API endpoint where embryo images are sent for classification.

**Installation:**

1. **Clone the repository:**

   ```bash
   git clone https://<your-github-username>/embryo-selection-backend.git
   ```

2. **Create a virtual environment (recommended):**

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies:**

   ```bash
   pip install flask tensorflow numpy
   ```

**Deployment:**

Deployment on Render was done using the steps below:

1. **Create a Render account:** [https://render.com/](https://render.com/)
2. **Link your Git repository:** Connect your GitHub repository to your Render account.
3. **Configure environment variables:** You might need to define environment variables in Render for paths to your model file (hosted on Google Drive) or other settings.
4. **Deploy:** Follow Render's documentation for deployment specifics.

**Model File:**

The Xception model file is expected to be hosted on a cloud service. We hosted it on Google Drive for simplicity, and provided the appropriate path to the model file during deployment through environment variables.

**Using the Backend:**

1. **Start the Flask application:**

   ```bash
   python app.py
   ```

2. **Send a POST request to the `/predict` route:**

   The `/predict` route expects a POST request with the following structure:

   ```json
   {
     "image": image file
   }
   ```
   
3. **Receive the prediction response:**

   The backend will respond with a JSON object containing the predicted class ("good" or "bad") and a confidence score.


**Disclaimer:**

This model is intended for research purposes only and should not be used for medical decision making without proper validation and regulatory approval.
 

- **Model Training:** If the Xception model is not already trained, you'll need to provide instructions on how to train it or point users to the training script.
- **Data Preprocessing:** Describe any necessary preprocessing steps for the embryo images before sending them to the `/predict` route.
- **Confidence Scores:** If your model outputs confidence scores along with classifications, consider including them in the prediction response.
- **Error Handling:** Implement robust error handling in the backend to gracefully handle invalid requests or unexpected situations.
- **Testing:** Write unit tests to ensure the backend functionality works as expected.

By incorporating these suggestions, you can create a comprehensive and informative README file that effectively documents your embryo selection backend project.
