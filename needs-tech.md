# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given Visitor count is available
  When Server restrarts
  Then recover visitor count value from aggreggate count value

Scenario: Reconcile counts if the sensor is offline for a while

  Given previous visitor counter value is available
  When Sensor turns off
  Then Update visitor counter value offline and combine it with
  previous data when sensor turns on
