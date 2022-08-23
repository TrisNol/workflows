# Python-Main
This action is intended for repos hosting Python code.

## Requirements
- `requirements.txt` in the calling repo
- [pytest](https://docs.pytest.org/en/7.1.x/) compatible unit tests

- Input parameters:
  - Optional:
    - version (defaults to: '3.10')
    - min_test_coverage (defaults to: '0.6')

## Example
```yaml
      - name: Call composite workflow 
        uses: trisnol/workflows/python-main@main
        with: 
          version: '3.9'
          min_test_coverage: '0.42'
```
