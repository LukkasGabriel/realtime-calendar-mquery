# Dynamic Date List Generator (Power Query M)

This Power Query (M) snippet generates a dynamic list of dates starting from a user-defined start date up to the current date on the user's local machine. The list updates automatically every day based on the system's local date.

## How it works

- You set the starting date by changing the value of `#date(YYYY,MM,DD)`.
- The script calculates the number of days from that start date up to today.
- It generates a list of dates incrementing day by day.
- The list refreshes dynamically based on the user's local system date.

## Code snippet

```m
= List.Dates(
    #date(2025,6,1),
    Number.From(DateTime.LocalNow()) - Number.From(#date(2025,6,1)),
    #duration(1,0,0,0)
)
````
## How to use

- Replace the first #date(2025,6,1) with your desired start date.

- Make sure the second Number.From(#date(2025,6,1)) matches the start date.

- Load this query in Power BI or Excel Power Query.

- Refresh to see the list update automatically based on your computer's current date.

## Example
- If you set the start date to #date(2025,6,1) and today is 2025-06-10, the list will contain all dates from June 1, 2025 to June 10, 2025.



