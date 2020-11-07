---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 03da361f8dd68d345782568dc243d4438cad1d77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687996"
---
# <span data-ttu-id="d086f-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d086f-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="d086f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d086f-102">SYNOPSIS</span></span>
<span data-ttu-id="d086f-103">Ottiene gli elementi da un contenitore nel backup.</span><span class="sxs-lookup"><span data-stu-id="d086f-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d086f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d086f-104">SYNTAX</span></span>

### <span data-ttu-id="d086f-105">GetItemsForContainer (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d086f-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d086f-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="d086f-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d086f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d086f-107">DESCRIPTION</span></span>
<span data-ttu-id="d086f-108">Il cmdlet **Get-AzureRmRecoveryServicesBackupItem** ottiene gli elementi in un contenitore o un valore in Azure Backup e lo stato di protezione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="d086f-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="d086f-109">Un contenitore registrato in un Vault di servizi di ripristino di Azure può avere uno o più elementi che possono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="d086f-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="d086f-110">Per le macchine virtuali di Azure può essere presente un solo elemento di backup nel contenitore della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d086f-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="d086f-111">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="d086f-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d086f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d086f-112">EXAMPLES</span></span>

### <span data-ttu-id="d086f-113">Esempio 1: ottenere un elemento da un contenitore di backup</span><span class="sxs-lookup"><span data-stu-id="d086f-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="d086f-114">Il primo comando ottiene il contenitore di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="d086f-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="d086f-115">Il secondo comando ottiene l'elemento di backup denominato V2VM in $Container e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="d086f-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="d086f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d086f-116">PARAMETERS</span></span>

### <span data-ttu-id="d086f-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="d086f-117">-BackupManagementType</span></span>
<span data-ttu-id="d086f-118">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="d086f-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="d086f-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d086f-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d086f-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d086f-120">AzureVM</span></span> 
- <span data-ttu-id="d086f-121">Marte</span><span class="sxs-lookup"><span data-stu-id="d086f-121">MARS</span></span> 
- <span data-ttu-id="d086f-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="d086f-122">SCDPM</span></span> 
- <span data-ttu-id="d086f-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="d086f-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d086f-124">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="d086f-124">-Container</span></span>
<span data-ttu-id="d086f-125">Specifica un oggetto contenitore da cui questo cmdlet ottiene gli elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="d086f-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="d086f-126">Per ottenere un **AzureRmRecoveryServicesBackupContainer** , usare il cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="d086f-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="d086f-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d086f-127">-Name</span></span>
<span data-ttu-id="d086f-128">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="d086f-128">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="d086f-129">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="d086f-129">-ProtectionState</span></span>
<span data-ttu-id="d086f-130">Specifica lo stato di protezione.</span><span class="sxs-lookup"><span data-stu-id="d086f-130">Specifies the state of protection.</span></span>
<span data-ttu-id="d086f-131">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d086f-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d086f-132">IRPending.</span><span class="sxs-lookup"><span data-stu-id="d086f-132">IRPending.</span></span>
<span data-ttu-id="d086f-133">La sincronizzazione iniziale non è stata avviata e non è ancora disponibile un punto di recupero.</span><span class="sxs-lookup"><span data-stu-id="d086f-133">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="d086f-134">Protetta.</span><span class="sxs-lookup"><span data-stu-id="d086f-134">Protected.</span></span>
<span data-ttu-id="d086f-135">La protezione è in corso.</span><span class="sxs-lookup"><span data-stu-id="d086f-135">Protection is ongoing.</span></span> 
- <span data-ttu-id="d086f-136">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="d086f-136">ProtectionError.</span></span>
<span data-ttu-id="d086f-137">Si è verificato un errore di protezione.</span><span class="sxs-lookup"><span data-stu-id="d086f-137">There is a protection error.</span></span>
- <span data-ttu-id="d086f-138">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="d086f-138">ProtectionStopped.</span></span>
<span data-ttu-id="d086f-139">La protezione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="d086f-139">Protection is disabled.</span></span>

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

### <span data-ttu-id="d086f-140">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="d086f-140">-ProtectionStatus</span></span>
<span data-ttu-id="d086f-141">Specifica lo stato di protezione complessivo di un elemento nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="d086f-141">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="d086f-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d086f-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d086f-143">Sano</span><span class="sxs-lookup"><span data-stu-id="d086f-143">Healthy</span></span>
- <span data-ttu-id="d086f-144">Malsano</span><span class="sxs-lookup"><span data-stu-id="d086f-144">Unhealthy</span></span>

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

### <span data-ttu-id="d086f-145">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d086f-145">-WorkloadType</span></span>
<span data-ttu-id="d086f-146">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d086f-146">Specifies the workload type.</span></span> <span data-ttu-id="d086f-147">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d086f-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d086f-148">AzureVM</span><span class="sxs-lookup"><span data-stu-id="d086f-148">AzureVM</span></span> 
- <span data-ttu-id="d086f-149">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="d086f-149">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d086f-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d086f-150">-DefaultProfile</span></span>
<span data-ttu-id="d086f-151">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d086f-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d086f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d086f-152">CommonParameters</span></span>
<span data-ttu-id="d086f-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d086f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d086f-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d086f-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d086f-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d086f-155">INPUTS</span></span>

## <span data-ttu-id="d086f-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d086f-156">OUTPUTS</span></span>

### <span data-ttu-id="d086f-157">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="d086f-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="d086f-158">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase]</span><span class="sxs-lookup"><span data-stu-id="d086f-158">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="d086f-159">Note</span><span class="sxs-lookup"><span data-stu-id="d086f-159">NOTES</span></span>

## <span data-ttu-id="d086f-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d086f-160">RELATED LINKS</span></span>

[<span data-ttu-id="d086f-161">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d086f-161">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="d086f-162">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="d086f-162">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="d086f-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d086f-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="d086f-164">Ripristinare-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="d086f-164">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


