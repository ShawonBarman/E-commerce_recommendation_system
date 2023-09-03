# E-commerce_recommendation_system
<p>This project is a Django-based E-commerce recommendation system that uses a dataset scraped from Amazon to provide product recommendations to users. Here's a breakdown of the key components and functionality of your project:</p>

<ol>
  <li><strong>Project Structure:</strong> I have organized my Django project into two apps: 'recommendationSystem' (the main app) and 'myApp'.</li>
  <li><strong>Data Scraping:</strong> I scraped data from the Amazon website to build a dataset. This dataset likely contains information about various products, including their titles, categories, sub-categories, prices, ratings, and other relevant attributes.</li>
  <li><strong>Data Preprocessing:</strong> I used the scikit-learn library to perform data preprocessing, which includes feature transformation using a preprocessor and computing the cosine similarity matrix.</li>
  <li><strong>Machine Learning Models:</strong> I have trained machine learning models for clustering (K-Means) and DBSCAN. These models are loaded using joblib for further use in the recommendation system.</li>
  <li><strong>Recommendation Algorithm:</strong> The recommendation logic is primarily based on K-Means clustering and cosine similarity. When a user enters a product title, your system finds the cluster to which that product belongs and recommends other products within the same cluster based on cosine similarity scores.</li>
  <li><strong>Django Views:</strong> My 'myApp/views.py' contains Django view functions for handling user requests. The 'home' view renders the main page, and the 'get_recommendations' function generates product recommendations. The 'recommend_products' view handles POST requests when a user submits a product title and displays recommendations on the same page.</li>
  <li><strong>User Interface:</strong> I have created HTML templates (index.html) for the user interface, with input fields for users to enter product titles and a section to display recommended products. Bootstrap is used for styling.</li>
  <li><strong>Routing and URLs:</strong> I have defined URL patterns in the 'urls.py' files for routing user requests to the appropriate views.</li>
  <li><strong>Data Display:</strong> The recommended products are displayed in a responsive card layout, showing product details like title, category, sub-category, price, ratings, and total ratings.</li>
  <li><strong>Static Files:</strong> Static files like CSS are loaded using '{% static %}' template tags.</li>
  <li><strong>Database:</strong> In this project, I used a pre-built dataset (data.pkl) and machine learning models loaded from joblib files, rather than a database to store and retrieve product information.</li>
</ol>

<p>Overall, my Django E-commerce recommendation system uses machine learning to provide product recommendations based on user input and similarity scores, offering a user-friendly interface for interaction. Users can input a product title, and the system will suggest similar products from the dataset based on the clustering and similarity calculations you've implemented.</p>

<h3> Here are step-by-step instructions on how to run this Django-based E-commerce recommendation project in a user-friendly way:</h3>

<ol>
  <li><strong>Download the Project from GitHub and Unzip:</strong> Look for a "Code" button on this GitHub page. Click on it and select "Download ZIP" to download the project as a ZIP archive. And then locate the downloaded ZIP file on your computer (usually in your "Downloads" folder). After that right-click the ZIP file and select "Extract" or "Extract All" (the exact option may vary depending on your operating system). Then choose a destination folder where you want to extract the project files.</li>
  <li><strong>Navigate to Project Directory:</strong> Open the command prompt or terminal in this project root directory directly. Or open the command prompt or terminal on your computer and then use the 'cd' command to navigate to the root directory of this Django project. For example:
  <ul>
    <li>cd path/to/this/project</li>
  </ul>
  </li>
  <li><strong>Create a Virtual Environment:</strong> Create a virtual environment to isolate this project dependencies. This helps manage package versions.
  <ul>
    <li>python -m venv myenv</li>
  </ul>
  </li>
  <li><strong>Activate the Virtual Environment:</strong> Activate the virtual environment you just created. This ensures that the project uses the isolated environment.
  <ul>
    <li>myenv\Scripts\activate   (Windows)</li>
    <li>source myenv/bin/activate   (macOS/Linux)</li>
  </ul>
  </li>
  <li><strong>Upgrade Pip:</strong> Upgrade the 'pip' tool to the latest version to ensure you have the most recent package manager.
  <ul>
    <li>python.exe -m pip install --upgrade pip</li>
  </ul>
  </li>
  <li><strong>Install Django and Required Packages:</strong> Install Django and the necessary Python packages for this project.
  <ul>
    <li>pip install django</li>
    <li>pip install numpy</li>
    <li>pip install pandas</li>
    <li>pip install joblib</li>
    <li>pip install scikit-learn==1.2.2</li>
  </ul>
  </li>
  <li><strong>Database Setup:</strong> Run the following commands to set up the database for this Django project:
  <ul>
    <li>python manage.py makemigrations</li>
    <li>python manage.py migrate</li>
  </ul>
  </li>
  <li><strong>Run the Development Server:</strong> Start the Django development server to run this project locally:
  <ul>
    <li>python manage.py runserver</li>
  </ul>
  </li>
  <li><strong>Access This Project:</strong> Once the server is running, open a web browser and enter the following URL: 'http://localhost:8000/'. You should see this E-commerce recommendation system's home page.</li>
  <li><strong>Interact with the Recommendation System:</strong> On the home page, you can enter a product title and click the "Recommend" button to get product recommendations based on your input.</li>
</ol>

<p>Now this Django E-commerce recommendation project should be up and running locally. Users can access the recommendation system through their web browsers and receive product recommendations based on their input.</p>
