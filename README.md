# `python_init`

This is a platform/course for complete beginners to teach themselves programming, specifically in Python. Currently it's very much a WIP.

## Features

The course is a fully interactive 'book' which requires the user to run code in the provided editor or shell to advance:

![full](images/full.png)

The code at each step is checked automatically. Common mistakes can be caught and pointed out to the student. If needed, the student can get small hints to gradually guide them to the solution:

![hints](images/hints.png)

If they're still really stuck, they can reveal the solution bit by bit:

![solution](images/solution.png)

Several debuggers are provided, including [snoop](https://github.com/alexmojaki/snoop):

![snoop](images/snoop.png)

[birdseye](https://github.com/alexmojaki/birdseye):

![birdseye](images/birdseye.png)

and [Python Tutor](http://pythontutor.com/):

![pythontutor](images/pythontutor.png)

## Getting started

1. Clone the repository.
2. In the `backend` folder:
    1. Ensure the `python` command points to Python 3.8.
    2. Run `./setup.sh`. This will:
        1. Install `poetry` if needed.
        2. Create a virtualenv and install Python dependencies.
        3. Create a sqlite database, run migrations, and create a user.
    3. Activate the virtualenv with `poetry shell`.
    4. Run the backend development server with `./manage.py runserver`.
3. In the `frontend` folder:
    1. Ensure you have recent versions of `node` and `npm`.
    2. Run `npm install` to download dependencies.
    3. Run `npm start` to start the frontend development server.
4. Go to http://localhost:3000/accounts/login/ and login with the email "admin@example.com" and the password "admin".
5. You should be redirected to http://localhost:3000/course/ and see the start of the course: "Introducing The Shell".

## Controls

The course consists of *pages* and each page consists of *steps*. Each step requires that the user runs some code that satisfies the requirements of that step. Once they succeed, they are shown the next step. Once they complete all the steps in a page, they are shown the "Next page" button to move forward. They can click "Previous" if they want to review completed pages, but it doesn't affect their progress - any code they submit is still evaluated against the current step, and refreshing the page returns to the last page. Hopefully these basics (without the formal details) should become intuitively clear to the user as they try to use the site.

To explore the course more freely:

1. Click the hamburger menu icon in the top left.
2. Click Settings.
3. Turn Developer mode on.
4. This should give you two red buttons floating at the bottom of the screen. They change the currently active step, so you can move forward without having to complete exercises or backwards to test a step again.

At the beginning of the course only the shell is available to encourage quick exploration. After a few pages an editor is introduced to allow running full programs.

The course provides three debuggers to specially run code: snoop, PythonTutor, and birdseye. Each should only become available starting from a specific page which introduces that tool. No such page has been written yet for birdseye, so for now it's immediately available when the editor is introduced.
