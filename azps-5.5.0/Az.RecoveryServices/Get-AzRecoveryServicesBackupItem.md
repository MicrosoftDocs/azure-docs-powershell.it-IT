---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 8124122b59dcee8a654d52c6f1d9382cb90e2a10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206211"
---
# <span data-ttu-id="94df9-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="94df9-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="94df9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94df9-102">SYNOPSIS</span></span>

<span data-ttu-id="94df9-103">Recupera gli elementi da un contenitore in Backup.</span><span class="sxs-lookup"><span data-stu-id="94df9-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="94df9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94df9-104">SYNTAX</span></span>

### <span data-ttu-id="94df9-105">GetItemsForContainer (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94df9-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="94df9-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="94df9-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="94df9-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="94df9-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

## <span data-ttu-id="94df9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94df9-108">DESCRIPTION</span></span>

<span data-ttu-id="94df9-109">Il cmdlet **Get-AzRecoveryServicesBackupItem** ottiene l'elenco degli elementi protetti in un contenitore e lo stato di protezione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="94df9-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="94df9-110">Un contenitore registrato in un vault di Servizi di ripristino di Azure può contenere uno o più elementi che possono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="94df9-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="94df9-111">Per le macchine virtuali di Azure, può essere presente un solo elemento di backup nel contenitore di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="94df9-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="94df9-112">Impostare il contesto del vault usando il parametro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="94df9-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="94df9-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94df9-113">EXAMPLES</span></span>

### <span data-ttu-id="94df9-114">Esempio 1: Recuperare un elemento da un contenitore Backup</span><span class="sxs-lookup"><span data-stu-id="94df9-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="94df9-115">Il primo comando ottiene il contenitore di tipo AzureVM e quindi lo archivia nella $Container variabile.</span><span class="sxs-lookup"><span data-stu-id="94df9-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="94df9-116">Il secondo comando recupera l'elemento di backup denominato V2VM in $Container e quindi lo archivia nella $BackupItem variabile.</span><span class="sxs-lookup"><span data-stu-id="94df9-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="94df9-117">Esempio 2: Ottenere un elemento Condivisione file di Azure da FriendlyName</span><span class="sxs-lookup"><span data-stu-id="94df9-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -FriendlyName "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="94df9-118">Il primo comando ottiene il contenitore di tipo AzureStorage e quindi lo archivia nella $Container variabile.</span><span class="sxs-lookup"><span data-stu-id="94df9-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="94df9-119">Il secondo comando ottiene l'elemento backup il cui nome friendlyName corrisponde al valore passato in Parametro FriendlyName e quindi lo archivia nella $BackupItem variabile.</span><span class="sxs-lookup"><span data-stu-id="94df9-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="94df9-120">L'uso del parametro FriendlyName può comportare la restituzione di più di una condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="94df9-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="94df9-121">In questi casi, eseguire il cmdlet passando il valore per il parametro -Name come proprietà Name restituita nel set di risultati di $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="94df9-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="94df9-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94df9-122">PARAMETERS</span></span>

### <span data-ttu-id="94df9-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="94df9-123">-BackupManagementType</span></span>

<span data-ttu-id="94df9-124">Classe di risorse protetta.</span><span class="sxs-lookup"><span data-stu-id="94df9-124">The class of resources being protected.</span></span> <span data-ttu-id="94df9-125">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="94df9-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94df9-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="94df9-126">AzureVM</span></span>
- <span data-ttu-id="94df9-127">MAB</span><span class="sxs-lookup"><span data-stu-id="94df9-127">MAB</span></span>
- <span data-ttu-id="94df9-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="94df9-128">AzureStorage</span></span>
- <span data-ttu-id="94df9-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="94df9-129">AzureWorkload</span></span>

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

### <span data-ttu-id="94df9-130">-Container</span><span class="sxs-lookup"><span data-stu-id="94df9-130">-Container</span></span>

<span data-ttu-id="94df9-131">Specifica un oggetto contenitore da cui questo cmdlet ottiene gli elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="94df9-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="94df9-132">Per ottenere un **cmdlet AzureRmRecoveryServicesBackupContainer,** usare il cmdlet **Get-AzRecoveryServicesBackupContainer.**</span><span class="sxs-lookup"><span data-stu-id="94df9-132">To obtain an **AzureRmRecoveryServicesBackupContainer**, use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="94df9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94df9-133">-DefaultProfile</span></span>

