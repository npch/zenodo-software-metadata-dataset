# Zenodo Software Metadata Dataset

The dataset contains Zenodo metadata records for all software records in Zenodo
from 2017-10-26.

### Creative Commons Zero waiver
To the extent possible under law, CERN has waived all copyright and related or
neighboring rights to Zenodo Software Metadata Dataset.

## Dataset

The file ``data.json`` contains the entire dataset. The file contains a JSON
document per line and can e.g. be loaded in Python by the following short
script:

```python
import json

with open('data.json', 'rb') as fp:
    for line in fp:
        record = json.loads(line)
```

### Records selection criteria
The dataset contains all records of type software in Zenodo including all
versions. More specifically this was the query:

https://zenodo.org/search?all_versions&type=software

- Each record represents a specific version of a software, hence the same
  software package may exists in multiple different records.
- Records that was archived via the Zenodo-GitHub integration has information
  from which GitHub repository they were archived. Note that the repository may
  have been renamed, deleted, changed on GitHub from the time that the software
  was archived in Zenodo.
