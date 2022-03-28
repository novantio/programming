## content
- [init](#init)
- [rules](#rules)
- [post](#post)

## init

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

## rules
- name function first letter capital public var, small private var
- post can read if Capital

## post
for sample login
# create struct
```
type LOGIN struct {
	U string `json:"u"`
	P string `json:"p"`
}
```
then bind input in login
```
var login LOGIN
err := c.Bind(&login)
```
