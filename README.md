# Build and Operate Your First AWS CI/CD Pipeline

This standalone repository is for the lab: **Build and Operate Your First AWS CI/CD Pipeline**.

## What this repo contains

- `app.js`, `package.json`: simple Node.js app (single canonical source)
- `buildspec.yml`: CodeBuild instructions
- `appspec.yml` and `scripts/`: CodeDeploy lifecycle configuration
- `infra/target-template.yaml`: EC2 + CodeDeploy + artifact bucket stack
- `infra/pipeline-template.yaml`: CodePipeline + CodeBuild + CodeCommit stack

Note: app and deployment assets are intentionally kept only at repository root to avoid duplication.

## Primary runnable path (lab)

This lab runs with **CodeCommit as source** (stable in sandbox accounts).

High-level flow:
1. Deploy target stack.
2. Deploy pipeline stack.
3. Push/update source in CodeCommit.
4. Pipeline runs Source -> Build -> Deploy.
5. Validate app on EC2 public IP and `/health`.

## Optional learner variant

Learners can replace the pipeline source stage with GitHub via CodeStar Connections if their account permissions allow it.

