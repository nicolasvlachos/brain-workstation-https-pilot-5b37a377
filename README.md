# Brain Workstation HTTPS pilot fixture

Synthetic repository for the Brain Workstation approval and integration workflow.

## Pilot verification

Brain Workstation records approval, verification, and integration for this pilot.

To verify local readiness, run `php artisan brain:doctor --workers` from the Brain Workstation application directory. Both the scheduler and the queue worker heartbeats must pass.

The trusted runner independently verifies the candidate and signs the verification evidence. Brain Workstation validates that signature. A human reviews the approved criteria. After the pull request merges in GitHub, Brain Workstation verifies and records both the accepted candidate commit and the merge commit.