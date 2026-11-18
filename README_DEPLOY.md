# IGGL E&I TOOLS v2.3 – deployment fix

## Dependency fix
This package pins Streamlit to 1.41.1 and Python to 3.11 to avoid uncontrolled upgrades during deployment. The app uses only Streamlit and Python standard-library modules.

## Deploy / update an existing Streamlit Community Cloud app
1. Extract this ZIP.
2. Replace the files in your GitHub repository with the files from this package.
3. Ensure `app.py`, `requirements.txt`, and `runtime.txt` are in the repository root (same folder).
4. Commit and push the changes.
5. In Streamlit Community Cloud, open the app menu and choose **Reboot app**. If dependency installation remains cached, use **Manage app → Reboot** after the new commit, or delete and redeploy the app.
6. If it still fails, open **Manage app → Logs**, scroll to the first `ERROR:` / `Could not find a version` / `ResolutionImpossible` line, and share that section.

## Local run
```bash
python -m venv .venv
# Windows
.venv\\Scripts\\activate
pip install -r requirements.txt
streamlit run app.py
```

## App content
- Home
- Instrumentation
- Electrical
- Telecom
- Audit Trail

Gas Engineering is removed. Audit Trail remains session-based and can be exported as CSV.
