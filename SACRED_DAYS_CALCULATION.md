# Sacred Days Calculation - How It Works

This document explains exactly how the AsantePost app calculates the sacred days of the Asante calendar. Please review and indicate any corrections needed.

---

## The Core Concept: The Adaduanan (42-Day Cycle)

The entire sacred calendar is built on a single repeating cycle called the **Adaduanan**, which is **42 days long** (6 weeks).

Every sacred day has a fixed position within this 42-day cycle. Once you know where **Day 0** (Akwasidae) falls, all other sacred days are determined automatically.

---

## Reference Date (Anchor Point)

The app uses **February 1, 2025** as the reference Akwasidae (Day 0).

All calculations work by measuring how many days have passed since this date, then using modulo 42 to find the current position in the cycle.

```
Formula:
   days_since_reference = (target_date - February 1, 2025) in days
   cycle_position = days_since_reference mod 42
   (if negative, add 42)
```

---

## Sacred Day Positions Within the 42-Day Cycle

Starting from Akwasidae (Day 0), the sacred days fall at these positions:

| Position | Day Type   | Meaning                         |
|----------|------------|----------------------------------|
| **0**    | Akwasidae  | Most sacred day; Asantehene sits in state |
| **1**    | Fodwoɔ     | Day of rest (day after Akwasidae) |
| **9**    | Fofie      | Day of purification and cleansing |
| **19**   | Dapaah     | Day of preparation               |
| **21**   | Awukudae   | Ancestor veneration (midpoint of cycle) |
| **22**   | Fodwoɔ     | Day of rest (day after Awukudae)  |
| **30**   | Fofie      | Day of purification and cleansing |
| **40**   | Dapaah     | Day of preparation               |

All other positions (2-8, 10-18, 20, 23-29, 31-39, 41) are **regular days** with no special significance.

---

## Worked Example

**Question:** What type of day is March 15, 2025?

1. Days since Feb 1, 2025 = **42 days**
2. 42 mod 42 = **0**
3. Position 0 = **Akwasidae**

**Question:** What type of day is February 22, 2025?

1. Days since Feb 1, 2025 = **21 days**
2. 21 mod 42 = **21**
3. Position 21 = **Awukudae**

---

## The 2025 Calendar (Hard-Coded Dates Currently in the App)

These are the specific dates the app shows for 2025. Please verify each one:

### January 2025
| Date       | Day of Week | Sacred Day |
|------------|-------------|------------|
| January 13 | Monday      | Dapaah     |
| January 14 | Tuesday     | Awukudae   |
| January 23 | Thursday    | Fofie      |
| January 31 | Friday      | Dapaah     |

### February 2025
| Date        | Day of Week | Sacred Day |
|-------------|-------------|------------|
| February 1  | Saturday    | Akwasidae  |
| February 2  | Sunday      | Fodwoɔ     |
| February 24 | Monday      | Dapaah     |
| February 25 | Tuesday     | Awukudae   |

### March 2025
| Date       | Day of Week | Sacred Day |
|------------|-------------|------------|
| March 6    | Thursday    | Fofie      |
| March 14   | Friday      | Dapaah     |
| March 15   | Saturday    | Akwasidae  |
| March 16   | Sunday      | Fodwoɔ     |

### April 2025
| Date       | Day of Week | Sacred Day |
|------------|-------------|------------|
| April 7    | Monday      | Dapaah     |
| April 8    | Tuesday     | Awukudae   |
| April 17   | Thursday    | Fofie      |
| April 25   | Friday      | Dapaah     |
| April 26   | Saturday    | Akwasidae  |
| April 27   | Sunday      | Fodwoɔ     |

### May 2025
| Date       | Day of Week | Sacred Day |
|------------|-------------|------------|
| May 19     | Monday      | Dapaah     |
| May 20     | Tuesday     | Awukudae   |
| May 29     | Thursday    | Fofie      |

### June 2025
| Date       | Day of Week | Sacred Day |
|------------|-------------|------------|
| June 6     | Friday      | Dapaah     |
| June 7     | Saturday    | Akwasidae  |
| June 8     | Sunday      | Fodwoɔ     |
| June 30    | Monday      | Dapaah     |

### July 2025
| Date       | Day of Week | Sacred Day |
|------------|-------------|------------|
| July 1     | Tuesday     | Awukudae   |
| July 10    | Thursday    | Fofie      |
| July 18    | Friday      | Dapaah     |
| July 19    | Saturday    | Akwasidae  |
| July 20    | Sunday      | Fodwoɔ     |

### August 2025
| Date       | Day of Week | Sacred Day |
|------------|-------------|------------|
| August 11  | Monday      | Dapaah     |
| August 12  | Tuesday     | Awukudae   |
| August 21  | Thursday    | Fofie      |
| August 29  | Friday      | Dapaah     |
| August 30  | Saturday    | Akwasidae  |
| August 31  | Sunday      | Fodwoɔ     |

### September 2025
| Date          | Day of Week | Sacred Day |
|---------------|-------------|------------|
| September 22  | Monday      | Dapaah     |
| September 23  | Tuesday     | Awukudae   |

### October 2025
| Date        | Day of Week | Sacred Day |
|-------------|-------------|------------|
| October 2   | Thursday    | Fofie      |
| October 10  | Friday      | Dapaah     |
| October 11  | Saturday    | Akwasidae  |
| October 12  | Sunday      | Fodwoɔ     |

### November 2025
| Date         | Day of Week | Sacred Day |
|--------------|-------------|------------|
| November 3   | Monday      | Dapaah     |
| November 4   | Tuesday     | Awukudae   |
| November 13  | Thursday    | Fofie      |
| November 21  | Friday      | Dapaah     |
| November 22  | Saturday    | Akwasidae  |
| November 23  | Sunday      | Fodwoɔ     |

### December 2025
| Date         | Day of Week | Sacred Day |
|--------------|-------------|------------|
| December 15  | Monday      | Dapaah     |
| December 16  | Tuesday     | Awukudae   |
| December 25  | Thursday    | Fofie      |

---

## Akan Day Names (Weekday Mapping)

The app also maps Gregorian weekdays to Akan day names:

| Gregorian  | Akan Name  | Associated With     |
|------------|------------|---------------------|
| Monday     | Dwowda     | Calmness            |
| Tuesday    | Benada     | Ocean               |
| Wednesday  | Wukuda     | Spider (Ananse)     |
| Thursday   | Yawda      | Earth               |
| Friday     | Fida       | Fertility           |
| Saturday   | Memeneda   | God                 |
| Sunday     | Kwasiada   | Soul / Spirit       |

---

## Questions for Review

1. **Is the 42-day cycle length correct?**
2. **Is February 1, 2025 correctly an Akwasidae?**
3. **Are the positions within the cycle correct?** (Especially: Fofie at day 9/30, Dapaah at day 19/40, Awukudae at day 21)
4. **Are all the 2025 dates listed above correct?**
5. **Are the Akan weekday name mappings correct?**
6. **Are there any sacred days missing that should be included?**

---

*Please mark any corrections directly on this document or provide feedback so I can update the app accordingly.*
