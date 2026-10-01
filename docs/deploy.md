# Deploy checklist

## Before the deploy
- Confirm the release tag and the change list with the service owner
- Check that the last CI run on the tag is green
- Post the deploy notice in the team channel

## During the deploy
- Deploy to one canary instance first and watch error rates for ten minutes
- Roll out to the remaining instances in two batches

## After the deploy
- Confirm the health checks and the dashboards are normal
- Close the deploy notice with the final status

## Rollback
- Roll back if error rates stay above the alert threshold for five minutes after the canary
- Redeploy the previous release tag to all instances in one batch
- Post the rollback and the reason in the team channel, then open an incident if users were affected
