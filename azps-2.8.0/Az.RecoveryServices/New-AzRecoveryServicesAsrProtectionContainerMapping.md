---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 67cf974faa735bc8d07703094d9afe71127c7137
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855970"
---
# <span data-ttu-id="55dc1-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="55dc1-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="55dc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="55dc1-103">Crea un mapping del contenitore di protezione del ripristino di Azure site associando i criteri di replica specificati al contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="55dc1-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="55dc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55dc1-104">SYNTAX</span></span>

### <span data-ttu-id="55dc1-105">EnterpriseToAzure (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55dc1-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55dc1-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="55dc1-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55dc1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55dc1-107">DESCRIPTION</span></span>
<span data-ttu-id="55dc1-108">Il cmdlet **New-AzRecoveryServicesAsrProtectionContainerMapping** crea un mapping del contenitore di protezione del ripristino di Azure site associando i criteri di replica specificati al contenitore di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="55dc1-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="55dc1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55dc1-109">EXAMPLES</span></span>

### <span data-ttu-id="55dc1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="55dc1-110">Example 1</span></span>
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

<span data-ttu-id="55dc1-111">Avvia la creazione del mapping del contenitore di protezione con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="55dc1-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="55dc1-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="55dc1-112">Example 2</span></span>
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

<span data-ttu-id="55dc1-113">Avvia la creazione del mapping del contenitore di protezione con i parametri specificati e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="55dc1-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="55dc1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55dc1-114">PARAMETERS</span></span>

### <span data-ttu-id="55dc1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55dc1-115">-DefaultProfile</span></span>
<span data-ttu-id="55dc1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55dc1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="55dc1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="55dc1-117">-Name</span></span>
<span data-ttu-id="55dc1-118">Specifica il nome del mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="55dc1-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="55dc1-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="55dc1-119">-Policy</span></span>
<span data-ttu-id="55dc1-120">Specifica l'oggetto Criteri di replica ASR per il criterio di replica da usare nel mapping.</span><span class="sxs-lookup"><span data-stu-id="55dc1-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

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

### <span data-ttu-id="55dc1-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="55dc1-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="55dc1-122">Specifica l'oggetto contenitore di protezione ASR per il contenitore di protezione principale da usare nel mapping.</span><span class="sxs-lookup"><span data-stu-id="55dc1-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

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

### <span data-ttu-id="55dc1-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="55dc1-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="55dc1-124">Specifica l'oggetto contenitore di protezione ASR per il contenitore di protezione ripristino da usare nel mapping (usato se viene replicato in una posizione di ripristino che non è Azure).</span><span class="sxs-lookup"><span data-stu-id="55dc1-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

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

### <span data-ttu-id="55dc1-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="55dc1-125">-Confirm</span></span>
<span data-ttu-id="55dc1-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55dc1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55dc1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55dc1-127">-WhatIf</span></span>
<span data-ttu-id="55dc1-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55dc1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55dc1-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55dc1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55dc1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55dc1-130">CommonParameters</span></span>
<span data-ttu-id="55dc1-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55dc1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55dc1-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55dc1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55dc1-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55dc1-133">INPUTS</span></span>

### <span data-ttu-id="55dc1-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="55dc1-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="55dc1-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55dc1-135">OUTPUTS</span></span>

### <span data-ttu-id="55dc1-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="55dc1-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="55dc1-137">Note</span><span class="sxs-lookup"><span data-stu-id="55dc1-137">NOTES</span></span>

## <span data-ttu-id="55dc1-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55dc1-138">RELATED LINKS</span></span>

[<span data-ttu-id="55dc1-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="55dc1-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="55dc1-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="55dc1-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
