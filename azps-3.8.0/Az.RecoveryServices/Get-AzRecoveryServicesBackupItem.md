---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 75eb9975a578e1114e994b08949eda8d3dafda0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018848"
---
# <span data-ttu-id="7f340-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7f340-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="7f340-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f340-102">SYNOPSIS</span></span>

<span data-ttu-id="7f340-103">Ottiene gli elementi da un contenitore nel backup.</span><span class="sxs-lookup"><span data-stu-id="7f340-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="7f340-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f340-104">SYNTAX</span></span>

### <span data-ttu-id="7f340-105">GetItemsForContainer (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f340-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f340-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="7f340-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f340-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="7f340-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f340-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f340-108">DESCRIPTION</span></span>

<span data-ttu-id="7f340-109">Il cmdlet **Get-AzRecoveryServicesBackupItem** ottiene gli elementi in un contenitore o un valore in Azure Backup e lo stato di protezione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="7f340-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="7f340-110">Un contenitore registrato in un Vault di servizi di ripristino di Azure può avere uno o più elementi che possono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="7f340-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="7f340-111">Per le macchine virtuali di Azure può essere presente un solo elemento di backup nel contenitore della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f340-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="7f340-112">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="7f340-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="7f340-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f340-113">EXAMPLES</span></span>

### <span data-ttu-id="7f340-114">Esempio 1: ottenere un elemento da un contenitore di backup</span><span class="sxs-lookup"><span data-stu-id="7f340-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="7f340-115">Il primo comando ottiene il contenitore di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="7f340-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="7f340-116">Il secondo comando ottiene l'elemento di backup denominato V2VM in $Container e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="7f340-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="7f340-117">Esempio 2: ottenere un elemento di condivisione file di Azure da FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7f340-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="7f340-118">Il primo comando ottiene il contenitore di tipo AzureStorage e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="7f340-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="7f340-119">Il secondo comando ottiene l'elemento di backup il cui FriendlyName corrisponde al valore passato nel parametro FriendlyName e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="7f340-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="7f340-120">L'uso del parametro FriendlyName può determinare la restituzione di più di una condivisione di file Azure.</span><span class="sxs-lookup"><span data-stu-id="7f340-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="7f340-121">In questi casi, usare il parametro Name con il valore parameter come proprietà Name restituita nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="7f340-121">In such cases use -Name parameter with parameter value as the Name property returned in $BackupItem variable.</span></span>

## <span data-ttu-id="7f340-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f340-122">PARAMETERS</span></span>

### <span data-ttu-id="7f340-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7f340-123">-BackupManagementType</span></span>

<span data-ttu-id="7f340-124">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="7f340-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="7f340-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f340-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f340-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7f340-126">AzureVM</span></span>
- <span data-ttu-id="7f340-127">Marte</span><span class="sxs-lookup"><span data-stu-id="7f340-127">MARS</span></span>
- <span data-ttu-id="7f340-128">SCDPM</span><span class="sxs-lookup"><span data-stu-id="7f340-128">SCDPM</span></span>
- <span data-ttu-id="7f340-129">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="7f340-129">AzureBackupServer</span></span>
- <span data-ttu-id="7f340-130">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="7f340-130">AzureSQL</span></span>
- <span data-ttu-id="7f340-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="7f340-131">AzureStorage</span></span>
- <span data-ttu-id="7f340-132">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="7f340-132">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f340-133">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="7f340-133">-Container</span></span>

<span data-ttu-id="7f340-134">Specifica un oggetto contenitore da cui questo cmdlet ottiene gli elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="7f340-134">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="7f340-135">Per ottenere un **AzureRmRecoveryServicesBackupContainer** , usare il cmdlet **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="7f340-135">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="7f340-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f340-136">-DefaultProfile</span></span>

<span data-ttu-id="7f340-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f340-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f340-138">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="7f340-138">-DeleteState</span></span>
<span data-ttu-id="7f340-139">Specifica il DeleteState dell'elemento i valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f340-139">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f340-140">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="7f340-140">ToBeDeleted</span></span>
- <span data-ttu-id="7f340-141">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="7f340-141">NotDeleted</span></span>

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

