---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9b836a4c4c056699e2c74bcb4d5b373f5bfe170e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509756"
---
# <span data-ttu-id="24daf-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="24daf-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="24daf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24daf-102">SYNOPSIS</span></span>
<span data-ttu-id="24daf-103">Ottiene gli elementi da un contenitore nel backup.</span><span class="sxs-lookup"><span data-stu-id="24daf-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24daf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24daf-104">SYNTAX</span></span>

### <span data-ttu-id="24daf-105">GetItemsForContainer (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24daf-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24daf-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="24daf-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24daf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24daf-107">DESCRIPTION</span></span>
<span data-ttu-id="24daf-108">Il cmdlet **Get-AzureRmRecoveryServicesBackupItem** ottiene gli elementi in un contenitore o un valore in Azure Backup e lo stato di protezione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="24daf-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="24daf-109">Un contenitore registrato in un Vault di servizi di ripristino di Azure può avere uno o più elementi che possono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="24daf-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="24daf-110">Per le macchine virtuali di Azure può essere presente un solo elemento di backup nel contenitore della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="24daf-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="24daf-111">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="24daf-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="24daf-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24daf-112">EXAMPLES</span></span>

### <span data-ttu-id="24daf-113">Esempio 1: ottenere un elemento da un contenitore di backup</span><span class="sxs-lookup"><span data-stu-id="24daf-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="24daf-114">Il primo comando ottiene il contenitore di tipo AzureVM e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="24daf-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="24daf-115">Il secondo comando ottiene l'elemento di backup denominato V2VM in $Container e lo archivia nella variabile $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="24daf-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="24daf-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24daf-116">PARAMETERS</span></span>

### <span data-ttu-id="24daf-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="24daf-117">-BackupManagementType</span></span>
<span data-ttu-id="24daf-118">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="24daf-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="24daf-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="24daf-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24daf-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="24daf-120">AzureVM</span></span> 
- <span data-ttu-id="24daf-121">Marte</span><span class="sxs-lookup"><span data-stu-id="24daf-121">MARS</span></span> 
- <span data-ttu-id="24daf-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="24daf-122">SCDPM</span></span> 
- <span data-ttu-id="24daf-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="24daf-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24daf-124">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="24daf-124">-Container</span></span>
<span data-ttu-id="24daf-125">Specifica un oggetto contenitore da cui questo cmdlet ottiene gli elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="24daf-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="24daf-126">Per ottenere un **AzureRmRecoveryServicesBackupContainer** , usare il cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="24daf-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: GetItemsForContainer
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24daf-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24daf-127">-DefaultProfile</span></span>
<span data-ttu-id="24daf-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24daf-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24daf-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="24daf-129">-Name</span></span>
<span data-ttu-id="24daf-130">Specifica il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="24daf-130">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24daf-131">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="24daf-131">-ProtectionState</span></span>
<span data-ttu-id="24daf-132">Specifica lo stato di protezione.</span><span class="sxs-lookup"><span data-stu-id="24daf-132">Specifies the state of protection.</span></span>
<span data-ttu-id="24daf-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="24daf-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24daf-134">IRPending.</span><span class="sxs-lookup"><span data-stu-id="24daf-134">IRPending.</span></span>
<span data-ttu-id="24daf-135">La sincronizzazione iniziale non è stata avviata e non è ancora disponibile un punto di recupero.</span><span class="sxs-lookup"><span data-stu-id="24daf-135">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="24daf-136">Protetta.</span><span class="sxs-lookup"><span data-stu-id="24daf-136">Protected.</span></span>
<span data-ttu-id="24daf-137">La protezione è in corso.</span><span class="sxs-lookup"><span data-stu-id="24daf-137">Protection is ongoing.</span></span> 
- <span data-ttu-id="24daf-138">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="24daf-138">ProtectionError.</span></span>
<span data-ttu-id="24daf-139">Si è verificato un errore di protezione.</span><span class="sxs-lookup"><span data-stu-id="24daf-139">There is a protection error.</span></span>
- <span data-ttu-id="24daf-140">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="24daf-140">ProtectionStopped.</span></span>
<span data-ttu-id="24daf-141">La protezione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="24daf-141">Protection is disabled.</span></span>

```yaml
Type: ItemProtectionState
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24daf-142">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="24daf-142">-ProtectionStatus</span></span>
<span data-ttu-id="24daf-143">Specifica lo stato di protezione complessivo di un elemento nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="24daf-143">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="24daf-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="24daf-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24daf-145">Sano</span><span class="sxs-lookup"><span data-stu-id="24daf-145">Healthy</span></span>
- <span data-ttu-id="24daf-146">Malsano</span><span class="sxs-lookup"><span data-stu-id="24daf-146">Unhealthy</span></span>

```yaml
Type: ItemProtectionStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24daf-147">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="24daf-147">-WorkloadType</span></span>
<span data-ttu-id="24daf-148">Specifica il tipo di carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="24daf-148">Specifies the workload type.</span></span> <span data-ttu-id="24daf-149">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="24daf-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="24daf-150">AzureVM</span><span class="sxs-lookup"><span data-stu-id="24daf-150">AzureVM</span></span> 
- <span data-ttu-id="24daf-151">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="24daf-151">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24daf-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24daf-152">CommonParameters</span></span>
<span data-ttu-id="24daf-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24daf-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24daf-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24daf-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24daf-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24daf-155">INPUTS</span></span>

### <span data-ttu-id="24daf-156">Nessuno</span><span class="sxs-lookup"><span data-stu-id="24daf-156">None</span></span>
<span data-ttu-id="24daf-157">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="24daf-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24daf-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24daf-158">OUTPUTS</span></span>

### <span data-ttu-id="24daf-159">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="24daf-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="24daf-160">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase]</span><span class="sxs-lookup"><span data-stu-id="24daf-160">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="24daf-161">Note</span><span class="sxs-lookup"><span data-stu-id="24daf-161">NOTES</span></span>

## <span data-ttu-id="24daf-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24daf-162">RELATED LINKS</span></span>

[<span data-ttu-id="24daf-163">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="24daf-163">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="24daf-164">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="24daf-164">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="24daf-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="24daf-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="24daf-166">Ripristinare-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="24daf-166">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


