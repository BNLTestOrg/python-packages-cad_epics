# cad_epics
Wrapper for accessing EPICS devices.
Replacement for cad_io.epicsAccess_caproto

Example in python:
```python
from cad_epics import epics
epics.get(('testAPD:scope1:','MaxValue_RBV'))
{('testAPD:scope1:', 'MaxValue_RBV'): {'value': 1.5416382345661996, 'timestamp': 1681489817.159665, 'alarm': 0}}

def callback(*argv):
  print(argv)

epics.subscribe(callback, ('testAPD:scope1:','MaxValue_RBV'))
({('testAPD:scope1:', 'MaxValue_RBV'): {'value': 1.5044295100280594, 'timestamp': 1681489875.174341, 'alarm': 0}},)
...
epics.unsubscribe()
```

