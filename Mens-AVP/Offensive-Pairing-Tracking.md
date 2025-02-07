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

### Training Parameters
- Location 1: Always targeting Seam
- Location 2: Varies between Sharp Cross, Hard Line, and Either Sideline
- Visual Cues: Progress from Defender → Blocker → Live Blocker
- Attack Sides: Alternating between Left and Right

### Notes for Future Updates
- Add new practice sessions as new rows in the table
- Date format: YYYY-MM-DD
- Scores range: -5 to 10 (minimum possible: 5 attempts × -1 point)

### Future Visualization Plans
Currently, the data is presented in tabular format only. For optimal visualization of player progress, the following graph types should be considered:

1. **Line Charts** (Priority)
   - Best for showing player score progression over rounds
   - Can overlay multiple players for comparison
   - Helps identify trends and patterns in performance

2. **Heat Maps**
   - Useful for showing performance patterns across different conditions
   - Can highlight strengths/weaknesses in specific attack scenarios
   - Good for identifying optimal attack combinations

3. **Radar/Spider Charts**
   - Good for comparing performance across different visual cues
   - Can show balanced/unbalanced skill development
   - Useful for comparing left vs right side efficiency

4. **Bar Charts with Error Bars**
   - Good for showing average performance with variability
   - Can group by attack conditions or time periods
   - Useful for statistical analysis

Implementation options being considered:
- Custom web dashboard using React/Recharts
- Python with Matplotlib/Seaborn for automated graph generation
- Integration with existing analytics platforms