<h1>School Appointment API</h1>

<p>This project is a REST API built using Django and Django REST Framework to manage hospital appointment bookings. The API allows the creation, retrieval, update, and deletion of appointments, making it easy to manage patient consultations in a hospital setting.</p>

<h2>Project Structure</h2>

<pre>
📂 hospital-api
 ├── 📁 appointments        # App containing models, serializers, views, and URLs for appointments
 ├── 📁 hospital            # Main Django project folder
 ├── 📁 migrations          # Database migrations for the appointments app
 ├── 📁 static              # Static files (CSS, JS, etc.)
 ├── 📁 templates           # HTML templates for rendering views (if any)
 ├── manage.py              # Django management script
 ├── requirements.txt       # Python dependencies
 └── README.md              # This file
</pre>

<h2>Endpoints</h2>

<ul>
  <li><strong>GET /appointments/</strong> - List all appointments</li>
  <li><strong>POST /appointments/</strong> - Create a new appointment</li>
  <li><strong>GET /appointments/&lt;id&gt;/</strong> - Retrieve details of a specific appointment</li>
  <li><strong>PUT /appointments/&lt;id&gt;/</strong> - Update an existing appointment</li>
  <li><strong>DELETE /appointments/&lt;id&gt;/</strong> - Delete an appointment</li>
</ul>

<h2>Installation</h2>

<ol>
  <li>Clone this repository:
    <pre><code>git clone https://github.com/yourusername/hospital-api.git</code></pre>
  </li>
  <li>Navigate to the project directory:
    <pre><code>cd hospital-api</code></pre>
  </li>
  <li>Create and activate a virtual environment:
    <pre><code>python -m venv env
source env/bin/activate</code></pre>
  </li>
  <li>Install dependencies:
    <pre><code>pip install -r requirements.txt</code></pre>
  </li>
  <li>Run migrations to set up the database:
    <pre><code>python manage.py migrate</code></pre>
  </li>
  <li>Start the development server:
    <pre><code>python manage.py runserver</code></pre>
  </li>
</ol>

<h2>Authentication</h2>

<p>This API uses token-based authentication. You can obtain a token by sending a POST request to <code>/api-token-auth/</code> with valid credentials (username and password). Once you have the token, include it in the headers of your requests as follows:</p>

<pre><code>Authorization: Token your_token_here</code></pre>

<h2>Technologies Used</h2>

<ul>
  <li><strong>Django</strong>: Web framework for building the API.</li>
  <li><strong>Django REST Framework</strong>: Toolkit for building Web APIs.</li>
  <li><strong>SQLite</strong>: Default database for development (can be replaced with PostgreSQL or others).</li>
</ul>

<h2>Future Enhancements</h2>

<ul>
  <li>Implement pagination for large appointment lists.</li>
  <li>Add user roles (admin, doctor, patient) with different permissions.</li>
  <li>Extend appointment models to include more detailed information like diagnosis and doctor’s notes.</li>
</ul>
