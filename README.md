# Tiny Python CI Project

A minimal project for learning CI/CD with GitHub Actions.

## Files

- `app.py` — a couple of trivial functions (`add`, `subtract`)
- `test_app.py` — pytest tests for those functions
- `.github/workflows/ci.yml` — the CI/CD pipeline: runs tests on every push/PR, then a placeholder "deploy" step on `main`

## Run locally

```bash
pip install pytest
pytest
```

## Push to GitHub

```bash
cd tiny-python-ci
git init
git add .
git commit -m "Initial commit: tiny CI project"
git branch -M main
git remote add origin <your-empty-github-repo-url>
git push -u origin main
```

Once pushed, go to the **Actions** tab on GitHub — the workflow should run automatically.

## Try breaking it

Edit `test_app.py` so an assertion is wrong (e.g. `assert add(2, 3) == 99`), push, and watch
the Actions tab go red. Then fix it and push again to watch it go green.
