---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 084f18e1091059680e0c59b234b295120049cef6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984253"
---
# <span data-ttu-id="1d802-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="1d802-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="1d802-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d802-102">SYNOPSIS</span></span>

<span data-ttu-id="1d802-103">Recupera gli elementi da un contenitore nel backup.</span><span class="sxs-lookup"><span data-stu-id="1d802-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="1d802-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d802-104">SYNTAX</span></span>

### <span data-ttu-id="1d802-105">GetItemsForContainer (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d802-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="1d802-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="1d802-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="1d802-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="1d802-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

## <span data-ttu-id="1d802-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1d802-108">DESCRIPTION</span></span>

<span data-ttu-id="1d802-109">Il cmdlet **Get-AzRecoveryServicesBackupItem** ottiene l'elenco degli elementi protetti in un contenitore e lo stato di protezione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="1d802-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="1d802-110">Un contenitore registrato in un vault dei servizi di ripristino di Azure può contenere uno o più elementi che possono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="1d802-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="1d802-111">Per le macchine virtuali di Azure, può essere presente un solo elemento di backup nel contenitore di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="1d802-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="1d802-112">Impostare il contesto del vault usando il parametro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="1d802-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="1d802-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d802-113">EXAMPLES</span></span>

### <span data-ttu-id="1d802-114">Esempio 1: Recuperare un elemento da un contenitore Backup</span><span class="sxs-lookup"><span data-stu-id="1d802-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="1d802-115">Il primo comando ottiene il contenitore di tipo AzureVM e quindi lo archivia nella $Container variabile.</span><span class="sxs-lookup"><span data-stu-id="1d802-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="1d802-116">Il secondo comando recupera l'elemento di backup denominato V2VM in $Container e quindi lo archivia nella $BackupItem variabile.</span><span class="sxs-lookup"><span data-stu-id="1d802-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="1d802-117">Esempio 2: Ottenere un elemento Condivisione file di Azure da FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1d802-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -FriendlyName "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="1d802-118">Il primo comando ottiene il contenitore di tipo AzureStorage e quindi lo archivia nella $Container variabile.</span><span class="sxs-lookup"><span data-stu-id="1d802-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="1d802-119">Il secondo comando ottiene l'elemento di backup il cui valore friendlyName corrisponde al valore passato in Parametro FriendlyName e quindi lo archivia nella $BackupItem variabile.</span><span class="sxs-lookup"><span data-stu-id="1d802-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="1d802-120">L'uso del parametro FriendlyName può comportare la restituzione di più di una condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d802-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="1d802-121">In questi casi, eseguire il cmdlet passando il valore per il parametro -Name come proprietà Name restituita nel set di risultati di $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="1d802-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="1d802-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d802-122">PARAMETERS</span></span>

### <span data-ttu-id="1d802-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="1d802-123">-BackupManagementType</span></span>

<span data-ttu-id="1d802-124">Classe di risorse protetta.</span><span class="sxs-lookup"><span data-stu-id="1d802-124">The class of resources being protected.</span></span> <span data-ttu-id="1d802-125">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="1d802-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d802-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="1d802-126">AzureVM</span></span>
- <span data-ttu-id="1d802-127">MAB</span><span class="sxs-lookup"><span data-stu-id="1d802-127">MAB</span></span>
- <span data-ttu-id="1d802-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="1d802-128">AzureStorage</span></span>
- <span data-ttu-id="1d802-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="1d802-129">AzureWorkload</span></span>

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

### <span data-ttu-id="1d802-130">-Container</span><span class="sxs-lookup"><span data-stu-id="1d802-130">-Container</span></span>

<span data-ttu-id="1d802-131">Specifica un oggetto contenitore da cui questo cmdlet ottiene gli elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="1d802-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="1d802-132">Per ottenere un **cmdlet AzureRmRecoveryServicesBackupContainer,** usare il cmdlet **Get-AzRecoveryServicesBackupContainer.**</span><span class="sxs-lookup"><span data-stu-id="1d802-132">To obtain an **AzureRmRecoveryServicesBackupContainer**, use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="1d802-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d802-133">-DefaultProfile</span></span>

