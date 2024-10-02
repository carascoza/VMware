# Comandos vmware-vdiskmanager.exe

Criar disco manualmente
```powershell
vmware-vdiskmanager.exe -c -s 10GB -a lsilogic -t 0 "<caminho>\<arquivo></arquivo>.vmdk"
```

Comandos exemplos:
```powershell
vmware-vdiskmanager.exe -c -s 850MB -a ide -t 0 myIdeDisk.vmdk
vmware-vdiskmanager.exe -d myDisk.vmdk
vmware-vdiskmanager.exe -r sourceDisk.vmdk -t 0 destinationDisk.vmdk
vmware-vdiskmanager.exe -x 36GB myDisk.vmdk
vmware-vdiskmanager.exe -n sourceName.vmdk destinationName.vmdk
vmware-vdiskmanager.exe -k myDisk.vmdk
vmware-vdiskmanager.exe -p <mount-point>
```