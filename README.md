# IMDb Sentiment Analysis

Sentiment analysis is a technique used to determine whether a piece of text expresses a positive, negative, or neutral sentiment. This project classifies IMDb movie reviews as either positive or negative using a sentiment analysis model built with Python's Flask framework and machine learning algorithms.

## Project Structure

The project includes the following key files:
- **`app.py`**: The main Flask application file where the sentiment analysis model is loaded and the web interface is created.
- **`Naive_Bayes_model_imdb.pkl`**: The serialized Naive Bayes model trained on the IMDb dataset.
- **`countVect_imdb.pkl`**: The serialized CountVectorizer used to transform text data into feature vectors.
- **`templates/home.html`**: The HTML template for the home page where users can input their reviews.
- **`templates/result.html`**: The HTML template for displaying the prediction result.
- **`Procfile`**: A file used for deploying the Flask application on platforms like Heroku.

## Steps to Use

1. **Environment Setup**:
    - Install the necessary dependencies using `pip`:
      ```sh
      pip install -r requirements.txt
      ```
    - Ensure that your Python environment has the correct versions of the required libraries, especially `scikit-learn`, `pandas`, and `flasgger`.

2. **Activate Virtual Environment**:
    - Navigate to the project directory and activate the virtual environment:
      ```sh
      cd myenv/Scripts
      activate
      ```

3. **Run the Application**:
    - Start the Flask web server:
      ```sh
      python app.py
      ```
    - The application will be accessible at `http://127.0.0.1:5000`.

4. **Input Review**:
    - On the home page, enter an IMDb movie review in the provided text box.
    - Click the 'Predict' button to get the sentiment classification.

5. **View Result**:
    - The result page will display whether the review is classified as positive or negative.

## Algorithms Used

1. **CountVectorizer**:
   - Converts a collection of text documents to a matrix of token counts. It transforms the text input into numerical data that can be used by machine learning models.

2. **Multinomial Naive Bayes**:
   - A probabilistic classifier based on applying Bayes' theorem with strong (naive) independence assumptions. It is particularly suited for classification with discrete features (like word counts).

## Deployment

To deploy this application on a platform like Heroku, include a `Procfile` in your project directory. This file specifies the commands that should be executed to start your application.

Example `Procfile`:




## Additional Notes

- Ensure that your Python environment matches the versions of the libraries used during the development of this project to avoid compatibility issues.
- If you encounter warnings related to version mismatches in scikit-learn, consider using the same version that was originally used to train the model or retrain the model with your current environment.


