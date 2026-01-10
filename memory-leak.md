# Memory Leak Incident

## What Dynatrace shows
- Gradually increasing memory usage
- GC running more frequently
- Pod restarts due to OOMKill
- Response times degrading before crash

## What this usually means
The application is allocating memory and not releasing it.
Over time, the JVM / process hits its limit and crashes.

## How to investigate
1. Check Dynatrace Memory consumption per process
2. Look at GC pause time and heap utilization
3. Identify which service version was deployed before memory started rising
4. Compare memory usage before and after deployment

## What usually fixes it
- Rollback the last deployment
- Restart affected pods
- Add heap dump and analyze in MAT
- Set memory limits and alerts to prevent silent buildup

## How to prevent next time
- Add memory trend alerts
- Monitor allocation rate
- Run load tests before production release
