## Human vs AI Test Coverage

| Test Area                           | Human |  AI |
| ----------------------------------- | :---: | :-: |
| Valid username + valid password     |   ✅   |  ✅  |
| Invalid username + valid password   |   ✅   |  ✅  |
| Valid username + invalid password   |   ✅   |  ✅  |
| Invalid username + invalid password |   ✅   |  ❌  |
| Empty username                      |   ❌   |  ✅  |
| Empty password                      |   ❌   |  ✅  |
| Both fields empty                   |   ❌   |  ✅  |
| Password case sensitivity           |   ❌   |  🔎 |
| Whitespace handling                 |   ❌   |  🔎 |
