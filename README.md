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
