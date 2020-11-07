---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 2dfc4b8fd0491a9f8c2200876609ab0a8cb00cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855749"
---
# <span data-ttu-id="c3546-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c3546-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="c3546-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3546-102">SYNOPSIS</span></span>

<span data-ttu-id="c3546-103">Ottiene gli elementi da un contenitore nel backup.</span><span class="sxs-lookup"><span data-stu-id="c3546-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="c3546-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3546-104">SYNTAX</span></span>

### <span data-ttu-id="c3546-105">GetItemsForContainer (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3546-105">GetItemsForContainer (Default)</span></span>

```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3546-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="c3546-106">GetItemsForVault</span></span>

```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3546-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="c3546-107">GetItemsForPolicy</span></span>

```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [[-DeleteState] <ItemDeleteState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3546-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3546-108">DESCRIPTION</span></span>

<span data-ttu-id="c3546-109">Il cmdlet **Get-AzRecoveryServicesBackupItem** ottiene gli elementi in un contenitore o un valore in Azure Backup e lo stato di protezione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="c3546-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="c3546-110">Un contenitore registrato in un Vault di servizi di ripristino di Azure può avere uno o più elementi che possono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="c3546-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="c3546-111">Per le macchine virtuali di Azure può essere presente un solo elemento di backup nel contenitore della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c3546-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="c3546-112">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="c3546-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="c3546-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3546-113">EXAMPLES</span></span>

### <span data-ttu-id="c3546-114">Esempio 1: ottenere un elemento da un contenitore di backup</span><span class="sxs-lookup"><span data-stu-id="c3546-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="c3546-115">Il primo comando ottiene il contenitore di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="c3546-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="c3546-116">Il secondo comando ottiene l'elemento di backup denominato V2VM in $Container e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="c3546-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="c3546-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3546-117">PARAMETERS</span></span>

### <span data-ttu-id="c3546-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="c3546-118">-BackupManagementType</span></span>

<span data-ttu-id="c3546-119">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="c3546-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="c3546-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3546-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3546-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="c3546-121">AzureVM</span></span>
- <span data-ttu-id="c3546-122">Marte</span><span class="sxs-lookup"><span data-stu-id="c3546-122">MARS</span></span>
- <span data-ttu-id="c3546-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="c3546-123">SCDPM</span></span>
- <span data-ttu-id="c3546-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="c3546-124">AzureBackupServer</span></span>
- <span data-ttu-id="c3546-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="c3546-125">AzureSQL</span></span>
- <span data-ttu-id="c3546-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="c3546-126">AzureStorage</span></span>
- <span data-ttu-id="c3546-127">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="c3546-127">AzureWorkload</span></span>

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

### <span data-ttu-id="c3546-128">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="c3546-128">-Container</span></span>

<span data-ttu-id="c3546-129">Specifica un oggetto contenitore da cui questo cmdlet ottiene gli elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="c3546-129">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="c3546-130">Per ottenere un **AzureRmRecoveryServicesBackupContainer** , usare il cmdlet **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="c3546-130">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="c3546-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3546-131">-DefaultProfile</span></span>

<span data-ttu-id="c3546-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3546-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3546-133">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="c3546-133">-DeleteState</span></span>
<span data-ttu-id="c3546-134">Specifica il DeleteState dell'elemento i valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3546-134">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3546-135">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="c3546-135">ToBeDeleted</span></span>
- <span data-ttu-id="c3546-136">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="c3546-136">NotDeleted</span></span>

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

### <span data-ttu-id="c3546-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3546-137">-Name</span></span>

<span data-ttu-id="c3546-138">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="c3546-138">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="c3546-139">-Policy</span><span class="sxs-lookup"><span data-stu-id="c3546-139">-Policy</span></span>

<span data-ttu-id="c3546-140">Oggetto Criteri di protezione.</span><span class="sxs-lookup"><span data-stu-id="c3546-140">Protection policy object.</span></span>

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

### <span data-ttu-id="c3546-141">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="c3546-141">-ProtectionState</span></span>

<span data-ttu-id="c3546-142">Specifica lo stato di protezione.</span><span class="sxs-lookup"><span data-stu-id="c3546-142">Specifies the state of protection.</span></span>
<span data-ttu-id="c3546-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3546-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3546-144">IRPending.</span><span class="sxs-lookup"><span data-stu-id="c3546-144">IRPending.</span></span>
<span data-ttu-id="c3546-145">La sincronizzazione iniziale non è stata avviata e non è ancora disponibile un punto di recupero.</span><span class="sxs-lookup"><span data-stu-id="c3546-145">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="c3546-146">Protetta.</span><span class="sxs-lookup"><span data-stu-id="c3546-146">Protected.</span></span>
<span data-ttu-id="c3546-147">La protezione è in corso.</span><span class="sxs-lookup"><span data-stu-id="c3546-147">Protection is ongoing.</span></span>
- <span data-ttu-id="c3546-148">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="c3546-148">ProtectionError.</span></span>
<span data-ttu-id="c3546-149">Si è verificato un errore di protezione.</span><span class="sxs-lookup"><span data-stu-id="c3546-149">There is a protection error.</span></span>
- <span data-ttu-id="c3546-150">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="c3546-150">ProtectionStopped.</span></span>
<span data-ttu-id="c3546-151">La protezione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c3546-151">Protection is disabled.</span></span>

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

### <span data-ttu-id="c3546-152">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="c3546-152">-ProtectionStatus</span></span>

<span data-ttu-id="c3546-153">Specifica lo stato di protezione complessivo di un elemento nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="c3546-153">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="c3546-154">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3546-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3546-155">Sano</span><span class="sxs-lookup"><span data-stu-id="c3546-155">Healthy</span></span>
- <span data-ttu-id="c3546-156">Malsano</span><span class="sxs-lookup"><span data-stu-id="c3546-156">Unhealthy</span></span>

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

### <span data-ttu-id="c3546-157">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c3546-157">-VaultId</span></span>

<span data-ttu-id="c3546-158">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c3546-158">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c3546-159">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="c3546-159">-WorkloadType</span></span>

<span data-ttu-id="c3546-160">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c3546-160">Specifies the workload type.</span></span>
<span data-ttu-id="c3546-161">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3546-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3546-162">AzureVM</span><span class="sxs-lookup"><span data-stu-id="c3546-162">AzureVM</span></span>
- <span data-ttu-id="c3546-163">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="c3546-163">AzureSQLDatabase</span></span>
- <span data-ttu-id="c3546-164">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="c3546-164">AzureFiles</span></span>
- <span data-ttu-id="c3546-165">MSSQL</span><span class="sxs-lookup"><span data-stu-id="c3546-165">MSSQL</span></span>

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

### <span data-ttu-id="c3546-166">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3546-166">-CommonParameters</span></span>

<span data-ttu-id="c3546-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3546-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3546-168">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3546-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3546-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3546-169">INPUTS</span></span>

### <span data-ttu-id="c3546-170">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="c3546-170">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="c3546-171">System. String</span><span class="sxs-lookup"><span data-stu-id="c3546-171">System.String</span></span>

## <span data-ttu-id="c3546-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3546-172">OUTPUTS</span></span>

### <span data-ttu-id="c3546-173">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="c3546-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="c3546-174">Note</span><span class="sxs-lookup"><span data-stu-id="c3546-174">NOTES</span></span>

## <span data-ttu-id="c3546-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3546-175">RELATED LINKS</span></span>

[<span data-ttu-id="c3546-176">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c3546-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="c3546-177">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c3546-177">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="c3546-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c3546-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="c3546-179">Ripristinare-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c3546-179">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
