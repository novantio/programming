create golang module for easy import
```
go mod init <module_name>
```
example module name : laksa.id/be

for import folder api use
```
import (
  "laksa.id/be/api"
)
```

same package same directory auto import
