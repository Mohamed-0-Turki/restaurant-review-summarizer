
# 🍽️ Restaurant Review Summarization API

This FastAPI application summarizes user reviews for a restaurant using a pretrained NLP model. It provides an overview of positive and negative feedback, along with the average rating.

---

## 🚀 Features

- Accepts a list of restaurant reviews (with ratings and comments).
- Calculates the average rating.
- Separates and summarizes positive and negative reviews.
- Provides a concise overview of restaurant feedback.
- Swagger UI documentation.

---

## 🧪 Example Request

```json
POST /summarize_reviews

{
  "reviews": [
    {
      "id": 1,
      "customerId": 33,
      "restaurantId": 16,
      "rating": 5,
      "comment": "The food was amazing! The pasta was perfectly cooked and the flavors were authentic. The service was very attentive."
    },
    {
      "id": 2,
      "customerId": 33,
      "restaurantId": 16,
      "rating": 2,
      "comment": "The experience was disappointing. The food took too long to arrive and was cold by the time it got to our table."
    }
  ]
}
````

### 🔁 Example Response

```json
{
  "average_rating": 3.5,
  "positive_overview": "Customers appreciated the delicious food, especially the well-cooked pasta and attentive service.",
  "negative_overview": "Some customers were unhappy with long wait times and cold food upon arrival."
}
```

---

## 📦 Installation & Run

```bash
# 1. Clone the repository
git clone https://github.com/your-username/review-summarizer.git
cd review-summarizer

# 2. Create and activate a virtual environment
python -m venv venv
source venv/bin/activate       # Windows: venv\Scripts\activate

# 3. Install required packages
pip install fastapi uvicorn transformers torch

# 4. Run the server
uvicorn main:app --reload
```

---

## 📘 API Docs

Once the server is running:

* Swagger UI: [http://localhost:8000/docs](http://localhost:8000/docs)
* ReDoc: [http://localhost:8000/redoc](http://localhost:8000/redoc)

---

## 🛠️ Notes

* The model used is `facebook/bart-large-cnn` via Hugging Face Transformers.
* First-time model loading may take some time and disk space (\~1.5–2 GB).

---

## 📄 License

This project is open-source and free to use under the MIT License.

```
