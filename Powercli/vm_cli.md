# Comandos CLI VM

>[!IMPORTANT]
>Necessario conectar no vcenter antes de rodas os comandos cmdlets PowerCLI, comando.
```powershell
Connect-VIServer “vCenter Name / IP ”
```

### Listar Propriedades VM
```powershell
Get-VM -Name MyVM*
```

### Listar VMs com status "PoweredOff" (desligadas)
```powershell
Get-VM | where-object {$_.PowerState –eq “PoweredOff”}
```

### Ligar estacão virtual
```powershell
Start-VM -VM VM -Confirm -RunAsync
```

### Desligar estacão virtual
```powershell
Stop-VM -VM VM -Kill -Confirm:$false
```

Link Oficial: <https://developer.vmware.com/docs/powercli/latest/products/vmwarevsphereandvsan/categories/vm/>
