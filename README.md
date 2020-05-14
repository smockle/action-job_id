# action-job_id

An action which outputs the identifier of a specified workflow-run’s job.

## Inputs

### `job_index`

**Optional** The index of the job whose identifier will be output. Defaults to the first job. Default: `0`

## Environment Variables

### `GITHUB_TOKEN`

**Optional** A token to authenticate on behalf of the GitHub App installed on your repository. Default: `${{ github.token }}`

### `GITHUB_REPOSITORY`

**Optional** The owner and repository name. For example, `smockle/action-job_id`. Default: `${{ github.repository }}`

### `GITHUB_RUN_ID`

**Optional** A unique number for each run within a repository. This number does not change if you re-run the workflow run. Default: `${{ github.run_id }}`

## Outputs

### `job_id`

The job identifier retrieved by this action

## Example usage

```YAML
- name: Retrieve 'job_id'
  uses: "smockle/action-job_id@master"
  with:
    job_index: 0
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
    GITHUB_REPOSITORY: ${{ github.repository }}
    GITHUB_RUN_ID: ${{ github.run_id }}
```