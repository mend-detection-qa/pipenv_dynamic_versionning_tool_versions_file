# Pipenv Test Case 2: .tool-versions File Detection

## What This Tests
Tests that `.tool-versions` (asdf) file is the second priority source for Python version detection in Pipenv projects.

## Expected
3.10.5 found through AsdfVersionFile

## Files
- `.tool-versions` - Contains `python 3.10.5`
- `Pipfile` - Contains conflicting version `3.9` in requires section

## Expected Behavior
Your version detection tool should detect **Python 3.10.5** from `.tool-versions`.

## Priority
This is the **second priority** detection method for Pipenv projects (after .python-version).

## Note
The .tool-versions file takes precedence over Pipfile when no .python-version file is present.
