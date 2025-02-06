# Useful Python codes

## 1. Get current script path
   ```py
   def get_current_script_path():
    if getattr(sys, 'frozen', False):
        return os.path.dirname(sys.executable)
    else:
        return os.path.dirname(os.path.realpath(__file__))
   ```
