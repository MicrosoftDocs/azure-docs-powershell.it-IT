---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: aaf1162cdeeb007a680a3e9de325cbd10fadef94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863898"
---
# Add-AzVMNetworkInterface

## Sinossi
Aggiunge un'interfaccia di rete a una macchina virtuale.

## SINTASSI

### GetNicFromNicId (impostazione predefinita)
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetNicFromNicObject
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzVMNetworkInterface** aggiunge un'interfaccia di rete a una macchina virtuale.
È possibile aggiungere un'interfaccia quando si crea una macchina virtuale o si aggiunge una a una macchina virtuale esistente.

## ESEMPI

### Esempio 1: aggiungere un'interfaccia di rete a una nuova macchina virtuale
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.
Il comando assegna un nome e una dimensione alla macchina virtuale.

Il secondo comando aggiunge un'interfaccia di rete alla macchina virtuale archiviata in $VirtualMachine.

### Esempio 2: aggiungere un'interfaccia di rete a una macchina virtuale esistente
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 usando il cmdlet **Get-AzVM** .
Il comando Archivia la macchina virtuale nella variabile $VirtualMachine.

Il secondo comando aggiunge un'interfaccia di rete alla macchina virtuale archiviata in $VirtualMachine.

Il comando finale aggiorna lo stato della macchina virtuale archiviata in $VirtualMachine in ResourceGroup11.

## PARAMETRI

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Specifica l'ID di un'interfaccia di rete da aggiungere a una macchina virtuale.
Puoi usare il cmdlet [Get-AzNetworkInterface](/powershell/module/azurerm.network/get-aznetworkinterface) per ottenere un'interfaccia di rete.

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkInterface
Specifica l'interfaccia di rete.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Primaria
Indica che questo cmdlet aggiunge l'interfaccia di rete come interfaccia principale.

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Specifica un oggetto macchina virtuale locale a cui aggiungere un'interfaccia di rete.
Per creare una macchina virtuale, usare il cmdlet **New-AzVMConfig** .
Per ottenere una macchina virtuale esistente, usare il cmdlet **Get-AzVM** .

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkInterface]
Il parametro ' NetworkInterface ' accetta il valore di tipo ' System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Network. Models. PSNetworkInterface]' dalla pipeline

### PSVirtualMachine
Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

## Note

## COLLEGAMENTI CORRELATI

[New-AzVMConfig](./New-AzVMConfig.md)

[Get-AzVM](./Get-AzVM.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)
