# Citizen Clinic Cybersecurity Education Center

## install

```
cd c3ec
python3 -m venv venv
source venv/bin/activate
pip3 install mkdocs mkdocs-material mkdocs-git-revision-date-localized-plugin
```

## update pages

- Make changes to .md files.
- Build the HTML:

```
source venv/bin/activate
python3 -m mkdocs build
git commit -am "update"
git push -uf
```
