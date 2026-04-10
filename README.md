# Liturgical Calendar Google Form Pre-Filler

Fetches liturgical calendar events from an ICS feed and generates
pre-filled Google Form URLs for the upcoming week (Monday–Saturday).

## Features
- Parses any standard `.ics` calendar URL
- Identifies the next Monday–Saturday window
- Generates pre-filled Google Form links with the liturgical day name and date
- Saves output to `prefilled_form_urls.txt`

## Prerequisites
- Python 3.7+
- A publicly accessible ICS calendar URL
- A Google Form with pre-fillable fields

Configuration
Set the following environment variables before running:

Variable	Description	Example
ICS_CALENDAR_URL	URL to the .ics liturgical calendar feed	https://example.com/calendar.ics
GOOGLE_FORM_URL	Base URL of your Google Form (pre-fill endpoint)	https://docs.google.com/forms/d/e/XXXXX/viewform
DAY_FIELD_ID	Google Form field ID for the liturgical day	entry.123456789
DATE_FIELD_ID	Google Form field ID for the date	entry.987654321
How to find Google Form field IDs
Open your Google Form
Click the three-dot menu → Get pre-filled link
Fill in sample data and click Get link
The URL will contain parameters like entry.123456789=SampleData
Those entry.XXXXXXXXX values are your field IDs
Setting environment variables
Linux/macOS:

bash
export ICS_CALENDAR_URL="https://example.com/calendar.ics"
export GOOGLE_FORM_URL="https://docs.google.com/forms/d/e/XXXXX/viewform"
export DAY_FIELD_ID="entry.123456789"
export DATE_FIELD_ID="entry.987654321"
Windows (PowerShell):

powershell
$env:ICS_CALENDAR_URL="https://example.com/calendar.ics"
$env:GOOGLE_FORM_URL="https://docs.google.com/forms/d/e/XXXXX/viewform"
$env:DAY_FIELD_ID="entry.123456789"
$env:DATE_FIELD_ID="entry.987654321"
Usage
bash
python liturgical_form_filler.py
Output
Console output showing the week's liturgical events and URLs
prefilled_form_urls.txt file with all generated links
