# 🧑‍💻 User Account Management Commands
This guide provides basic commands for managing user accounts on Linux.

## 🔒 Lock User Account
To lock a user account, preventing the user from logging in:

```bash
passwd -l USER-NAME
```
- `USER-NAME:` The username of the account to lock.


## 🔓 Unlock User Account
To unlock a previously locked user account:
```bash
passwd -u USER-NAME
```
- `USER-NAME`: The username of the account to unlock.

❌ Remove User Password
To remove a password from a user account (the user will be able to log in without a password):
```bash
passwd -d USER-NAME
```
- `USER-NAME`: The username of the account to remove the password.

## 📅 Set User Account Expiration Date
To set an expiration date for a user account (after this date, the user will no longer be able to log in):
```bash
chage -E YYYY-MM-DD USER-NAME
```
- `YYYY-MM-DD`: The expiration date in the format Year-Month-Day.
- `USER-NAME`: The username of the account for which you want to set the expiration date.

### Example:
To set the expiration date of the user jobs to 2025-01-01:
```bash
chage -E 2025-01-01 jobs
```