<span data-ttu-id="94df9-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94df9-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94df9-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="94df9-135">-DeleteState</span></span>
<span data-ttu-id="94df9-136">Specifica lo stato di eliminazione dell'elemento I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="94df9-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94df9-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="94df9-137">ToBeDeleted</span></span>
- <span data-ttu-id="94df9-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="94df9-138">NotDeleted</span></span>

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

### <span data-ttu-id="94df9-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="94df9-139">-FriendlyName</span></span>
<span data-ttu-id="94df9-140">FriendlyName dell'elemento di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="94df9-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="94df9-141">-Name</span><span class="sxs-lookup"><span data-stu-id="94df9-141">-Name</span></span>

<span data-ttu-id="94df9-142">Specifica il nome dell'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="94df9-142">Specifies the name of backup item.</span></span> <span data-ttu-id="94df9-143">Per la condivisione file, specificare l'ID univoco della condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="94df9-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="94df9-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="94df9-144">-Policy</span></span>

<span data-ttu-id="94df9-145">Oggetto criterio di protezione.</span><span class="sxs-lookup"><span data-stu-id="94df9-145">Protection policy object.</span></span>

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

### <span data-ttu-id="94df9-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="94df9-146">-ProtectionState</span></span>

<span data-ttu-id="94df9-147">Specifica lo stato di protezione.</span><span class="sxs-lookup"><span data-stu-id="94df9-147">Specifies the state of protection.</span></span>
<span data-ttu-id="94df9-148">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="94df9-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94df9-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="94df9-149">IRPending.</span></span>
<span data-ttu-id="94df9-150">La sincronizzazione iniziale non è stata avviata e non è ancora disponibile un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="94df9-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="94df9-151">Protetto.</span><span class="sxs-lookup"><span data-stu-id="94df9-151">Protected.</span></span>
<span data-ttu-id="94df9-152">La protezione è continua.</span><span class="sxs-lookup"><span data-stu-id="94df9-152">Protection is ongoing.</span></span>
- <span data-ttu-id="94df9-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="94df9-153">ProtectionError.</span></span>
<span data-ttu-id="94df9-154">Si è verificato un errore di protezione.</span><span class="sxs-lookup"><span data-stu-id="94df9-154">There is a protection error.</span></span>
- <span data-ttu-id="94df9-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="94df9-155">ProtectionStopped.</span></span>
<span data-ttu-id="94df9-156">La protezione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="94df9-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="94df9-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="94df9-157">-ProtectionStatus</span></span>

<span data-ttu-id="94df9-158">Specifica lo stato di protezione generale di un elemento nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="94df9-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="94df9-159">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="94df9-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94df9-160">Integro</span><span class="sxs-lookup"><span data-stu-id="94df9-160">Healthy</span></span>
- <span data-ttu-id="94df9-161">Non integro</span><span class="sxs-lookup"><span data-stu-id="94df9-161">Unhealthy</span></span>

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

### <span data-ttu-id="94df9-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="94df9-162">-VaultId</span></span>

<span data-ttu-id="94df9-163">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="94df9-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="94df9-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="94df9-164">-WorkloadType</span></span>

<span data-ttu-id="94df9-165">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="94df9-165">Workload type of the resource.</span></span> <span data-ttu-id="94df9-166">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="94df9-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="94df9-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="94df9-167">AzureVM</span></span>
- <span data-ttu-id="94df9-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="94df9-168">AzureFiles</span></span>
- <span data-ttu-id="94df9-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="94df9-169">MSSQL</span></span>

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

### <span data-ttu-id="94df9-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94df9-170">CommonParameters</span></span>
<span data-ttu-id="94df9-171">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94df9-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94df9-172">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94df9-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94df9-173">INPUT</span><span class="sxs-lookup"><span data-stu-id="94df9-173">INPUTS</span></span>

### <span data-ttu-id="94df9-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="94df9-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="94df9-175">System.String</span><span class="sxs-lookup"><span data-stu-id="94df9-175">System.String</span></span>

## <span data-ttu-id="94df9-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94df9-176">OUTPUTS</span></span>

### <span data-ttu-id="94df9-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="94df9-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="94df9-178">NOTE</span><span class="sxs-lookup"><span data-stu-id="94df9-178">NOTES</span></span>

## <span data-ttu-id="94df9-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94df9-179">RELATED LINKS</span></span>

[<span data-ttu-id="94df9-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="94df9-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="94df9-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="94df9-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="94df9-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="94df9-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="94df9-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="94df9-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
