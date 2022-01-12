### Bootstrap project on IDE

If you start this project you have to:

* Install and configure Python environment.
    Ideally [Anaconda](https://www.anaconda.com/download/).

    Then create an env:
    ```
    conda create --name pet python=3.9
    ```

    Here is the configuration settings for PyCharm:
    PyCharm --> Preferences --> Project: pet --> Project Interpreter --> Add New (plus sign)

* Install all the dependencies. Make sure this is the same pip that belongs to python you've used in IDE:
    ```
    conda activate pet
    pip install -r requirements.txt
    ```

* Upload data structure to database.
    Database in Dev environment is SQLite. It will be automatically created under project directory.
    But you have to create tables yourself. Make sure you use the same python as configured in IDE.
    ```
    python manage.py migrate
    ```

