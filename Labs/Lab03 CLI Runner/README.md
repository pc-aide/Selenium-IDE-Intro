# Lab03 CLI Runner

---

## doc
* https://www.selenium.dev/selenium-ide/docs/en/introduction/command-line-runner

---

## Prerequisites
1. nodeJS
2. npm install -g selenium-side-runner

---

## Browser

### Edge
* npm install -g edgedriver

---

## env
````powershell
[Environment]::SetEnvironmentVariable(
  "PATH",
  "$env:PATH;$env:APPDATA\npm",
  [EnvironmentVariableTarget]::User
)
````

---

## Test
`selenium-side-runner /path/to/your-project.side`
