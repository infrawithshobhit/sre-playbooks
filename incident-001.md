# Incident 001 – High API Latency After Deployment

## What happened
After a production deployment, API latency jumped from 200ms to 4s.
Customers started timing out.

## What Dynatrace showed
- Database calls were 5x slower
- Connection pool was saturated
- Thread pool was full

## Root cause
A new query was added without an index, causing table scans.

## What we did
- Rolled back the deployment
- Added the missing index
- Increased DB connections temporarily

## Outcome
Latency returned to normal within 18 minutes.
No data loss. Limited customer impact.

## What we learned
Always analyze query plans before production releases.
