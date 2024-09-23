- 💀 Hi, I’m @itsmepopo09
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
itsmepopo09/itsmepopo09 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
name: Security Checks

on: [push, pull_request]

jobs:
  security:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2

    # Run Bandit for Python security analysis
    - name: Run Bandit
      run: |name: Security Check

    steps:
    - uses: actions/checkout@v2

    # Run Bandit for Python security analysis
    - name: Run Bandit
      run: |
        pip install bandit
        bandit -r .

    # Run Dependabot to check for vulnerable dependencies
    - name: Dependabot Alert
      uses: dependabot/fetch-metadata@v1

    # Set up Snyk to scan for vulnerabilities
    - name: Snyk Security Scan
      uses: snyk/actions@master
      env:
        SNYK_TOKEN: ${{ secrets.SNYK_TOK
        pip install bandit
        bandit -r .

    # Run Dependabot to check for vulnerable dependencies
    - name: Dependabot Alert
      uses: dependabot/fetch-metadata@v1

    # Set up Snyk to scan for vulnerabilities
    - name: Snyk Security Scan
      uses: snyk/actions@master
      env:
        SNYK_TOKEN: ${{ secrets.SNYK_TOKEN }}

