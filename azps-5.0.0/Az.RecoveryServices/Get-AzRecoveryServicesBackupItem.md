---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301237"
---
# <span data-ttu-id="9e94b-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9e94b-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="9e94b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e94b-102">SYNOPSIS</span></span>

<span data-ttu-id="9e94b-103">Ottiene gli elementi da un contenitore nel backup.</span><span class="sxs-lookup"><span data-stu-id="9e94b-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="9e94b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e94b-104">SYNTAX</span></span>

### <span data-ttu-id="9e94b-105">GetItemsForContainer (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e94b-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e94b-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="9e94b-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e94b-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="9e94b-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e94b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e94b-108">DESCRIPTION</span></span>

<span data-ttu-id="9e94b-109">Il cmdlet **Get-AzRecoveryServicesBackupItem** Ottiene l'elenco degli elementi protetti in un contenitore e lo stato di protezione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="9e94b-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="9e94b-110">Un contenitore registrato in un Vault di servizi di ripristino di Azure può avere uno o più elementi che possono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="9e94b-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="9e94b-111">Per le macchine virtuali di Azure può essere presente un solo elemento di backup nel contenitore della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e94b-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="9e94b-112">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="9e94b-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="9e94b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e94b-113">EXAMPLES</span></span>

### <span data-ttu-id="9e94b-114">Esempio 1: ottenere un elemento da un contenitore di backup</span><span class="sxs-lookup"><span data-stu-id="9e94b-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="9e94b-115">Il primo comando ottiene il contenitore di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="9e94b-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="9e94b-116">Il secondo comando ottiene l'elemento di backup denominato V2VM in $Container e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="9e94b-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="9e94b-117">Esempio 2: ottenere un elemento di condivisione file di Azure da FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9e94b-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="9e94b-118">Il primo comando ottiene il contenitore di tipo AzureStorage e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="9e94b-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="9e94b-119">Il secondo comando ottiene l'elemento di backup il cui FriendlyName corrisponde al valore passato nel parametro FriendlyName e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="9e94b-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="9e94b-120">L'uso del parametro FriendlyName può determinare la restituzione di più di una condivisione di file Azure.</span><span class="sxs-lookup"><span data-stu-id="9e94b-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="9e94b-121">In questi casi, Esegui il cmdlet passando il parametro value for-Name come proprietà Name restituita nel set di risultati di $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="9e94b-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="9e94b-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e94b-122">PARAMETERS</span></span>

### <span data-ttu-id="9e94b-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="9e94b-123">-BackupManagementType</span></span>

<span data-ttu-id="9e94b-124">Classe di risorse protette.</span><span class="sxs-lookup"><span data-stu-id="9e94b-124">The class of resources being protected.</span></span> <span data-ttu-id="9e94b-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e94b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e94b-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="9e94b-126">AzureVM</span></span>
- <span data-ttu-id="9e94b-127">MAB</span><span class="sxs-lookup"><span data-stu-id="9e94b-127">MAB</span></span>
- <span data-ttu-id="9e94b-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="9e94b-128">AzureStorage</span></span>
- <span data-ttu-id="9e94b-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="9e94b-129">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e94b-130">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="9e94b-130">-Container</span></span>

<span data-ttu-id="9e94b-131">Specifica un oggetto contenitore da cui questo cmdlet ottiene gli elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="9e94b-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="9e94b-132">Per ottenere un **AzureRmRecoveryServicesBackupContainer** , usare il cmdlet **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="9e94b-132">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e94b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e94b-133">-DefaultProfile</span></span>

<span data-ttu-id="9e94b-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e94b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e94b-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="9e94b-135">-DeleteState</span></span>
<span data-ttu-id="9e94b-136">Specifica il DeleteState dell'elemento i valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e94b-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e94b-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="9e94b-137">ToBeDeleted</span></span>
- <span data-ttu-id="9e94b-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="9e94b-138">NotDeleted</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e94b-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9e94b-139">-FriendlyName</span></span>
<span data-ttu-id="9e94b-140">FriendlyName dell'elemento di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="9e94b-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="9e94b-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e94b-141">-Name</span></span>

