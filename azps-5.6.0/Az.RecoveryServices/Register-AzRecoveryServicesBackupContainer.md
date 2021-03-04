---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 83a0e4edd82bd77358df1d95b53e388bb35a9e9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953294"
---
# <span data-ttu-id="53494-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="53494-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="53494-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53494-102">SYNOPSIS</span></span>
<span data-ttu-id="53494-103">Il cmdlet **Register-AzRecoveryServicesBackupContainer** registra una macchina virtuale di Azure per AzureWorkloads con workloadType specifico.</span><span class="sxs-lookup"><span data-stu-id="53494-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="53494-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53494-104">SYNTAX</span></span>

### <span data-ttu-id="53494-105">Registra (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="53494-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53494-106">Registra di nuovo</span><span class="sxs-lookup"><span data-stu-id="53494-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53494-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="53494-107">DESCRIPTION</span></span>
<span data-ttu-id="53494-108">Questo comando consente a Backup di Azure di convertire la risorsa in un contenitore di backup che viene quindi registrato nel vault dei servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="53494-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="53494-109">Il servizio Backup di Azure può quindi individuare i carichi di lavoro del tipo di carico di lavoro specificato all'interno di questo contenitore da proteggere in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="53494-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="53494-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53494-110">EXAMPLES</span></span>

### <span data-ttu-id="53494-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53494-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="53494-112">Il cmdlet registra una macchina virtuale di Azure come contenitore per il carico di lavoro MSSQL.</span><span class="sxs-lookup"><span data-stu-id="53494-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="53494-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53494-113">PARAMETERS</span></span>

### <span data-ttu-id="53494-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="53494-114">-BackupManagementType</span></span>
<span data-ttu-id="53494-115">Classe di risorse protetta.</span><span class="sxs-lookup"><span data-stu-id="53494-115">The class of resources being protected.</span></span> <span data-ttu-id="53494-116">Attualmente il valore supportato per questo cmdlet è AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="53494-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

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

### <span data-ttu-id="53494-117">-Container</span><span class="sxs-lookup"><span data-stu-id="53494-117">-Container</span></span>
<span data-ttu-id="53494-118">Contenitore in cui si trova l'elemento</span><span class="sxs-lookup"><span data-stu-id="53494-118">Container where the item resides</span></span>

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

### <span data-ttu-id="53494-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53494-119">-DefaultProfile</span></span>
<span data-ttu-id="53494-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53494-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53494-121">-Force</span><span class="sxs-lookup"><span data-stu-id="53494-121">-Force</span></span>
<span data-ttu-id="53494-122">Forzare la registrazione del contenitore (impedisce la finestra di dialogo di conferma).</span><span class="sxs-lookup"><span data-stu-id="53494-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="53494-123">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="53494-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="53494-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53494-124">-ResourceId</span></span>
<span data-ttu-id="53494-125">ID della risorsa Azure il cui elemento rappresentativo deve essere controllato se è già protetto da un Vault dei servizi di ripristino nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="53494-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

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

### <span data-ttu-id="53494-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="53494-126">-VaultId</span></span>
<span data-ttu-id="53494-127">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="53494-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="53494-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="53494-128">-WorkloadType</span></span>
<span data-ttu-id="53494-129">Tipo di carico di lavoro della risorsa.</span><span class="sxs-lookup"><span data-stu-id="53494-129">Workload type of the resource.</span></span> <span data-ttu-id="53494-130">Il valore corrente supportato è AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="53494-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="53494-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53494-131">-Confirm</span></span>
<span data-ttu-id="53494-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53494-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53494-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53494-133">-WhatIf</span></span>
<span data-ttu-id="53494-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53494-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="53494-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53494-135">CommonParameters</span></span>
<span data-ttu-id="53494-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53494-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53494-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="53494-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53494-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="53494-138">INPUTS</span></span>

### <span data-ttu-id="53494-139">System.String</span><span class="sxs-lookup"><span data-stu-id="53494-139">System.String</span></span>

## <span data-ttu-id="53494-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53494-140">OUTPUTS</span></span>

### <span data-ttu-id="53494-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="53494-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="53494-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="53494-142">NOTES</span></span>

## <span data-ttu-id="53494-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53494-143">RELATED LINKS</span></span>
