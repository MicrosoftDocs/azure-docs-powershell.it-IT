---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c871d8620e8c4507ec972f3888babfd259ede172
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192871"
---
# <span data-ttu-id="e11dd-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e11dd-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="e11dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e11dd-102">SYNOPSIS</span></span>
<span data-ttu-id="e11dd-103">Crea un mapping del contenitore di Azure Site Recovery Protection associando i criteri di replica specificati al contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="e11dd-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="e11dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e11dd-104">SYNTAX</span></span>

### <span data-ttu-id="e11dd-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e11dd-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e11dd-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="e11dd-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e11dd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e11dd-107">DESCRIPTION</span></span>
<span data-ttu-id="e11dd-108">Il cmdlet **New-AzRecoveryServicesAsrProtectionContainerMapping** crea un mapping del contenitore di protezione di Azure Site Recovery associando i criteri di replica specificati al contenitore di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="e11dd-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="e11dd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e11dd-109">EXAMPLES</span></span>

### <span data-ttu-id="e11dd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e11dd-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="e11dd-111">Avvia la creazione del mapping del contenitore di protezione con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e11dd-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="e11dd-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e11dd-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="e11dd-113">Avvia la creazione del mapping del contenitore di protezione con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e11dd-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e11dd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e11dd-114">PARAMETERS</span></span>

### <span data-ttu-id="e11dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e11dd-115">-DefaultProfile</span></span>
<span data-ttu-id="e11dd-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e11dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e11dd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e11dd-117">-Name</span></span>
<span data-ttu-id="e11dd-118">Specifica il nome del mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="e11dd-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="e11dd-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="e11dd-119">-Policy</span></span>
<span data-ttu-id="e11dd-120">Specifica l'oggetto criterio di replica ASR per il criterio di replica da usare nel mapping.</span><span class="sxs-lookup"><span data-stu-id="e11dd-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e11dd-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e11dd-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="e11dd-122">Specifica l'oggetto contenitore di protezione ASR per il contenitore di protezione principale da usare nel mapping.</span><span class="sxs-lookup"><span data-stu-id="e11dd-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e11dd-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e11dd-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="e11dd-124">Specifica l'oggetto contenitore di protezione ASR per il contenitore di protezione di ripristino da usare nel mapping (usato se si replica in una posizione di ripristino diversa da Azure).</span><span class="sxs-lookup"><span data-stu-id="e11dd-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e11dd-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e11dd-125">-Confirm</span></span>
<span data-ttu-id="e11dd-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e11dd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e11dd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e11dd-127">-WhatIf</span></span>
<span data-ttu-id="e11dd-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e11dd-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e11dd-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e11dd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e11dd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e11dd-130">CommonParameters</span></span>
<span data-ttu-id="e11dd-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e11dd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e11dd-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e11dd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e11dd-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="e11dd-133">INPUTS</span></span>

### <span data-ttu-id="e11dd-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="e11dd-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="e11dd-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e11dd-135">OUTPUTS</span></span>

### <span data-ttu-id="e11dd-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="e11dd-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e11dd-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e11dd-137">NOTES</span></span>

## <span data-ttu-id="e11dd-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e11dd-138">RELATED LINKS</span></span>

[<span data-ttu-id="e11dd-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e11dd-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="e11dd-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e11dd-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
