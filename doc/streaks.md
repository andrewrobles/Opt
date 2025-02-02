[Changelog](../)
# Streaks

### Subtasks 
- [x] log the return body in the client
- [x] write api test cases
- [x] design get streak function
- [x] pass api test cases
- [x] integrate functionality with routes
- [x] handle edge cases
- [x] shorten streak by one
- [x] verify that the streak is returned
- [x] show the streak count in the client if the streak one or more days
- [x] use consistent parameter order for heatmap and getstreak functions

### getStreak(dates, start, today)
- convert today from a string into a dates object called `end`
- if dates array is empty
    - convert start into a dates object called `start`
- else
    - convert last element into a dates object called `start`
- calculate the number of days in between the two date objects using ChatGPT provided function `calculateDaysBetween`

### calculateDaysBetween(date1, date2)

```js
function calculateDaysBetween(date1, date2) {
    // Convert dates to Date objects
    const d1 = new Date(date1)
    const d2 = new Date(date2)

    // Get the difference in milliseconds
    const differenceInMillis = Math.abs(d2 - d1)

    // Convert milliseconds to days
    const differenceInDays = differenceInMillis / (1000 * 60 * 60 * 24)

    return differenceInDays
}

```
### edge cases
```
{
    "name":"Eat out",
    "dates":["2025-01-18"],
    "started":"2025-01-16",
    "streak":2
}
{
    "name":"Eat out",
    "dates":["2025-01-18"],
    "started":"2025-01-16",
    "streak":0
}
```