# Friends Tableau Dashboard

An interactive Tableau dashboard on the TV show **Friends** (1994–2004), built from episode-level data for all 10 seasons.

![Friends cast](images/friends-cast.jpg)

## What the dashboard shows

**Dashboard 1** brings together 11 worksheets:

| Element | What it shows |
|---|---|
| Season / Episode / Year | Episode selector tiles |
| Duration in Minutes | Episode runtime |
| Total Stars / Total Votes | IMDb-style rating and vote count |
| Description | Episode synopsis |
| DIRECTORS | Episodes directed by each director |
| Total Episodes By Season | Episode count per season |
| Total Stars By Season And Episodes | Average stars across seasons and episodes |
| Total Votes By Season And Episodes | Vote totals across seasons and episodes |

## The data

`data/Friends_dataset.csv` — 236 episodes, one row per episode:

| Column | Description |
|---|---|
| Episode title | Episode title (e.g. "The One Where Monica Gets a Roommate") |
| Description | Episode synopsis |
| Season | Season number (1–10) |
| Episode | Episode number within the season |
| Duration in minutes | Runtime (22–30 minutes) |
| Year | Original air year (1994–2004) |
| Director | Episode director |
| Total stars | Average rating (6.9–9.7) |
| Total votes | Number of ratings |

Most episodes were directed by Kevin Bright (54) and Gary Halvorson (54), followed by Michael Lembeck (24) and James Burrows (15).

## How to open it

1. Open `tableau/Friends_Dashboard.twb` in Tableau Desktop.
2. The workbook reads its data from `../data/Friends_dataset.csv` and its cast image from `../images/friends-cast.jpg`, relative to the workbook — keep the folder structure as it is and everything loads automatically.

## Files

```
friends-tableau-dashboard/
├── README.md
├── tableau/
│   └── Friends_Dashboard.twb   # The dashboard (Tableau 18.1 workbook format)
├── data/
│   └── Friends_dataset.csv     # 236 episodes
└── images/
    ├── friends-cast.jpg            # Cast photo used in the dashboard
    ├── friends-cast-couch.jpg      # Cast on the Central Perk couch
    └── friends-cast-milkshakes.jpg # Cast with milkshakes
```

## Notes

- The workbook originally pointed at absolute paths on a local Windows machine (`C:/Users/areef/OneDrive ...`). The data connection and the dashboard image were changed to the relative paths `../data` and `../images/friends-cast.jpg` so the project works anywhere; no analysis or formatting was changed.
- The dashboard image originally referenced a local file (`p183931_b_h10_af.jpg`) that was not included with the project. It now points to `images/friends-cast.jpg`.
- The dataset was converted from mixed Latin-1/UTF-8 encoding to clean UTF-8 (two "fiancé" descriptions); no values were changed.
- A separate Netflix dashboard project (Netflix_Dashboard.twb, Netflix_Dashboard__29392.twbr, Book1.twb, netflix_titles.csv) is not part of this repository.
