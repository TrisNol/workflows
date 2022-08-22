# Workflows
This repo hosts a collection of reuseable workflows built as [composite actions](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action).

Each action is placed in a separate folder and can be caled as follows:

```yaml
      - name: Call composite workflow 
        uses: trisnol/workflows/<action>@main
```

Replace `<action>` with the folder's name hosting the action (e.g., python-main to call the Python based action). The string behind the `@` specifies the branch or release to reference.


