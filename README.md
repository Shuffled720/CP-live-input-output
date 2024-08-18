This setup is for windows device(latest working on windows 11 18/08/2023)


1)select default profile as cmd
2)select default compiler as g++(if not alterned in past then leave this step)
3)click on terminal -> configure task -> add task.json
4)the code there with below code:
5)save every thing and make input nd output.txt and open in multi window view
6)put cursor on cpp editor and enter on keyboard ctrl+shift+b
7)as per inputs in input.txt outputs will be given in output.txt

THANKSSSSSSSSSS!!!
{
    "version": "2.0.0",
    "tasks": [
      {
        "label": "Compile and run",
        "type": "shell",
        "command": "",
        "args": [
          "copy",
          "\"${file}\"",
          "${workspaceFolder}\\jspwTest.cpp",
          "&&",
          "g++",
          "jspwTest.cpp",
          "-o",
          "jspwTest",
          "&&",
          "jspwTest",
          "<",
          "input.txt",
          ">",
          "output.txt",
          "&&",
          "del",
          "jspwTest.exe",
          "&&",
          "del",
          "jspwTest.cpp"
        ],
        "presentation": {
          "reveal": "silent"
        },
        "group": {
          "kind": "build",
          "isDefault": true
        },
        "problemMatcher": {
          "owner": "cpp",
          "fileLocation": [
            "relative",
            "${workspaceRoot}"
          ],
          "pattern": {
            "regexp": "^(.*):(\\d+):(\\d+):\\s+(warning|error):\\s+(.*)$",
            "file": 1,
            "line": 2,
            "column": 3,
            "severity": 4,
            "message": 5
          }
        }
      }
    ]
  }
