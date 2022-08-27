# GCR-Push
This action is intended for repos that can be built into Docker images and shall be pushed to the [Google Container Registry (GCR for short)](https://cloud.google.com/container-registry) for further use.

## Requirements
- `Dockerfile` in the calling repo

- Input parameters:
  - Required:
    - service_account_key
    - project_id
    - image_name
  - Optional:
    - image_version (defaults to: latest)

## Example
```yaml
      - name: Call composite workflow 
        uses: trisnol/workflows/gcr-push@main
        with: 
          service_account_key: ${{ secrets.GCP_SERVICE_ACCOUNT_KEY }}
          project_id: ${{ secrets.GCP_PROJECT_ID }}
          image_name: composite-workflow-test
          image_version: v1.0.0
```
