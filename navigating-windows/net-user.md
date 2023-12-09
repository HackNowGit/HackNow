# net user

## Overview

* add user accounts

## Add Users to Non-Admin Group

```
net user username /add
```

```
net user username password /add
```

```
net user /add username password
```

## Add User to Administrator Group

```
net localgroup administrators username /add
```

## Check if You are Part of a Domain

```
net localgroup /domain
```

## List all Users in a Domain

```
net users /domain
```
