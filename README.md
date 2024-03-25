# GA actions

This is a repository for KeyCore github actions, intended for use with the KeyCore build platform. They can be used in your repo like this example for pull.

~~If used with the KeyCore github_runner setup, remember to add the cleanup_runner action, to stop the runner from spending more time than necessary.~~

```
- name: Cleanup Step 
  if: always() 
  uses: KeyCore/ga_actions/cleanup_runner@master
```

More general use is like:

```
uses: KeyCore/ga_actions/pull@master
  with:
    gh_user: ${{ secrets.GH_USER }}
    gh_token: ${{ secrets.GH_TOKEN }}
    gh_org: KeyCore
    gh_repo: KEDL
```

Currently there are actions for:
- git clone
- git pull
- s3 store
- s3 retrieve
