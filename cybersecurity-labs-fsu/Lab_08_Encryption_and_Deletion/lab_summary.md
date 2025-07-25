# Lab 8 Summary – Encryption and Secure Deletion

**Course**: LIS 5775 – Cybersecurity Fundamentals  
**Student**: Jonah McKitty

---

## 🔐 Part 1: Volume Encryption with VeraCrypt

### Tools Used:
- **VeraCrypt**

### Key Activities:
- Created a new encrypted volume using VeraCrypt.
- Transferred files into the encrypted drive.
- Explored the option to create a hidden volume for plausible deniability.

### Key Takeaways:
- VeraCrypt allows full-volume encryption, including external drives.
- Hidden volumes provide an extra layer of protection by concealing sensitive data within another encrypted volume.
- Keyfiles can be used alongside passwords to enhance authentication security.

---

## 🧹 Part 2: Secure File Deletion with Eraser

### Tool Used:
- **Eraser**

### Key Activities:
- Created a 20MB text file and securely deleted it using Eraser.
- Observed the overwrite process and discussed shredding methods.

### Key Takeaways:
- Eraser uses multi-pass overwriting techniques to prevent file recovery.
- Secure deletion takes longer due to repeated overwrites, but it significantly reduces the chance of data being recovered.
- Right-click integration allows quick shredding of files directly from the context menu.

---

## 🧠 Reflection Questions

- **Why isn’t this built into Windows?**  
  Most users don’t need secure deletion, and third-party tools offer more advanced options.

- **Can you shred any file?**  
  Yes, Eraser allows secure deletion of individual files, folders, or entire drives.

- **Why does it take so long?**  
  Because secure deletion involves multiple overwrite passes to ensure data is unrecoverable.

---

## 🧾 Conclusion

This lab demonstrated the importance of both encrypting sensitive data and securely deleting files to prevent unauthorized access. Tools like VeraCrypt and Eraser provide powerful, user-friendly solutions for protecting data at rest and ensuring it’s unrecoverable when no longer needed.