<span data-ttu-id="1d802-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d802-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d802-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="1d802-135">-DeleteState</span></span>
<span data-ttu-id="1d802-136">Specifica lo stato di eliminazione dell'elemento I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="1d802-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d802-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="1d802-137">ToBeDeleted</span></span>
- <span data-ttu-id="1d802-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="1d802-138">NotDeleted</span></span>

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

### <span data-ttu-id="1d802-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1d802-139">-FriendlyName</span></span>
<span data-ttu-id="1d802-140">FriendlyName dell'elemento di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="1d802-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="1d802-141">-Name</span><span class="sxs-lookup"><span data-stu-id="1d802-141">-Name</span></span>

<span data-ttu-id="1d802-142">Specifica il nome dell'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="1d802-142">Specifies the name of backup item.</span></span> <span data-ttu-id="1d802-143">Per la condivisione file, specificare l'ID univoco della condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="1d802-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="1d802-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="1d802-144">-Policy</span></span>

<span data-ttu-id="1d802-145">Oggetto criterio di protezione.</span><span class="sxs-lookup"><span data-stu-id="1d802-145">Protection policy object.</span></span>

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

### <span data-ttu-id="1d802-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="1d802-146">-ProtectionState</span></span>

<span data-ttu-id="1d802-147">Specifica lo stato di protezione.</span><span class="sxs-lookup"><span data-stu-id="1d802-147">Specifies the state of protection.</span></span>
<span data-ttu-id="1d802-148">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="1d802-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d802-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="1d802-149">IRPending.</span></span>
<span data-ttu-id="1d802-150">La sincronizzazione iniziale non è stata avviata e non è ancora disponibile un punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1d802-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="1d802-151">Protetto.</span><span class="sxs-lookup"><span data-stu-id="1d802-151">Protected.</span></span>
<span data-ttu-id="1d802-152">La protezione è continua.</span><span class="sxs-lookup"><span data-stu-id="1d802-152">Protection is ongoing.</span></span>
- <span data-ttu-id="1d802-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="1d802-153">ProtectionError.</span></span>
<span data-ttu-id="1d802-154">Si è verificato un errore di protezione.</span><span class="sxs-lookup"><span data-stu-id="1d802-154">There is a protection error.</span></span>
- <span data-ttu-id="1d802-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="1d802-155">ProtectionStopped.</span></span>
<span data-ttu-id="1d802-156">La protezione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="1d802-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="1d802-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="1d802-157">-ProtectionStatus</span></span>

<span data-ttu-id="1d802-158">Specifica lo stato di protezione generale di un elemento nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="1d802-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="1d802-159">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="1d802-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d802-160">Integro</span><span class="sxs-lookup"><span data-stu-id="1d802-160">Healthy</span></span>
- <span data-ttu-id="1d802-161">Non integro</span><span class="sxs-lookup"><span data-stu-id="1d802-161">Unhealthy</span></span>

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

### <span data-ttu-id="1d802-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1d802-162">-VaultId</span></span>

<span data-ttu-id="1d802-163">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1d802-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1d802-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="1d802-164">-WorkloadType</span></span>

<span data-ttu-id="1d802-165">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1d802-165">Workload type of the resource.</span></span> <span data-ttu-id="1d802-166">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="1d802-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d802-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="1d802-167">AzureVM</span></span>
- <span data-ttu-id="1d802-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="1d802-168">AzureFiles</span></span>
- <span data-ttu-id="1d802-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="1d802-169">MSSQL</span></span>

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

### <span data-ttu-id="1d802-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d802-170">CommonParameters</span></span>
<span data-ttu-id="1d802-171">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d802-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d802-172">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d802-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d802-173">INPUT</span><span class="sxs-lookup"><span data-stu-id="1d802-173">INPUTS</span></span>

### <span data-ttu-id="1d802-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="1d802-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="1d802-175">System.String</span><span class="sxs-lookup"><span data-stu-id="1d802-175">System.String</span></span>

## <span data-ttu-id="1d802-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d802-176">OUTPUTS</span></span>

### <span data-ttu-id="1d802-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="1d802-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="1d802-178">NOTE</span><span class="sxs-lookup"><span data-stu-id="1d802-178">NOTES</span></span>

## <span data-ttu-id="1d802-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d802-179">RELATED LINKS</span></span>

[<span data-ttu-id="1d802-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="1d802-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="1d802-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="1d802-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="1d802-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1d802-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="1d802-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="1d802-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
