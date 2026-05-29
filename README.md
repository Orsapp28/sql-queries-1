# SQL Queries 1

Write SQL queries against the [cars database](https://github.com/CP-Evenings-and-Weekends/cars-database) to answer the questions below.  Save each answer (the query *and* the result) in `answers.txt`.

## Setup

Get the [cars database](https://github.com/CP-Evenings-and-Weekends/cars-database) running locally before you start — follow the setup instructions in that repo (it runs in Docker).

Tables you'll use today: `AppUser`, `UserProfile`, `Car`, `CarModel`.

## Requirements

Answer each of the following with a single SQL query:

1. How many app users are there?
2. How many app users have a first name beginning with "R"?
3. Who are the first 5 users sorted by last name?
4. What is the average mileage of a car?
5. What is the average mileage of a car with 3 or more previous owners?
6. What is the average mileage of a car with 3 or more previous owners manufactured after 2008?
7. How long is the longest model name?
8. How many users live in Chicago?
9. How many users live in cities with the word "Park" in their name?

> Hint: today's lesson covered `SELECT`, `WHERE`, `LIMIT`, `ORDER BY`, and aggregate functions (`COUNT`, `AVG`, `MIN`, `MAX`).  You don't need `JOIN` (that's tomorrow) — questions about user location can be answered directly from the `UserProfile` table.

## Things to think about
- For question 7, what's the difference between `LENGTH(model)` and `CHAR_LENGTH(model)` on a text column?
- `AVG` returns a `numeric` that can have a lot of decimal places.  How would you round it to 2 places?
- For "first name beginning with R" — what's the difference between `LIKE 'R%'` and `LIKE 'r%'`?  How would you make the match case-insensitive?

## Stretch
- Re-do question 6 using `BETWEEN` for the manufacture year range (say, 2008–2015).
- Find the user whose email is the *longest* — `ORDER BY` + `LIMIT`.
- For each manufacture year that has at least one car, report how many cars that year has.  (You'll need `GROUP BY` — sneak peek at tomorrow.)

> Stuck? Have a code error? Use the ["4 Before Me"](https://docs.google.com/document/d/1nseOs5oabYBKNHfwJZNAR7GlU0zkZxNagsw63AD7XV0/edit) debugging checklist to help you solve it!
