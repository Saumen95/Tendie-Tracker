
A web app for tracking expenses and budgets.

What are tendies?
Basically, money. Internet people call money 'tendies' and it's a word play on 'tender' (i.e. legal currency) and chicken tenders the food ¯\\\_(ツ)_/¯

## Features
  * Quick and bulk expensing
  * Budget creation and automatic tracking of expenses per budget
  * Custom spend categories
  * Dashboard with dynamic reporting
  * Detailed reports that break down spending
  * Add additional payers for tracking expenses across multiple people
  * Export your data directly into raw, CSV, and Excel
  * Responsive design - compatible with all major browsers and devices

## Built with
  * Front-end: [Bootstrap](https://getbootstrap.com/), [Chart.js](https://www.chartjs.org/), and [DataTables](https://datatables.net/)
    * [Tendietracker.com](https://www.tendietracker.com) uses [Webflow](https://www.webflow.com) and stills / mock ups from [Pixabay](https://pixabay.com) and [Burst](https://burst.shopify.com). Images are created with [Gimp](https://www.gimp.org/), [Figma](https://www.figma.com), and [ScreenToGif](https://www.screentogif.com/)
  * Back-end: [Flask](https://flask.palletsprojects.com)
  * Hosting: [Heroku](https://www.heroku.com)

## Demo
### Dashboard
<img src="https://raw.githubusercontent.com/eddyharrington/Tendie-Tracker/master/docs/dashboard.gif" height="400">

### Expensing
<img src="https://raw.githubusercontent.com/eddyharrington/Tendie-Tracker/master/docs/expensing.gif" height="400">

### Budgets
<img src="https://raw.githubusercontent.com/eddyharrington/Tendie-Tracker/master/docs/budgets.gif" height="400">

### Reports
<img src="https://raw.githubusercontent.com/eddyharrington/Tendie-Tracker/master/docs/reports.gif" height="400">

## Run it locally (written for Windows and VSCode)
1) Create a directory and clone the repo in it
```
git clone https://github.com/Saumen95/Tendie-Tracker.git
```
2) Create your virtual environment:
```
python -m venv env
```
3) Activate your virtual environment:
```
env\Scripts\activate
```
4) Install the dependencies:
```
pip install -r requirements.txt
```
5) Create the DB in Postgres (schema in repo [here](./dbCreateStatements-Postgres.txt))

6) Set your environment variables in .env file (otherwise hard code the string ```app.secret_key``` in app.py and ```engine``` in all of the ```.py``` files):
```
# App variable
SECRET_KEY=someRandomStringOfText

# DB variable
DATABASE_URL=postgres://{user}:{password}@{hostname}:{port}/{database-name}
```
7) Build and run the Flask app in VSCode

## Discussion
Some of the other things I wanted to add and may work on at a later time include:
  * Tests
  * User intro / walk-through of the app
  * Improved budget tracking (i.e calculates if your weekly / monthly spending is on-track or not)
  * Dark theme
  * Suggested spend categories
