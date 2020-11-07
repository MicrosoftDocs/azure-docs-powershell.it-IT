---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 1f67da2d15aca003853bcb21846535bad4e2a066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677634"
---
# <span data-ttu-id="8e880-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="8e880-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="8e880-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e880-102">SYNOPSIS</span></span>
<span data-ttu-id="8e880-103">Crea un oggetto di mapping del disco per i dischi di una macchina virtuale Azure da replicare.</span><span class="sxs-lookup"><span data-stu-id="8e880-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="8e880-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e880-104">SYNTAX</span></span>

### <span data-ttu-id="8e880-105">AzureToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e880-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e880-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8e880-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e880-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e880-107">DESCRIPTION</span></span>
<span data-ttu-id="8e880-108">Crea un oggetto di mapping del disco che esegue il mapping di un disco di una macchina virtuale di Azure all'account di archiviazione della cache e dell'account di archiviazione di destinazione (area di ripristino) da usare per replicare il disco.</span><span class="sxs-lookup"><span data-stu-id="8e880-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="8e880-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e880-109">EXAMPLES</span></span>

### <span data-ttu-id="8e880-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8e880-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="8e880-111">Creare un oggetto di mapping del disco per i dischi di una macchina virtuale di Azure da replicare. Usato durante Azure in Azure per abilitare e proteggere l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8e880-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="8e880-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e880-112">PARAMETERS</span></span>

### <span data-ttu-id="8e880-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e880-113">-DefaultProfile</span></span>
<span data-ttu-id="8e880-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e880-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e880-115">-DiskID</span><span class="sxs-lookup"><span data-stu-id="8e880-115">-DiskId</span></span>
<span data-ttu-id="8e880-116">Specifica l'ID disco del disco gestito.</span><span class="sxs-lookup"><span data-stu-id="8e880-116">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e880-117">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8e880-117">-LogStorageAccountId</span></span>
<span data-ttu-id="8e880-118">Specifica l'ID dell'account di archiviazione del log o della cache da usare per archiviare i registri di replica.</span><span class="sxs-lookup"><span data-stu-id="8e880-118">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e880-119">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8e880-119">-ManagedDisk</span></span>
<span data-ttu-id="8e880-120">Specifica che l'input è per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="8e880-120">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e880-121">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8e880-121">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="8e880-122">Specifica l'ID dell'account di archiviazione di Azure a cui eseguire la replica.</span><span class="sxs-lookup"><span data-stu-id="8e880-122">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e880-123">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="8e880-123">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="8e880-124">Specifica il tipo di account del disco gestito replicato.</span><span class="sxs-lookup"><span data-stu-id="8e880-124">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e880-125">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8e880-125">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="8e880-126">Specifica l'ID del gruppo di risorse di recupero per il disco gestito replicato.</span><span class="sxs-lookup"><span data-stu-id="8e880-126">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e880-127">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="8e880-127">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="8e880-128">Specifica il disco di destinazione del ripristino per il disco gestito replicato.</span><span class="sxs-lookup"><span data-stu-id="8e880-128">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e880-129">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="8e880-129">-VhdUri</span></span>
<span data-ttu-id="8e880-130">Specifica l'URI VHD del disco a cui corrisponde il mapping.</span><span class="sxs-lookup"><span data-stu-id="8e880-130">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e880-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8e880-131">-Confirm</span></span>
<span data-ttu-id="8e880-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e880-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e880-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e880-133">-WhatIf</span></span>
<span data-ttu-id="8e880-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e880-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e880-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8e880-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e880-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e880-136">CommonParameters</span></span>
<span data-ttu-id="8e880-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e880-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e880-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e880-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e880-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e880-139">INPUTS</span></span>

### <span data-ttu-id="8e880-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8e880-140">None</span></span>

## <span data-ttu-id="8e880-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e880-141">OUTPUTS</span></span>

### <span data-ttu-id="8e880-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="8e880-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="8e880-143">Note</span><span class="sxs-lookup"><span data-stu-id="8e880-143">NOTES</span></span>

## <span data-ttu-id="8e880-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e880-144">RELATED LINKS</span></span>
