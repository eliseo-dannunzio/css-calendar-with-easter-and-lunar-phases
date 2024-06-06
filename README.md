# css-calendar-with-easter-and-lunar-phases

So, some time back I created a VERY clunky CSS/HTML calendar, it was using a lot of unnecessary checkboxes and labels  for the initial UI. While it worked, it was very UI un-friendly.

Fast forward a few years, **:has()** is now a reality and functions like **mod()**, **min()** and **max()** are more prominent. The rules have changed and there are a few more features:

1. The clunky checkbox and label system from the original version has now been replaced with `SELECT` tags and are now being recognized using the new `:has()` selector allowing a more intuitive UI.
2. A section on the bottom of the calendar indicating the date of Easter for that year. This value gets recalculated when the year is updated from the UI.
3. A literal Easter egg will appear over the respective date indicated in (2)
4. I've also provided functionality to calculate lunar phases for each date, which also update when the month or year are updated. NB: This uses the eight unicode lunar transitions, and so isn't
   terribly accurate in terms of the display as there are also transitions between these eight phases, but this is suitable enough to give the user a general idea of the current phase the moon
   is in on that date.
5. You'll note that **calc()** is not being used anywhere. What I've found over the last few months is that `calc()` isn't really needed as `max()` has an implied `calc()` which allows calculations
   to be performed without the overhead that browsers impose when encountering `calc()`. The `calc()` function is notorious for building up a memory overhead that causes memory to stack up within
   the browser only to hit a limit when `calc()` is nested around 100 levels. The `max()` function somehow circumvents this and prevents this from happening. This has allowed more calculations to
   be performed and thus has allowed me to even get this far with the project with all these new features.

Why do this? To push the limits of CSS and HTML and see how far I can go with this sort of thing... I love what i've been able to do with CSS, and showing others that it's not just a styling 
framework, but also a computational and programming framework, provided it's done right.

Where to from here? I'm now looking into the possibility of whether I can use these new features to push CSS even further and make a chess engine... Who knows?