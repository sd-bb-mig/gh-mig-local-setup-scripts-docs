# Revert the executed migrations from github

```python

import webbrowser

ghe_repos = []

firefox_url = "C:\\Program Files\\Mozilla Firefox\\firefox.exe"
# Register the browser
webbrowser.register('firefox', None, webbrowser.BackgroundBrowser(firefox_url))
#
# for ghe_repo in ghe_repos:
#     url = (f"https://{GHORG_URL}/{ghe_repo}/settings")
#     webbrowser.get('firefox').open_new_tab(url)

# for ghe_repo in ghe_repos:
#     repo = ghe_repo.replace('XOPS-', '')
#     url = f'https://{BBURL}/plugins/servlet/branch-permissions/XOPS/{repo}'
#     webbrowser.get('firefox').open_new_tab(url)


# print(f"delete from git_repo_data where name in ('{"','".join(ghe_repos)}');")

# for ghe_repo in ghe_repos:
#     repo = ghe_repo.replace('XOPS-', '')
#     print(f"update repositories set migrated=0, updated_on = null where name='{repo}' and migrated > 0;")

#
# bb_repos = []
# for ghe_repo in ghe_repos:
#     repo = ghe_repo.replace('XOPS-', '')
#     bb_repos.append(repo)
#
# print(f"select * from repositories where name in ('{"','".join(bb_repos)}')")

```
