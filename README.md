# Job Platform Project

მოკლე აღწერა:
ეს არის Django-ზე აგებული დასაქმების პლატფორმა, რომელიც უზრუნველყოფს:
- მომხმარებლის რეგისტრაციას და ლოგინს
- მომხმარებლის ტიპების მართვას: დამსაქმებელი, სამუშაოს მაძიებელი, ადმინისტრატორი
- API endpoints-ებს მონაცემების წაკითხვისა და დასატესტად

## მოთხოვნები
- Python 3.11+
- Django 5.x
- სხვა საჭირო პაკეტები `requirements.txt`-ში

## ინსტალაცია
1. კლონირება:
```bash
git clone https://github.com/username/job-platform-project.git
cd job-platform-project
ვირტუალური გარემოს შექმნა და აქტივაცია:

bash
Copy code
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
პაკეტების ინსტალაცია:

bash
Copy code
pip install -r requirements.txt
ბაზის მიგრაცია:

bash
Copy code
python manage.py migrate
სერვერის გაშვება
bash
Copy code
python manage.py runserver
დასაშვები URL: http://127.0.0.1:8000/

API ტესტირება
Swagger UI: http://127.0.0.1:8000/api/swagger/

ან Postman-ის გამოყენებით:

მომხმარებლის რეგისტრაცია:

http
Copy code
POST /api/users/
Content-Type: application/json

{
  "username": "sandro",
  "email": "sandro@example.com",
  "password": "123456",
  "user_type": "employer"
}
მომხმარებლის მიღება:

http
Copy code
GET /api/users/
Authorization: Token <YOUR_TOKEN>
