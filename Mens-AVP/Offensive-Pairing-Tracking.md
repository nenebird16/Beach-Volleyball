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
graph TD
    subgraph Results["Player Performance by Round"]
        style Results fill:#f5f5f5,stroke:#333,stroke-width:2px
        
        %% Create nodes for each score
        J1[John R1: 1]
        J2[John R2: 0]
        J3[John R3: 0]
        J4[John R4: 2]
        J5[John R5: 3]
        J6[John R6: 8]
        
        B1[Ben R1: 0]
        B2[Ben R2: 5]
        B3[Ben R3: 1]
        B4[Ben R4: 5]
        B5[Ben R5: 8]
        B6[Ben R6: 4]
        
        N1[Nate R1: 5]
        N2[Nate R2: 7]
        N3[Nate R3: 0]
        N4[Nate R4: 6]
        N5[Nate R5: 1]
        N6[Nate R6: 1]
        
        %% Connect nodes in sequence
        J1 --> J2 --> J3 --> J4 --> J5 --> J6
        B1 --> B2 --> B3 --> B4 --> B5 --> B6
        N1 --> N2 --> N3 --> N4 --> N5 --> N6
        
        %% Style for John's line
        style J1 fill:#8884d8,stroke:#8884d8,stroke-width:2px
        style J2 fill:#8884d8,stroke:#8884d8,stroke-width:2px
        style J3 fill:#8884d8,stroke:#8884d8,stroke-width:2px
        style J4 fill:#8884d8,stroke:#8884d8,stroke-width:2px
        style J5 fill:#8884d8,stroke:#8884d8,stroke-width:2px
        style J6 fill:#8884d8,stroke:#8884d8,stroke-width:2px
        
        %% Style for Ben's line
        style B1 fill:#82ca9d,stroke:#82ca9d,stroke-width:2px
        style B2 fill:#82ca9d,stroke:#82ca9d,stroke-width:2px
        style B3 fill:#82ca9d,stroke:#82ca9d,stroke-width:2px
        style B4 fill:#82ca9d,stroke:#82ca9d,stroke-width:2px
        style B5 fill:#82ca9d,stroke:#82ca9d,stroke-width:2px
        style B6 fill:#82ca9d,stroke:#82ca9d,stroke-width:2px
        
        %% Style for Nate's line
        style N1 fill:#ffc658,stroke:#ffc658,stroke-width:2px
        style N2 fill:#ffc658,stroke:#ffc658,stroke-width:2px
        style N3 fill:#ffc658,stroke:#ffc658,stroke-width:2px
        style N4 fill:#ffc658,stroke:#ffc658,stroke-width:2px
        style N5 fill:#ffc658,stroke:#ffc658,stroke-width:2px
        style N6 fill:#ffc658,stroke:#ffc658,stroke-width:2px
    end
```

### Training Parameters
- Location 1: Always targeting Seam
- Location 2: Varies between Sharp Cross, Hard Line, and Either Sideline
- Visual Cues: Progress from Defender → Blocker → Live Blocker
- Attack Sides: Alternating between Left and Right

### Notes for Future Updates
- Add new practice sessions as new rows in the table
- Update visualization to include new scores
- Date format: YYYY-MM-DD
- Scores range: -5 to 10 (minimum possible: 5 attempts × -1 point)