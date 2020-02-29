# Clean

## Removing control characters
For reference, see [here].

```python
import unicodedata as unicode
def remove_control_characters(string):
    # Create list without control characters
    characters = (char for char in string if unicode.category(char)[0] != 'C')
    
    # Join back together & return result
    return ''.join(characters)
```
