## Lab 1: Account & Group Provisioning

### Objective
Configure the system to meet production user management specifications:
1. Create a new group named `opsmanagers`.
2. Create a user named `natasha` who belongs to `opsmanagers` as a secondary (supplementary) group.
3. Create a user named `harry` who belongs to `opsmanagers` as a secondary group, configured with a non-interactive shell.
4. Manually configure passwords for both accounts.

### Implementation Commands

```bash
# 1. Create the system group
groupadd opsmanagers

# 2. Create the user accounts with specified parameters
useradd -G opsmanagers natasha
useradd -G opsmanagers -s /sbin/nologin harry

# 3. Configure user passwords interactively
passwd harry
passwd natasha
```

### Verification
Confirm the attributes match the specifications:
```bash
getent passwd harry natasha
```