<span data-ttu-id="9e94b-142">Specifica il nome dell'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="9e94b-142">Specifies the name of backup item.</span></span> <span data-ttu-id="9e94b-143">Per la condivisione file, specificare l'ID univoco della condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="9e94b-143">For file share, specify the unique ID of protected file share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e94b-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="9e94b-144">-Policy</span></span>

<span data-ttu-id="9e94b-145">Oggetto Criteri di protezione.</span><span class="sxs-lookup"><span data-stu-id="9e94b-145">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e94b-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="9e94b-146">-ProtectionState</span></span>

<span data-ttu-id="9e94b-147">Specifica lo stato di protezione.</span><span class="sxs-lookup"><span data-stu-id="9e94b-147">Specifies the state of protection.</span></span>
<span data-ttu-id="9e94b-148">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e94b-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e94b-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="9e94b-149">IRPending.</span></span>
<span data-ttu-id="9e94b-150">La sincronizzazione iniziale non è stata avviata e non è ancora disponibile un punto di recupero.</span><span class="sxs-lookup"><span data-stu-id="9e94b-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="9e94b-151">Protetta.</span><span class="sxs-lookup"><span data-stu-id="9e94b-151">Protected.</span></span>
<span data-ttu-id="9e94b-152">La protezione è in corso.</span><span class="sxs-lookup"><span data-stu-id="9e94b-152">Protection is ongoing.</span></span>
- <span data-ttu-id="9e94b-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="9e94b-153">ProtectionError.</span></span>
<span data-ttu-id="9e94b-154">Si è verificato un errore di protezione.</span><span class="sxs-lookup"><span data-stu-id="9e94b-154">There is a protection error.</span></span>
- <span data-ttu-id="9e94b-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="9e94b-155">ProtectionStopped.</span></span>
<span data-ttu-id="9e94b-156">La protezione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="9e94b-156">Protection is disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e94b-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="9e94b-157">-ProtectionStatus</span></span>

<span data-ttu-id="9e94b-158">Specifica lo stato di protezione complessivo di un elemento nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="9e94b-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="9e94b-159">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e94b-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e94b-160">Sano</span><span class="sxs-lookup"><span data-stu-id="9e94b-160">Healthy</span></span>
- <span data-ttu-id="9e94b-161">Malsano</span><span class="sxs-lookup"><span data-stu-id="9e94b-161">Unhealthy</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e94b-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9e94b-162">-VaultId</span></span>

<span data-ttu-id="9e94b-163">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9e94b-163">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e94b-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="9e94b-164">-WorkloadType</span></span>

<span data-ttu-id="9e94b-165">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9e94b-165">Workload type of the resource.</span></span> <span data-ttu-id="9e94b-166">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9e94b-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e94b-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="9e94b-167">AzureVM</span></span>
- <span data-ttu-id="9e94b-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="9e94b-168">AzureFiles</span></span>
- <span data-ttu-id="9e94b-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="9e94b-169">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e94b-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e94b-170">CommonParameters</span></span>
<span data-ttu-id="9e94b-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e94b-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e94b-172">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e94b-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e94b-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e94b-173">INPUTS</span></span>

### <span data-ttu-id="9e94b-174">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="9e94b-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="9e94b-175">System. String</span><span class="sxs-lookup"><span data-stu-id="9e94b-175">System.String</span></span>

## <span data-ttu-id="9e94b-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e94b-176">OUTPUTS</span></span>

### <span data-ttu-id="9e94b-177">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="9e94b-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="9e94b-178">Note</span><span class="sxs-lookup"><span data-stu-id="9e94b-178">NOTES</span></span>

## <span data-ttu-id="9e94b-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e94b-179">RELATED LINKS</span></span>

[<span data-ttu-id="9e94b-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9e94b-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="9e94b-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9e94b-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="9e94b-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="9e94b-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="9e94b-183">Ripristinare-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9e94b-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
