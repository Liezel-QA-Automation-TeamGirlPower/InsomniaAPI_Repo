## Importing Insomnia API Tests

### 1. Export Your Insomnia Workspace

- Open Insomnia
- Click the Workspace dropdown → Import/Export → Export Data
- Choose "Current Workspace" (or "All Data")
- Export as JSON and save the file

### 2. Add Export to This Repo

1. Create a folder named `insomnia` in the repo root (if it doesn't exist)
2. Place your exported JSON file in that folder, e.g. `insomnia/insomnia_workspace.json`

### 3. Commit and Push

```powershell
mkdir insomnia
Move-Item "C:\path\to\your\export.json" .\insomnia\insomnia_workspace.json
git add insomnia/insomnia_workspace.json
git commit -m "Add Insomnia workspace export"
git push
```

### 4. (Optional) Run API Tests via CLI

Install the Insomnia CLI:
```powershell
npm install -g insomnia-inso
```
Run tests:
```powershell
inso run --workspace insomnia/insomnia_workspace.json
```

### 5. (Optional) Add CI/CD

You can add a script or GitHub Actions workflow to run API tests automatically on push. Ask for help if you want this set up!

mkdir insomnia
Move-Item "C:\path\to\your\export.json" .\insomnia\insomnia_workspace.json
git add insomnia/insomnia_workspace.json
git commit -m "Add Insomnia workspace export"
git push

# Run tests locally (optional): 
install the CLI: npm install -g insomnia-inso. 
Inspect CLI help with inso --help. 
A common pattern is inso run (see inso run --help) pointing to your workspace file, e.g.: inso run --workspace insomnia/insomnia_workspace.json

# API Documentation
https://github.com/vdespa/quick-introduction-to-postman/blob/main/simple-tool-rental-api.md 
