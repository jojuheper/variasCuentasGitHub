Como hacer posible trabajar con varias cuentas GitHub sin tener que modificar a cada rato las propiedades del fichero.

# En el Pc
----

* 🇪🇸 Tener instalado Git.  ✔️  
* 🇬🇧 Have Git Installed.  
    ➡️ [Git](https://git-scm.com/)

---------

* 🇪🇸 Abrir Git Bash en la carpeta del Usuario.
* 🇬🇧 Open Git Bash in User folder.

```
#Windows 
C:\Usuario\
C:\Usuario\.ssh

#Linux
~/
~/.ssh
```

* 🇪🇸 Si no esta la carpeta .ssh se crea. ✔️  
* 🇬🇧 If not found .ssh folder, you have create one.
```
mkdir .ssh
```  
--------

* 🇪🇸 Crear una ssh key, para ello una vez situados en la carpeta .ssh del usuario pondremos lo siguiente, recuerda realizar esto por cada cuenta GitHub que tengas.
* 🇬🇧 If we founded or created .ssh folder, we can use the next code, remember make a ssh-key for every single acc in GitHub.
```
#Windows
ssh-keygem.exe

#Linux
~/.ssh-keygen -t rsa -b 4096
```

----

* 🇪🇸 Generara y pregunta algo como esto, observar el ejemplo.
* 🇬🇧 It will generate and ask something like this, 👓 read example.
```
~>ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/home/ylo/.ssh/id_rsa):          (name of file)
Enter passphrase (empty for no passphrase):       Recomendation: putit one (password, if u put it, github ask u forever), can skip this part if u want 
Enter same passphrase again:          put the same password again, if skip before, skip this too
Your identification has been saved in C:/User/.ssh/id_rsa.     (remember name)
Your public key has been saved in C:/User/.ssh/id_rsa.pub.     (remember this one is public for you)
The key fingerprint is:
SHA256:Up6fo75Y8973M393QdQsK3Z0aTNBz0Doijhg+c User@User
The key's randomart image is:
+---[RSA 4096]----+
|    .      ..oo..|
|   . . .  . .o.X.|
|    . . o.  ..+ B|
|   .   o.o  .+ ..|
|    ..o.S   o..  |
|   . %o=      .  |
|    @.B...     . |
|   o.=. o. . .  .|
|    .oo  E. . .. |
+----[SHA256]-----+
```

* 🇪🇸 Se generan dos archivos uno de los cuales es .pub (publico) abrelo y copia su contenido, pegalo en setting/SSH and GPG keys [GitHub](https://docs.github.com/es/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account) desde el punto numero 2.
* 🇬🇧 ssh-keygen make two files, one of both .pub (public), open it and copy the content in setting/SSH and GPG keys [GitHub](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account) from point number 2.

* 🇪🇸 Creamos un archivo llamado *config* en la carpeta .ssh y agregaremos lo siguiente.
* 🇬🇧 Make a file *config* in the same folder .ssh and add.
```
# Github1
Host github.com
HostName github.com
User (your first user)
IdentityFile ~/.ssh/id_rsa_github    (your name file for first acc)

# Github2
Host github.com
HostName github.com
User (your second user)
IdentityFile ~/.ssh/id_rsa_github     (your name file for second acc)
```
-----

* 🇪🇸 Ahora puedes ir a tu repositorio GitHub y realiar la clonacion desde el formato SSH 👁️.
* 🇬🇧 Visit your reposiroty and now you can clone using ssh format ⚠️.
```
git clone git@github.com:jojuheper/variasCuentasGitHub.git

git console ask for your passphrase in order to config file, only put passphrase where you need to clone, pay attention for this.
```

* 🇪🇸 Ahora puedes usar los comandos de GitHub y se te iran activando las contraseñas del config en orden de creacion.
* 🇬🇧 Now you can use the basic command for GitHub and remember, the GitHub ask your password in the same order from config file.

**Enjoy!**  
**Thank for watch**
