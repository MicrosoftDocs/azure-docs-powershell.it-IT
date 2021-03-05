---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: fbdefd7e80e0054bbef8e12614316f7b23ff134a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015390"
---
# Update-AzVmss

## SYNOPSIS
Aggiorna lo stato di un sistema VMSS.

## SINTASSI

### DefaultParameter (Default)
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-ImageReferenceId <String>] [-ImageReferenceOffer <String>]
 [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>]
 [-ImageUri <String>] [-LicenseType <String>] [-ManagedDiskStorageAccountType <String>]
 [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>] [-MaxUnhealthyInstancePercent <Int32>]
 [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-OsDiskCaching <CachingTypes>]
 [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>] [-PauseTimeBetweenBatches <String>]
 [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>] [-PlanPublisher <String>]
 [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>] [-ScaleInPolicy <String[]>]
 [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>] [-SkuCapacity <Int32>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-AutomaticRepairGracePeriod <String>] [-BootDiagnosticsEnabled <Boolean>]
 [-BootDiagnosticsStorageUri <String>] [-CustomData <String>] [-DisableAutoRollback <Boolean>]
 [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticRepair <Boolean>]
 [-EnableAutomaticUpdate <Boolean>] [-IdentityId <String[]>] -IdentityType <ResourceIdentityType>
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-ProximityPlacementGroupId <String>]
 [-ScaleInPolicy <String[]>] [-SinglePlacementGroup <Boolean>] [-SkipExtensionsOnOverprovisionedVMs <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Update-AzVmss** aggiorna lo stato di un set di scalabilità macchina virtuale (VMSS) allo stato di un oggetto VMSS locale.

## ESEMPI

### Esempio 1: Aggiornare lo stato di un vms allo stato di un oggetto VMSS locale.
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

Questo comando aggiorna lo stato del sistema VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001 allo stato di un oggetto VMSS locale, $LocalVMSS.

## PARAMETERS

### -AsJob
Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomaticOSUpgrade
Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente a istanze di set di scala in modalità di distribuzione quando diventa disponibile una versione più recente dell'immagine.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutomaticRepairGracePeriod
La quantità di tempo per cui le riparazioni automatiche vengono sospese a causa di una modifica di stato nella macchina virtuale. Il tempo di tolleranza inizia dopo il completamento della modifica dello stato. In questo modo si evitano riparazioni accidentali o accidentali. La durata dell'ora deve essere specificata nel formato ISO 8601. Il periodo di tolleranza minimo consentito è 30 minuti (PT30M), che è anche il valore predefinito. Il periodo di tolleranza massimo consentito è 90 minuti (PT90M).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsEnabled
Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootDiagnosticsStorageUri
URI dell'account di archiviazione da usare per l'inserimento dell'output della console e dello screenshot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomData
Specifica una stringa di dati personalizzati codificata in base 64.
Questa decodifica viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.
La lunghezza massima della matrice binaria è 65535 byte. <br>
Per l'uso di cloud-init per la macchina virtuale, vedi Uso [di cloud-init](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)per personalizzare una macchina virtuale Linux durante la creazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -DisableAutoRollback
Disabilitare il rollback automatico per i criteri di aggiornamento automatico del sistema operativo

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Indica che questo cmdlet disabilita l'autenticazione tramite password per il sistema operativo Linux.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticRepair
Abilitare o disabilitare le riparazioni automatiche nel set di scalabilità della macchina virtuale.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutomaticUpdate
Indica se le macchine virtuali Di Windows nel sistema operativo VMS sono abilitate per gli aggiornamenti automatici.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
Questo parametro può essere usato dall'utente nella richiesta per abilitare o disabilitare La crittografia host per il set di scalabilità della macchina virtuale. 

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentityType
Specifica il tipo di identità usato per il set di scalabilità delle macchine virtuali.
Il tipo 'SystemAssignedUserAssigned' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.
Il tipo "Nessuna" rimuove le identità dal set di scalabilità delle macchine virtuali.
I valori accettabili per questo parametro sono:
- SystemAssigned
- UserAssigned
- SystemAssignedUserAssigned
- Nessuno

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceId
Specifica l'ID di riferimento dell'immagine.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceOffer
Specifica il tipo di offerta dell'immagine della macchina virtuale (VMImage).
Per ottenere un'offerta per l'immagine, usare Get-AzVMImageOffer cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferencePublisher
Specifica il nome di un autore di un'immagine VMImage.
Per ottenere un autore, usare il cmdlet Get-AzVMImagePublisher pubblicazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceSku
Specifica lo SKU VMImage.
Per ottenere SKU, usare il cmdlet Get-AzVMImageSku.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageReferenceVersion
Specifica la versione di VMImage.
Per usare la versione più recente, specificare un valore relativo alla versione più recente anziché a una specifica versione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageUri
Specifica l'URI BLOB per l'immagine dell'utente.
VMSS crea un disco del sistema operativo nello stesso contenitore dell'immagine utente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Specificare il tipo di licenza, che consente di portare lo scenario di licenza.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedDiskStorageAccountType
Specifica il tipo di account di archiviazione per il disco gestito.
I valori accettabili per questo parametro sono:
- StandardLRS
- PremiumLRS

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxBatchInstancePercent
La percentuale massima del totale di istanze di macchine virtuali che verranno aggiornate contemporaneamente dall'aggiornamento in un unico batch.
Poiché si tratta di un numero massimo di istanze non integre nei batch precedenti o futuri, la percentuale di istanze in un batch può ridursi per garantire un'affidabilità maggiore.
Se il valore non viene specificato, viene impostato su 20.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
Specifica il prezzo massimo che si è disposti a pagare per una VM/VMSS con priorità bassa. Questo prezzo è in dollari statunitensi. Questo prezzo verrà confrontato con l'attuale prezzo con priorità bassa per le dimensioni della macchina virtuale. Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento di VM/VMSS con priorità bassa e l'operazione avrà esito positivo solo se il valore maxPrice è maggiore del prezzo attuale con priorità bassa. MaxPrice verrà usato anche per eliminare una VM/VMSS con priorità bassa se il prezzo attuale con priorità bassa supera il valore maxPrice dopo la creazione di VM/VMSS. I valori possibili sono: qualsiasi valore decimale maggiore di zero. Esempio: 0,01538.  -1 indica che la VM/VMSS con priorità bassa non deve essere sfrattata per motivi di prezzo. Inoltre, il prezzo massimo predefinito è -1 se non viene fornito dall'utente.

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxUnhealthyInstancePercent
Percentuale massima delle istanze di macchine virtuali totali nel set di scalabilità che possono essere simultaneamente non integre, come risultato dell'aggiornamento o trovate in uno stato non integro dai controlli di integrità della macchina virtuale prima dell'interruzione dell'aggiornamento del rolling.
Questo vincolo verrà verificato prima di avviare qualsiasi batch.
Se il valore non viene specificato, viene impostato su 20.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxUnhealthyUpgradedInstancePercent
Percentuale massima di istanze di macchine virtuali aggiornate che possono essere trovate in uno stato non integro.
Questo controllo verrà eseguito dopo l'aggiornamento di ogni batch.
Se questa percentuale viene superata, l'aggiornamento verrà interrotto.
Se il valore non viene specificato, viene impostato su 20.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsDiskCaching
Specifica la modalità di memorizzazione nella cache del disco del sistema operativo. I valori accettabili per questo parametro sono:
- Nessuno
- ReadOnly
- ReadWrite Il valore predefinito è ReadWrite.
Se si modifica il valore della cache, il cmdlet riavvierà la macchina virtuale.
Questa impostazione influisce sulla coerenza e sulle prestazioni del disco.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OsDiskWriteAccelerator
Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overprovision
Indica se il cmdlet ha eseguito l'overprovisioning di VMSS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PauseTimeBetweenBatches
Il tempo di attesa tra il completamento dell'aggiornamento per tutte le macchine virtuali in un unico batch e l'avvio del batch successivo.
La durata dell'ora deve essere specificata nel formato ISO 8601.
Il valore predefinito è 0 secondi (PT0S).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanName
Specifica il nome del piano.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanProduct
Specifica il prodotto del piano.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanPromotionCode
Specifica il codice promozionale del piano.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlanPublisher
Specifica l'autore del piano.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProvisionVMAgent
Indica se è necessario eseguire il provisioning dell'agente della macchina virtuale nelle macchine virtuali Windows nel sistema VMSS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
ID risorsa del gruppo di posizionamento di prossimità da usare con questo set di scale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse a cui appartiene VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScaleInPolicy
Regole da seguire quando si ridimensiona un set di scalabilità delle macchine virtuali.  I valori possibili sono " Default", "OldestVM" e "NewestVM".  "Impostazione predefinita" quando un set di scalabilità delle macchine virtuali viene ridimensionato, il set di scala verrà prima bilanciato tra le aree, se si tratta di un set di scala di zona.  Quindi, sarà bilanciato il più possibile tra i domini di errore.  All'interno di ogni dominio di errore, le macchine virtuali scelte per la rimozione saranno le più recenti non protette dalla scalabilità.  Nel caso di un set di scale per macchine virtuali in fase di ridimensionamento, per la rimozione vengono scelte le macchine virtuali meno recenti non protette dal scale-in.  Per i set di scala delle macchine virtuali zonali, il set di scala verrà prima bilanciato tra più aree.  All'interno di ogni area vengono scelte le macchine virtuali meno recenti non protette per la rimozione.  Nel caso di un set di scale per macchine virtuali in fase di ridimensionamento, per la rimozione verranno scelte le macchine virtuali più recenti non protette dal scale-in.  Per i set di scala delle macchine virtuali zonali, il set di scala verrà prima bilanciato tra più aree.  All'interno di ogni area vengono scelte le macchine virtuali più recenti non protette per la rimozione.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Specifica il singolo gruppo di posizionamento.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipExtensionsOnOverprovisionedVMs
Specifica che le estensioni non vengono eseguite nelle macchine virtuali con overprovisioning aggiuntivo.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuCapacity
Specifica il numero di istanze nel sistema VMSS.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKUName
Specifica le dimensioni di tutte le istanze di VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkuTier
Specifica il livello di VMSS.
I valori accettabili per questo parametro sono:
- Standard
- Di base

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Coppie chiave-valore sotto forma di tabella hash. Ad esempio: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TerminateScheduledEventNotBeforeTimeoutInMinutes
Il periodo di tempo configurabile (in minuti) per l'eliminazione di una macchina virtuale dovrà approvare potenzialmente l'evento terminate pianificato prima che l'evento venga approvato automaticamente (timeout).

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TerminateScheduledEvents
Specifica se l'evento Terminate Scheduled è abilitato o disabilitato.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Specifica il fuso orario per Windows OS. ad esempio Ora \" solare \" Pacifico. <br>
I valori possibili possono essere [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) da fusi orari restituiti da [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UltrassdEnabled
Il contrassegno che abilita o disabilita una funzionalità che consente di avere uno o più dischi di dati gestiti con un UltraSSD_LRS di account di archiviazione nel set di scalabilità della macchina virtuale.
I dischi gestiti con tipo di account di UltraSSD_LRS possono essere aggiunti a un sistema VMSS solo se questa proprietà è abilitata.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UpgradePolicyMode
È stata specificata la modalità di un aggiornamento alle macchine virtuali nel set di scala.
I valori accettabili per questo parametro sono:
- Automatico
- Manuale
- Rotolamento

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdContainer
Specifica gli URL del contenitore usati per archiviare i dischi del sistema operativo per VMSS.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Specifica un oggetto VMSS locale.
Per ottenere un oggetto VMSS, usare il cmdlet Get-AzVmss VMSS.
Questo oggetto macchina virtuale contiene lo stato aggiornato per VMSS.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
Specifica il nome del sistema VMS creato da questo cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Boolean

## OUTPUT

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzVmss](./Get-AzVmss.md)

[New-AzVmss](./New-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[Restart-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)


