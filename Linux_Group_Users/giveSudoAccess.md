# Sudo access

>usermod -aG wheel prueba

**-a:** append (not eliminate from other group)

**-G:** GroupId or name 

**wheel:** group with sudo priviledge

Check if wheel has sudo priviledges
>sudo visudo

Access to file sudoers and check following line:
>%wheel ALL=(ALL) ALL
