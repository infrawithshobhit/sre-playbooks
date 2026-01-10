# API Latency Incident

## What Dynatrace shows
- Increase in response time (p95, p99)
- Request queue length rising
- Error rate may start increasing
- Downstream service calls taking longer

## What this usually means
The API is waiting on something:
• Database  
• Another microservice  
• Network  
• Thread pool saturation  

Latency is usually a **symptom**, not the root cause.

## How to investigate
1. Open the affected service in Dynatrace
2. Check Service Flow to see which downstream dependency is slow
3. Look at database call duration and external API calls
4. Check thread pool and connection pool utilization
5. Correlate with recent deployments or config changes

## What usually fixes it
- Restart or scale the slow downstream service
- Rollback the latest release
- Increase connection pool or thread pool
- Temporarily bypass or rate-limit slow integrations

## How to prevent next time
- Add SLOs on latency
- Add dependency-level alerts
- Enable distributed tracing
- Load test before every major release
