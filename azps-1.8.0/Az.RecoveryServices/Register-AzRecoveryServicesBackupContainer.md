---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: eeffbbd62a4c161b95004c6f4bd40d31fbd02517
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677603"
---
# <span data-ttu-id="0e744-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0e744-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="0e744-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e744-102">SYNOPSIS</span></span>
<span data-ttu-id="0e744-103">Questo comando consente a Azure Backup di convertire la risorsa in un contenitore di backup che viene quindi registrato nel Vault di servizi di ripristino specificati.</span><span class="sxs-lookup"><span data-stu-id="0e744-103">This command allows Azure Backup to convert the �Resource� to a �Backup Container� which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="0e744-104">Il servizio di backup di Azure può quindi trovare i carichi di lavoro del tipo di carico di lavoro specifico all'interno del contenitore per essere protetti in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="0e744-104">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="0e744-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e744-105">SYNTAX</span></span>

### <span data-ttu-id="0e744-106">Register (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0e744-106">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e744-107">Ripetere</span><span class="sxs-lookup"><span data-stu-id="0e744-107">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e744-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e744-108">DESCRIPTION</span></span>
<span data-ttu-id="0e744-109">Il cmdlet registra una VM di Azure per AzureWorkloads con specifiche workloadType.</span><span class="sxs-lookup"><span data-stu-id="0e744-109">The cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="0e744-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e744-110">EXAMPLES</span></span>

### <span data-ttu-id="0e744-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0e744-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="0e744-112">Il cmdlet registra una VM di Azure per il carico di lavoro MSSQL.</span><span class="sxs-lookup"><span data-stu-id="0e744-112">The cmdlet registers an azure VM for the workload MSSQL.</span></span>

## <span data-ttu-id="0e744-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e744-113">PARAMETERS</span></span>

### <span data-ttu-id="0e744-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0e744-114">-BackupManagementType</span></span>
<span data-ttu-id="0e744-115">Tipo di gestione del backup del contenitore di backup di Azure</span><span class="sxs-lookup"><span data-stu-id="0e744-115">The backup management type of the Azure Backup container</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e744-116">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="0e744-116">-Container</span></span>
<span data-ttu-id="0e744-117">Contenitore in cui si trova l'elemento</span><span class="sxs-lookup"><span data-stu-id="0e744-117">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e744-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e744-118">-DefaultProfile</span></span>
<span data-ttu-id="0e744-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e744-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e744-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0e744-120">-Force</span></span>
<span data-ttu-id="0e744-121">Force Registers container (impedisce la finestra di dialogo di conferma).</span><span class="sxs-lookup"><span data-stu-id="0e744-121">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="0e744-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0e744-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="0e744-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e744-123">-ResourceId</span></span>
<span data-ttu-id="0e744-124">ID della risorsa Azure il cui elemento rappresentativo deve essere controllato se è già protetto da qualche volta di RecoveryServices nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0e744-124">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e744-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0e744-125">-VaultId</span></span>
<span data-ttu-id="0e744-126">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0e744-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0e744-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="0e744-127">-WorkloadType</span></span>
<span data-ttu-id="0e744-128">Tipo di carico di lavoro della risorsa (ad esempio: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="0e744-128">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e744-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0e744-129">-Confirm</span></span>
<span data-ttu-id="0e744-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e744-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e744-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e744-131">-WhatIf</span></span>
<span data-ttu-id="0e744-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e744-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e744-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e744-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e744-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e744-134">CommonParameters</span></span>
<span data-ttu-id="0e744-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e744-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e744-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e744-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e744-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e744-137">INPUTS</span></span>

### <span data-ttu-id="0e744-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0e744-138">System.String</span></span>

## <span data-ttu-id="0e744-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e744-139">OUTPUTS</span></span>

### <span data-ttu-id="0e744-140">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="0e744-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="0e744-141">Note</span><span class="sxs-lookup"><span data-stu-id="0e744-141">NOTES</span></span>

## <span data-ttu-id="0e744-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e744-142">RELATED LINKS</span></span>