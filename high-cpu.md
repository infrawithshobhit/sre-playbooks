# High CPU Incident

## What Dynatrace shows
• Host CPU > 85%
• Service response time increasing
• Thread pool saturation

## How to investigate
• Check top consuming processes
• Correlate with recent deployments
• Look for GC spikes

## What usually fixes it
• Rollback bad deployment
• Scale pods
• Kill runaway jobs
