# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given Visitor count value is available
  When count of seating and parking change according to visitor count
  Then Visitor trend is shown

Scenario: Alert when seating capacity is full

  Given Count of seating and total seating capacity
  When count of seating is equal to total seating capacity
  Then Raise alert
