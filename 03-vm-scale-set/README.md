# Azure VM Scale Set and Autoscale Lab

Status: Documentation draft. Screenshot upload and evidence review pending.

## Objective

Document an Azure VM Scale Set lab completed while studying Azure fundamentals through CBT Nuggets. The walkthrough covers deployment, autoscale configuration, instance observations, and run-history review.

## Evidence and validation

The screenshot filenames have been organized, but the image contents have not yet been independently reviewed for this documentation. Captions below describe the planned evidence, not verified results. Exact settings, resource names, CPU thresholds, evaluation windows, cooldown periods, instance counts, and observed scaling events will be documented after review.

Configured autoscale rules and observed scaling events will be reported separately. This draft does not claim that a scale-out or scale-in event occurred.

## Walkthrough

### 1. Autoscale configuration

Planned evidence: instance limits and CPU-based autoscale rules. Exact values pending screenshot review.

![Autoscale instance limits](screenshots/01-vmss-autoscale-instance-limits.jpg)

![Autoscale CPU rules](screenshots/02-vmss-autoscale-cpu-rules.jpg)

### 2. Deployment configuration review

Planned evidence: basics, disks, networking, health, and advanced settings reviewed before deployment.

![Review basics](screenshots/03-vmss-review-basics.jpg)

![Review disks and networking](screenshots/04-vmss-review-disks-networking.jpg)

![Review health and advanced settings](screenshots/05-vmss-review-health-advanced.jpg)

### 3. Deployment and instance observations

Planned evidence: deployment completion, resource overview, and observed instances. Deployment status and instance counts pending screenshot review.

![Deployment completion](screenshots/06-vmss-deployment-complete.jpg)

![Running overview](screenshots/07-vmss-running-overview.jpg)

![Observed instances](screenshots/08-vmss-observed-instances.jpg)

### 4. Autoscale settings review

Planned evidence: autoscale overview, rules and limits, and individual scale-out and scale-in rule settings.

![Autoscale overview](screenshots/09-vmss-autoscale-overview.jpg)

![Autoscale rules and limits](screenshots/10-vmss-autoscale-rules-and-limits.jpg)

![Scale-out rule](screenshots/11-vmss-scale-out-rule.jpg)

![Scale-in rule](screenshots/12-vmss-scale-in-rule.jpg)

### 5. Run-history review

Use the latest one-hour capture for the main walkthrough. Observed events and their outcomes are pending review; an empty history will be documented as such rather than treated as proof of successful scaling.

![Autoscale run history](screenshots/13-vmss-autoscale-run-history.jpg)

## Results

Pending evidence review:

- Deployment outcome and resource configuration.
- Minimum, maximum, default, and observed instance counts.
- Scale-out and scale-in thresholds, durations, actions, and cooldowns.
- Whether the captured run history shows any scaling events.
- Lessons learned and limitations of the evidence.

## Cleanup

Cleanup status has not been confirmed. Do not interpret this documentation as evidence that the lab resources were deleted.

## Optional reference captures

These captures are supplementary and are not part of the numbered walkthrough:

- `reference-vmss-scaling-overview-before-edits.jpg`
- `reference-vmss-run-history-seven-day-view.jpg`

## Documentation checklist

- [x] Organize screenshot filenames.
- [ ] Upload the 13 numbered screenshots.
- [ ] Review screenshots for sensitive information before publishing images.
- [ ] Validate settings and replace draft captions with observed details.
- [ ] Document results and lessons learned.
- [ ] Confirm and document cleanup status.
