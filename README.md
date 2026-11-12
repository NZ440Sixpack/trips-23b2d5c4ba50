# Craig trip calendar feed
- Source data: gen.py (EVENTS = timed flights, STAYS = all-day hotels and untimed bush flights). Booked facts only; every event carries its conf # or "conf # not on file".
- Update: edit/add/delete rows in gen.py, keep each UID unchanged for the same flight, run `python3 gen.py` -> trips.ics.
- Cancel a trip: delete its rows; the event disappears from subscribers on next refresh.
- Times stored in UTC (Apple shows local). Alarm 3 h before each flight. Feed hints refresh every 1 h.
- Republish: push trips.ics to the hosting location (same file path = same URL). Hosting: NOT YET SET UP (needs GitHub login on box: `gh auth login`), then commit trips.ics to a repo and use the raw.githubusercontent.com/<user>/<repo>/main/trips.ics URL as webcal://.
