
# flaskLog4py

A easy to use flask-driven python thread logger. Not the best of it's market but useful if nothing else is applicable.

## To-Do

- Not having to reload the page to see changes **[HIGH PRIORITY]**  

and other stuff...
## Authors

- [@ParentProfanities](https://github.com/ParentProfanities)


## Usage/Examples

```python
import threading
import flaskLog4py
import time

def thr():
  console_1 = flaskLog4py.newConsole("Thread1")
  time.sleep(5)
  flaskLog4py.addLine(console_1,"Testing", flaskLog4py.LogType.DEBUG)
  flaskLog4py.changeStatus(console_1,"ended","red") 
x = threading.Thread(target=thr)
x.start()
flaskLog4py.startServer(3000)
```
Then, once ran, go on: `localhost:3000`

## Logging types (`flaskLog4py.LogType`)

| Color             | Python Enumeration Reference| Code             |
| ----------------- | ---------- |----------
| Debug | 1 | `flaskLog4py.LogType.DEBUG` |
| Information | 2| `flaskLog4py.LogType.INFORMATION` |
| Error |  3|   `flaskLog4py.LogType.ERROR`|

## Optimisations

If you feel the need to optimise this project, dont be scared to add your own features.
## License

[MIT](https://choosealicense.com/licenses/mit/)

