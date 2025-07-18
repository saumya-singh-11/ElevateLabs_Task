# Data Cleaning Summary – Medical Appointment No-Shows

This dataset originally contained 300+ rows with various data quality issues and was generated by using ChatGPT. The following cleaning steps were applied in the sheet titled "Cleaned_Data":

# General Cleaning
- Removed duplicate records
- Ensured consistent column formatting and headers

# Gender
- Standardized all values (e.g., female, FEMALE, male → Female, Male)
- Replaced missing values with "Unknown"

# Dates
- Verified ScheduledDate and AppointmentDate formats
- Calculated a new column `DaysBetween` to measure lead time between scheduling and appointment
- Flagged and excluded any logically invalid date entries (none found)

# Age
- Replaced outlier values (e.g., -1, 200) and blanks with the median age
- Ensured all values fall within a realistic human age range (0–120)

# Neighbourhood
- Replaced missing or corrupted entries with "Unknown"
- Capitalised the first letters

# Medical & Demographic Flags
- Verified that all binary columns (Diabetes, Hypertension, Alcoholism, Scholarship, SMS_received) contain only 0 or 1

# No-show
- Standardized to only "Yes" or "No"
- Removed rows with missing or invalid No-show values

