---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 62349410e3858978166fd9c5356a8c6b568b9600
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181614"
---
# New-AzVMConfig

## SYNOPSIS
Crea un oggetto macchina virtuale configurabile.

## SINTASSI

### DefaultParameterSet (Default)
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzVMConfig crea** un oggetto macchina virtuale locale configurabile per Azure.
Altri cmdlet possono essere usati per configurare un oggetto macchina virtuale, ad esempio Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface e Set-AzVMOSDisk.

## ESEMPI

### Esempio 1: Creare un oggetto macchina virtuale
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

Il primo comando ottiene il set di disponibilità denominato AvailabilitySet03 nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $AvailabilitySet locale.
Il secondo comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.
Il comando assegna un nome e le dimensioni alla macchina virtuale.
La macchina virtuale appartiene al set di disponibilità archiviato in $AvailabilitySet.

## PARAMETERS

### -AvailabilitySetId
Specifica l'ID di un set di disponibilità.
Per ottenere un oggetto set di disponibilità, usare il cmdlet Get-AzAvailabilitySet disponibilità.
L'oggetto set di disponibilità contiene una proprietà ID. <br>
Le macchine virtuali specificate nello stesso set di disponibilità sono allocate a nodi diversi per massimizzare la disponibilità. <br>
Per altre informazioni sui set di disponibilità, vedere [Gestire la disponibilità delle macchine virtuali.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
Per altre informazioni sulla manutenzione pianificata di Azure, vedere [Manutenzione pianificata per le macchine virtuali in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json) <br>
Attualmente, una macchina virtuale può essere aggiunta solo al set di disponibilità al momento della creazione. Il set di disponibilità a cui viene aggiunta la macchina virtuale deve essere nello stesso gruppo di risorse della risorsa del set di disponibilità. Non è possibile aggiungere una macchina virtuale esistente a un set di disponibilità. <br>
Questa proprietà non può esistere insieme a una proprietà non Null. Riferimento VirtualMachineScaleSet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUltrasSD
Consente di avere uno o più dischi dati gestiti con un UltraSSD_LRS di account di archiviazione nella macchina virtuale.
I dischi gestiti con tipo di account di UltraSSD_LRS possono essere aggiunti a una macchina virtuale solo se questa proprietà è abilitata.


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EvictionPolicy
Criteri di sgombero per la macchina virtuale Azure Spot.  I valori supportati sono "Deassegnazione" ed "Elimina".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HostId
ID dell'host

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityId
Specifica l'elenco delle identità utente associate al set di scalabilità delle macchine virtuali.
I riferimenti di identità utente ARM id risorsa nel formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityType
L'identità della macchina virtuale, se configurata.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Specifica un tipo di licenza, che indica che l'immagine o il disco della macchina virtuale è stato concesso in licenza in locale.
I valori possibili per Windows Server sono:
- Windows_Client
- Windows_Server I valori possibili per il sistema operativo Linux Server sono: 
- RHEL_BYOS (per ESTRAI) 
- SLES_BYOS (per SUSE) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
Specifica il prezzo massimo che si è disposti a pagare per una VM/VMSS con priorità bassa. Questo prezzo è in dollari statunitensi. Questo prezzo verrà confrontato con l'attuale prezzo con priorità bassa per le dimensioni della macchina virtuale. Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento di VM/VMSS con priorità bassa e l'operazione avrà esito positivo solo se il valore maxPrice è maggiore del prezzo attuale con priorità bassa. Il valore maxPrice verrà usato anche per eliminare una VM/VMSS con priorità bassa se il prezzo attuale con priorità bassa supera il valore maxPrice dopo la creazione di VM/VMSS. I valori possibili sono: qualsiasi valore decimale maggiore di zero. Esempio: 0,01538.  -1 indica che la VM/VMSS con priorità bassa non deve essere sfrattata per motivi di prezzo. Inoltre, il prezzo massimo predefinito è -1 se non è fornito dall'utente.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EncryptionAtHost
La proprietà EncryptionAtHost può essere usata dall'utente nella richiesta per abilitare o disabilitare La crittografia host per il set di scalabilità della macchina virtuale o della macchina virtuale. In questo modo verrà abilitata la crittografia per tutti i dischi, incluso il disco Risorsa/Temp nell'host stesso. Impostazione predefinita: la crittografia nell'host verrà disabilitata a meno che questa proprietà non sia impostata su true per la risorsa.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Priorità della macchina virtuale.  Solo i valori supportati sono "Normale", "Posizione" e "Basso".
"Normale" è per la macchina virtuale normale.
"Spot" è per una macchina virtuale spot.
"Low" è anche per la macchina virtuale spot, ma viene sostituito da "Spot". Usare "Spot" invece di "Low".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
ID risorsa del gruppo di posizionamento di prossimità da usare con la macchina virtuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
I tag associati alla risorsa.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Specifica un nome per la macchina virtuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
Specifica le dimensioni della macchina virtuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmssId
ID del set di scala per le macchine virtuali

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Specifica l'elenco delle aree di disponibilità per la macchina virtuale. I valori consentiti dipendono dalle funzionalità dell'area geografica. I valori consentiti saranno in genere 1,2,3.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### System.String[]

### System.Collections.Hashtable

### System.Management.Automation.SwitchParameter

## OUTPUT

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTE

## COLLEGAMENTI CORRELATI

[Update-AZVM](./Update-AzVM.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[Set-AzVMSourceImage](./Set-AzVMSourceImage.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)


