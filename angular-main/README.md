# Angular-Main

This action is a simple wrapper for Angular related CI actions

## Requirements
- `package.json` in the calling repo
- `Dockerfile` in the calling repo

- Input parameters:
  - Optional:
    - node_version (defaults to: 16)
    - path (defaults to: ./) Path to the Angular project (important for monorepos)

## Example
```yaml
      - name: Call composite workflow 
        uses: trisnol/workflows/angular-main@main
        with: 
          node_version: 16
          path: ./frontend
```

