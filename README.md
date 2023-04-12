# cad_epics
Wrapper for accessing EPICS devices.
Replacement for cad_io.epicsAccess_caproto

Example in python:
```python
from cad_epics import epics
epics.get(('testAPD:scope1','MaxValue_RBV'))
{('testAPD:scope1', 'MaxValue_RBV'): {'value': 1.9757047243599273, 'timestamp': 1681304764.704836, 'alarm': 0}}
```

