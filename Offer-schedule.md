The offer schedule is a way to display limits for an offers usage, in terms of days of week and/or hours of day.

## Schedule interpretation
* (day = *) 
  * Applies to all days.   
This will be applied to most offers, where there are no limits and thus no information about limits.
* (day = _INT_) 
  * Applies to number of day in week (1-7)
* (time_start = * && time_end = *)
  * No time limit, applies all day, only the day is displayed.
* (time_start = H:i && time_end = *) 
  * Offer has a start time, displayed as 'from H:i' | 'from 11:00'
* (time_start = * && time_end = TIME)
  * Offer has an end time, displayed as 'to H:i' | 'to 13:00'
* (time_start = H:i && time_end = TIME)
  * Offer has a start time and an end time, displayed as 'H:i - H:i' | '11:00 - 13:00' 

Several schedules can apply to the same day, schedules rules should be interpreted and combined to one _rule_ before output.
* (day = 1 && time_start = 10:00 && time_end 12:00)
* (day = 1 && time_start = 13:00 && time_end 15:00)
  * Displayed as 'Mondays 10:00 - 12:00 and 13:00 - 15:00'

An editor will choose to set a rule for all days _or_ for each day.  
A combination of (day = *) and (day = _INT_) is discouraged.    
A combination of rules for the same days with conflicting number of attributes set; (time_start = H:i || time_end = H:i) + (time_start = * || time_end = *) is discouraged.

## List shortening
The list can be simplified if the hours are the same, and several days can be combine into one _rule_.

### More than one day has the same hours
* (day = 1 && time_start = 12:00 && time_end = 14:00)  
  (day = 2 && time_start = 12:00 && time_end = *)  
  (day = 3 && time_start = 12:00 && time_end = 14:00)  
  (day = 5 && time_start = 12:00 && time_end = 14:00)  
  (day = 6 && time_start = 12:00 && time_end = *)  

  * Each of the days are listed before the hours:
    * Mondays, wednesdays and fridays 12:00-14:00
    * Tuesdays and saturdays from 12:00

### More than _two consecutive_ days have the same hours
* (day = 1 && time_start = 12:00 && time_end = 14:00)  
  (day = 2 && time_start = 12:00 && time_end = 14:00)  
  (day = 3 && time_start = 12:00 && time_end = 14:00)  
  (day = 5 && time_start = * && time_end = 15:00)  
  (day = 6 && time_start = * && time_end = 15:00)   

  * The days are displayed as a range
    * Mondays to wednesdays 12:00-14:0  
    * Saturdays and sundays to 15:00

## Conditional formatting and strings
* (All rules has day = * && time_start = _INT_ || time_end = _INT_)  
_The schedule is written as a paragraph without the day:_
  * 'This offer is valid H:i - H:i'
  * 'This offer is valid from H:i'  
  * 'This offer is valid to H:i'  
  * 'This offer is valid H:i - H:i and H:i - H:i'  

* (There are rules for more than one day but they all apply to the same hours, either separately or consecutively)  
_The schedule is written as a paragraph:_ 
  * 'This offer is valid tuesdays and wednesdays'
  * 'This offer is valid tuesdays - thursdays'
  * 'This offer is valid tuesdays and wednesdays H:i - H:i'
  * 'This offer is valid tuesdays - thursdays H:i - H:i'
  * 'This offer is valid tuesdays - thursdays from H:i'
  * 'This offer is valid tuesdays - thursdays to H:i'

* (There are rules for more than one day and they apply to different hours)  
_The schedule is written as a list with the 'this offer is valid' as the first row, and with a line break after each rule._
  * This offer is valid  
tuesdays and wednesdays H:i - H:i
fridays and saturdays H:i - H:i 
* This offer is valid 
tuesdays - thursdays H:i - H:i and H:i - H::i
fridays from H:i 

## Sorting
Any list with more than one entry will be sorted on 1: the first day in the rule, 2: the earliest time_start, 3: the earliest time_end in the rule.

## More examples

### Example 1
* (day = * && time_start = * && time_end = *)  
_No limit, no output_

### Example 2
* (day = * && time_start = 11:00 && time_end = 13:00)  
_Applies to all days, only time is displayed:_  
  * 11:00 - 13:00

### Example 3
* (day = 1 && time_start = 12:00 && time_end = *)  
  (day = 2 && time_start = 12:00 && time_end = *)  
  (day = 6 && time_start = 12:00 && time_end = 13:00)
  * Mondays and tuesdays from 12  
  * Saturdays 12:00 - 13:00





