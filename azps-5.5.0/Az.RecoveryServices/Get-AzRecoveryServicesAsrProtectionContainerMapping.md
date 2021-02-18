---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7d3b5735cc52ae190cc16c93ad9806a9f47b452d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193023"
---
# <span data-ttu-id="17f2f-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="17f2f-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="17f2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="17f2f-103">Ottiene i mapping del contenitore di protezione di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="17f2f-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="17f2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17f2f-104">SYNTAX</span></span>

### <span data-ttu-id="17f2f-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17f2f-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17f2f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="17f2f-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17f2f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="17f2f-107">DESCRIPTION</span></span>
<span data-ttu-id="17f2f-108">Il cmdlet **Get-AzRecoveryServicesAsrProtectionContainerMapping** ottiene informazioni sul contenitore di protezione ai mapping dei criteri di replica (associazione) nel vault per il contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="17f2f-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="17f2f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17f2f-109">EXAMPLES</span></span>

### <span data-ttu-id="17f2f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17f2f-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="17f2f-111">Elenco di mapping dei contenitori di protezione per il contenitore.</span><span class="sxs-lookup"><span data-stu-id="17f2f-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="17f2f-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="17f2f-112">Example 2</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container -Name $PrimaryProtectionContainerMapping

Name                                  : pcmmapping
ID                                    : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replica
                                        tionProtectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectionContainerMappings/pcmmapping
Health                                : Normal
HealthErrorDetails                    : {}
PolicyFriendlyName                    : V2aTestPolicy
PolicyId                              : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationPolicies/V2aTestPolicy
SourceFabricFriendlyName              : V2A-W2K12-400
SourceProtectionContainerFriendlyName : V2A-W2K12-400
State                                 : Paired
TargetFabricFriendlyName              : Microsoft Azure
TargetProtectionContainerFriendlyName : Microsoft Azure
TargetProtectionContainerId           : Microsoft Azure
```

<span data-ttu-id="17f2f-113">Ottiene tutti i mapping del contenitore di protezione per il contenitore di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="17f2f-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="17f2f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17f2f-114">PARAMETERS</span></span>

### <span data-ttu-id="17f2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f2f-115">-DefaultProfile</span></span>
<span data-ttu-id="17f2f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17f2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="17f2f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="17f2f-117">-Name</span></span>
<span data-ttu-id="17f2f-118">Specifica il nome del mapping del contenitore di protezione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="17f2f-118">Specifies the name of the protection container mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17f2f-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="17f2f-119">-ProtectionContainer</span></span>
<span data-ttu-id="17f2f-120">Ottenere mapping del contenitore di protezione corrispondenti all'oggetto contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="17f2f-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17f2f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f2f-121">CommonParameters</span></span>
<span data-ttu-id="17f2f-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f2f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f2f-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="17f2f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f2f-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="17f2f-124">INPUTS</span></span>

### <span data-ttu-id="17f2f-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="17f2f-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="17f2f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17f2f-126">OUTPUTS</span></span>

### <span data-ttu-id="17f2f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="17f2f-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="17f2f-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="17f2f-128">NOTES</span></span>

## <span data-ttu-id="17f2f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17f2f-129">RELATED LINKS</span></span>

[<span data-ttu-id="17f2f-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="17f2f-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="17f2f-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="17f2f-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)
