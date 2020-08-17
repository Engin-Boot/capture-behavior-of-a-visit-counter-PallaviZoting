# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given Sensor is available at entry gate
  When Patients enter from gate
  Then visitor counter value increment by one

Scenario: Compute parking slots to reserve for visiting specialists

  Given visitor counter value is available
  When Specialists visit hospital
  Then Find parking available parking slot using aggregate visitor count, availability of beds and nursing staff
