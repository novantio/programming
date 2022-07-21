# active directory
#path ldap
```
string path = @"LDAP://laksa.id/DC=LAKSA,DC=ID";
string domainAndUsername = domainz + @"\" + username;
string pwd="yourpasswordhere";
DirectoryEntry entry = new DirectoryEntry(paths, domainAndUsername, pwd);

```
