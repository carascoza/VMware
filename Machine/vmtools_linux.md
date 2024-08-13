# Install via SSH Linux

Monte imagem vmtoosl
```powershell
sudo mkdir /mnt/cdrom
```

listar diretorio
```powershell
ls /mnt/cdrom
```

Extrair arquivo vmtools
```powershell
tar xzvf /mnt/cdrom/VMwareTools-xxx.tar.gz -C /tmp/
```

listar pasta do instalador extraido
```powershell
cd /tmp/vmware-tools-distrib/
```

```powershell
sudo ./vmware-install.pl -f
```
Instalar o pacote do vmtools
```powershell
sudo apt install open-vm-tools-desktop
```
