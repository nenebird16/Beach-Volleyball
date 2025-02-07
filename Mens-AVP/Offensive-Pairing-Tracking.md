# Offensive Pairings Training Results

## Scoring System
Each player gets 5 opportunities per round. Points are awarded as follows:
- -1 point: Hitting error, block, or hit directly to defender (lack of execution)
- 0 points: Attack in the court that was dug but required a defensive dive
- +1 point: Kill (not in designated zone) or successful tool swing off block
- +2 points: Kill in designated zone
- Maximum score per round: 10 points (5 attempts × 2 points)

## Training Data

| Date | Round | Attack Side | Visual Cue | Location 1 | Location 2 | John | Ben | Nate |
|------|-------|-------------|------------|------------|------------|------|-----|------|
| 2025-02-07 | 1 | Left | Defender | Seam | Sharp Cross | 1 | 0 | 5 |
| 2025-02-07 | 2 | Right | Defender | Seam | Sharp Cross | 0 | 5 | 7 |
| 2025-02-07 | 3 | Left | Blocker | Seam | Hard Line | 0 | 1 | 0 |
| 2025-02-07 | 4 | Right | Blocker | Seam | Hard Line | 2 | 5 | 6 |
| 2025-02-07 | 5 | Right | Blocker | Seam | Hard Line | 3 | 8 | 1 |
| 2025-02-07 | 6 | Left | Live Blocker | Seam | Either Sideline | 8 | 4 | 1 |

## Performance Visualization

```mermaid
%%{init: {"theme": "default", "themeVariables": { "primaryColor": "#007fff" }}}%%
xychart-beta
    title "Player Performance by Round"
    x-axis "Round" [1, 2, 3, 4, 5, 6]
    y-axis "Score" [0, 10]
    line [1, 0, 0, 2, 3, 8] "John"
    line [0, 5, 1, 5, 8, 4] "Ben"
    line [5, 7, 0, 6, 1, 1] "Nate"
    legend show
    legend-position right
```

### Training Parameters
- Location 1: Always targeting Seam
- Location 2: Varies between Sharp Cross, Hard Line, and Either Sideline
- Visual Cues: Progress from Defender → Blocker → Live Blocker
- Attack Sides: Alternating between Left and Right

### Notes for Future Updates
- Add new practice sessions as new rows in the table
- Update the Mermaid chart data points to include new scores
- Date format: YYYY-MM-DD
- Scores range: -5 to 10 (minimum possible: 5 attempts × -1 point)