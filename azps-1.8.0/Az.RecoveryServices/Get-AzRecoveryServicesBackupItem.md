---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: c861bbe3b422360f58f36cbe859343f7dcc7ed37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677671"
---
# <span data-ttu-id="d94ac-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d94ac-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="d94ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d94ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d94ac-103">Ottiene gli elementi da un contenitore nel backup.</span><span class="sxs-lookup"><span data-stu-id="d94ac-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="d94ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d94ac-104">SYNTAX</span></span>

### <span data-ttu-id="d94ac-105">GetItemsForContainer (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d94ac-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d94ac-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="d94ac-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d94ac-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="d94ac-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d94ac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d94ac-108">DESCRIPTION</span></span>
<span data-ttu-id="d94ac-109">Il cmdlet **Get-AzRecoveryServicesBackupItem** ottiene gli elementi in un contenitore o un valore in Azure Backup e lo stato di protezione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="d94ac-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="d94ac-110">Un contenitore registrato in un Vault di servizi di ripristino di Azure può avere uno o più elementi che possono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="d94ac-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="d94ac-111">Per le macchine virtuali di Azure può essere presente un solo elemento di backup nel contenitore della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d94ac-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="d94ac-112">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="d94ac-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d94ac-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d94ac-113">EXAMPLES</span></span>

### <span data-ttu-id="d94ac-114">Esempio 1: ottenere un elemento da un contenitore di backup</span><span class="sxs-lookup"><span data-stu-id="d94ac-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="d94ac-115">Il primo comando ottiene il contenitore di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="d94ac-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="d94ac-116">Il secondo comando ottiene l'elemento di backup denominato V2VM in $Container e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d94ac-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="d94ac-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d94ac-117">PARAMETERS</span></span>

### <span data-ttu-id="d94ac-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d94ac-118">-BackupManagementType</span></span>
<span data-ttu-id="d94ac-119">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="d94ac-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="d94ac-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d94ac-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d94ac-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d94ac-121">AzureVM</span></span> 
- <span data-ttu-id="d94ac-122">Marte</span><span class="sxs-lookup"><span data-stu-id="d94ac-122">MARS</span></span> 
- <span data-ttu-id="d94ac-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="d94ac-123">SCDPM</span></span> 
- <span data-ttu-id="d94ac-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="d94ac-124">AzureBackupServer</span></span> 
- <span data-ttu-id="d94ac-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="d94ac-125">AzureSQL</span></span>
- <span data-ttu-id="d94ac-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="d94ac-126">AzureStorage</span></span>

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

### <span data-ttu-id="d94ac-127">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="d94ac-127">-Container</span></span>
<span data-ttu-id="d94ac-128">Specifica un oggetto contenitore da cui questo cmdlet ottiene gli elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="d94ac-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="d94ac-129">Per ottenere un **AzureRmRecoveryServicesBackupContainer** , usare il cmdlet Get-AzRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="d94ac-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="d94ac-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94ac-130">-DefaultProfile</span></span>
<span data-ttu-id="d94ac-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d94ac-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d94ac-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="d94ac-132">-Name</span></span>
<span data-ttu-id="d94ac-133">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="d94ac-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="d94ac-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="d94ac-134">-Policy</span></span>
<span data-ttu-id="d94ac-135">Oggetto Criteri di protezione.</span><span class="sxs-lookup"><span data-stu-id="d94ac-135">Protection policy object.</span></span>

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

### <span data-ttu-id="d94ac-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="d94ac-136">-ProtectionState</span></span>
<span data-ttu-id="d94ac-137">Specifica lo stato di protezione.</span><span class="sxs-lookup"><span data-stu-id="d94ac-137">Specifies the state of protection.</span></span>
<span data-ttu-id="d94ac-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d94ac-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d94ac-139">IRPending.</span><span class="sxs-lookup"><span data-stu-id="d94ac-139">IRPending.</span></span>
<span data-ttu-id="d94ac-140">La sincronizzazione iniziale non è stata avviata e non è ancora disponibile un punto di recupero.</span><span class="sxs-lookup"><span data-stu-id="d94ac-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="d94ac-141">Protetta.</span><span class="sxs-lookup"><span data-stu-id="d94ac-141">Protected.</span></span>
<span data-ttu-id="d94ac-142">La protezione è in corso.</span><span class="sxs-lookup"><span data-stu-id="d94ac-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="d94ac-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="d94ac-143">ProtectionError.</span></span>
<span data-ttu-id="d94ac-144">Si è verificato un errore di protezione.</span><span class="sxs-lookup"><span data-stu-id="d94ac-144">There is a protection error.</span></span>
- <span data-ttu-id="d94ac-145">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="d94ac-145">ProtectionStopped.</span></span>
<span data-ttu-id="d94ac-146">La protezione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="d94ac-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="d94ac-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="d94ac-147">-ProtectionStatus</span></span>
<span data-ttu-id="d94ac-148">Specifica lo stato di protezione complessivo di un elemento nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="d94ac-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="d94ac-149">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d94ac-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d94ac-150">Sano</span><span class="sxs-lookup"><span data-stu-id="d94ac-150">Healthy</span></span>
- <span data-ttu-id="d94ac-151">Malsano</span><span class="sxs-lookup"><span data-stu-id="d94ac-151">Unhealthy</span></span>

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

### <span data-ttu-id="d94ac-152">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d94ac-152">-VaultId</span></span>
<span data-ttu-id="d94ac-153">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d94ac-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d94ac-154">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d94ac-154">-WorkloadType</span></span>
<span data-ttu-id="d94ac-155">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d94ac-155">Specifies the workload type.</span></span> <span data-ttu-id="d94ac-156">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d94ac-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d94ac-157">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d94ac-157">AzureVM</span></span> 
- <span data-ttu-id="d94ac-158">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="d94ac-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="d94ac-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="d94ac-159">AzureFiles</span></span>

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

### <span data-ttu-id="d94ac-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94ac-160">CommonParameters</span></span>
<span data-ttu-id="d94ac-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d94ac-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94ac-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d94ac-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94ac-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d94ac-163">INPUTS</span></span>

### <span data-ttu-id="d94ac-164">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="d94ac-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="d94ac-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d94ac-165">System.String</span></span>

## <span data-ttu-id="d94ac-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d94ac-166">OUTPUTS</span></span>

### <span data-ttu-id="d94ac-167">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="d94ac-167">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="d94ac-168">Note</span><span class="sxs-lookup"><span data-stu-id="d94ac-168">NOTES</span></span>

## <span data-ttu-id="d94ac-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d94ac-169">RELATED LINKS</span></span>

[<span data-ttu-id="d94ac-170">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d94ac-170">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="d94ac-171">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d94ac-171">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="d94ac-172">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d94ac-172">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="d94ac-173">Ripristinare-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d94ac-173">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)


