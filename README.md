## 🔐 Using `netplwiz` in Windows — User Account Control Utility

### 📌 What is `netplwiz`?

`netplwiz` is a built-in Windows utility that provides a graphical interface to manage **user accounts** on a local machine. It's a shortcut to the **"User Accounts"** control panel.

### 🧭 How to Open It

1. Press `Win + R` to open the **Run** dialog.
2. Type `netplwiz` and press `Enter`.

This opens the **User Accounts** window.

### 🔍 What Can You Do With It?

Once the `netplwiz` utility is open, you can:

* View all **local user accounts**
* Add or remove **users**
* Change a user's **group membership** (e.g., Administrator, Standard User)
* Reset passwords for local users
* **Enable or disable automatic login**

---

### ⚠️ Automatic Login (Security Note)

One commonly used feature in `netplwiz` is the ability to disable the password prompt during login:

* Uncheck the box labeled **"Users must enter a user name and password to use this computer."**
* When you click **Apply**, you will be prompted to enter the username and password.
* After that, Windows will automatically log in with that account.

> ⚠️ **Security Risk**: Enabling automatic login bypasses password protection at startup, which can be a risk on shared or portable devices.

---

### 📂 Use Cases

| Use Case                               | Benefit                         |
| -------------------------------------- | ------------------------------- |
| Managing user accounts                 | No need for `cmd` or PowerShell |
| Enabling auto-login for kiosks or labs | Faster startup                  |
| Resetting local passwords              | Quick access for admin          |

---

### 💻 Behind the Scenes

`netplwiz` is essentially a shortcut for:

```cmd
control userpasswords2
```

Both commands open the same legacy user account manager, which is still available in Windows 10 and 11.

---

### ✅ Summary

* `netplwiz` is a useful tool for local account management.
* It is especially useful for configuring automatic login or troubleshooting user permission issues.
* Use with caution — especially in production or security-sensitive environments.

---

