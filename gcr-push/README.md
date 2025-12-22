# GCR-Push
This action is intended for repos that can be built into Docker images and shall be pushed to the [Google Cloud Artifact Registry](https://docs.cloud.google.com/artifact-registry/docs) for further use.

## Requirements
- `Dockerfile` in the calling repo

- Input parameters:
  - Required:
    - service_account_key
    - region
    - project_id
    - repository
    - image_name
  - Optional:
    - image_version (defaults to: latest)

## Example
```yaml
      - name: Call composite workflow 
        uses: trisnol/workflows/gcr-push@main
        with: 
          service_account_key: ${{ secrets.GCP_SERVICE_ACCOUNT_KEY }}
          region: eu-west1
          project_id: ${{ secrets.GCP_PROJECT_ID }}
          repository: my-docker-registry
          image_name: composite-workflow-test
          image_version: v1.0.0
```
