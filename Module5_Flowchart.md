```mermaid
    Start([Start]) --> Init[Initialize Score = 0]

    Init --> Display[Display Categories and Available Questions]
    Display --> Select[User Selects Category and Value]

    Select --> Used{Question Already Used?}
    Used -- Yes --> Display
    Used -- No --> ShowQ[Display Question]

    ShowQ --> Input[Get User Answer]
    Input --> Check{Is Answer Correct?}

    Check -- Yes --> Add[Add Points]
    Check -- No --> Sub[Subtract Points]

    Add --> Update[Update Score]
    Sub --> Update

    Update --> Mark[Mark Question as Used]
    Mark --> Done{All Questions Used?}

    Done -- No --> Display
    Done -- Yes --> Final[Display Final Score]

    Final --> End([End])
    