### <span data-ttu-id="7f340-142">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7f340-142">-FriendlyName</span></span>
<span data-ttu-id="7f340-143">FriendlyName dell'elemento di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="7f340-143">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="7f340-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f340-144">-Name</span></span>

<span data-ttu-id="7f340-145">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="7f340-145">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="7f340-146">-Policy</span><span class="sxs-lookup"><span data-stu-id="7f340-146">-Policy</span></span>

<span data-ttu-id="7f340-147">Oggetto Criteri di protezione.</span><span class="sxs-lookup"><span data-stu-id="7f340-147">Protection policy object.</span></span>

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

### <span data-ttu-id="7f340-148">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="7f340-148">-ProtectionState</span></span>

<span data-ttu-id="7f340-149">Specifica lo stato di protezione.</span><span class="sxs-lookup"><span data-stu-id="7f340-149">Specifies the state of protection.</span></span>
<span data-ttu-id="7f340-150">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f340-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f340-151">IRPending.</span><span class="sxs-lookup"><span data-stu-id="7f340-151">IRPending.</span></span>
<span data-ttu-id="7f340-152">La sincronizzazione iniziale non è stata avviata e non è ancora disponibile un punto di recupero.</span><span class="sxs-lookup"><span data-stu-id="7f340-152">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="7f340-153">Protetta.</span><span class="sxs-lookup"><span data-stu-id="7f340-153">Protected.</span></span>
<span data-ttu-id="7f340-154">La protezione è in corso.</span><span class="sxs-lookup"><span data-stu-id="7f340-154">Protection is ongoing.</span></span>
- <span data-ttu-id="7f340-155">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="7f340-155">ProtectionError.</span></span>
<span data-ttu-id="7f340-156">Si è verificato un errore di protezione.</span><span class="sxs-lookup"><span data-stu-id="7f340-156">There is a protection error.</span></span>
- <span data-ttu-id="7f340-157">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="7f340-157">ProtectionStopped.</span></span>
<span data-ttu-id="7f340-158">La protezione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="7f340-158">Protection is disabled.</span></span>

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

### <span data-ttu-id="7f340-159">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="7f340-159">-ProtectionStatus</span></span>

<span data-ttu-id="7f340-160">Specifica lo stato di protezione complessivo di un elemento nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="7f340-160">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="7f340-161">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f340-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f340-162">Sano</span><span class="sxs-lookup"><span data-stu-id="7f340-162">Healthy</span></span>
- <span data-ttu-id="7f340-163">Malsano</span><span class="sxs-lookup"><span data-stu-id="7f340-163">Unhealthy</span></span>

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

### <span data-ttu-id="7f340-164">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7f340-164">-VaultId</span></span>

<span data-ttu-id="7f340-165">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f340-165">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7f340-166">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="7f340-166">-WorkloadType</span></span>

<span data-ttu-id="7f340-167">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7f340-167">Specifies the workload type.</span></span>
<span data-ttu-id="7f340-168">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f340-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7f340-169">AzureVM</span><span class="sxs-lookup"><span data-stu-id="7f340-169">AzureVM</span></span>
- <span data-ttu-id="7f340-170">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="7f340-170">AzureSQLDatabase</span></span>
- <span data-ttu-id="7f340-171">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="7f340-171">AzureFiles</span></span>
- <span data-ttu-id="7f340-172">MSSQL</span><span class="sxs-lookup"><span data-stu-id="7f340-172">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f340-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f340-173">CommonParameters</span></span>
<span data-ttu-id="7f340-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f340-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f340-175">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f340-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f340-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f340-176">INPUTS</span></span>

### <span data-ttu-id="7f340-177">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="7f340-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="7f340-178">System. String</span><span class="sxs-lookup"><span data-stu-id="7f340-178">System.String</span></span>

## <span data-ttu-id="7f340-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f340-179">OUTPUTS</span></span>

### <span data-ttu-id="7f340-180">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="7f340-180">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="7f340-181">Note</span><span class="sxs-lookup"><span data-stu-id="7f340-181">NOTES</span></span>

## <span data-ttu-id="7f340-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f340-182">RELATED LINKS</span></span>

[<span data-ttu-id="7f340-183">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7f340-183">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="7f340-184">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7f340-184">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="7f340-185">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7f340-185">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="7f340-186">Ripristinare-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7f340-186">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
