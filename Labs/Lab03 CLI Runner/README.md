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
````powershell
# InstallDir %Appdata%\npm\node_modules\edgedriver
npm install -g edgedriver
````

---

## env
````powershell
get-command "selen*" |
 fl name,source


Name   : selenium-side-runner.ps1
Source : C:\Users\paul\AppData\Roaming\npm\selenium-side-runner.ps1

Name   : selenium-side-runner.cmd
Source : C:\Users\paul\AppData\Roaming\npm\selenium-side-runner.cmd
````
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
