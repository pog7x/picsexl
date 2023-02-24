# picsexl

[![PyPI](https://img.shields.io/pypi/v/picsexl)](https://pypi.org/project/picsexl/)
[![License](https://img.shields.io/github/license/pog7x/picsexl)](https://github.com/pog7x/picsexl/blob/master/LICENSE)

## Converter from ics format to xls

### Installation

```bash
pip install picsexl
```

### Example
```python
from datetime import datetime, timezone
from picsexl import PIcsExl

p = PIcsExl(
    file_path="/path/to/your/file.ics",
    mail_to="some.email@gmail.com",
    start_date=datetime(2022, 10, 1, 0, 0, 0, tzinfo=timezone.utc),
    end_date=datetime(2022, 10, 30, 23, 59, 59, tzinfo=timezone.utc),
)
p.run_sniff_and_write_ics_lines()
```