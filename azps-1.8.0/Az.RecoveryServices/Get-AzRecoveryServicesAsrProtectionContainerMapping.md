---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 588c00dc877c4e451a4d8a0c0b44ec001b0787ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677688"
---
# <span data-ttu-id="439cc-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="439cc-101">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="439cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="439cc-102">SYNOPSIS</span></span>
<span data-ttu-id="439cc-103">Ottiene i mapping del contenitore di protezione del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="439cc-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

## <span data-ttu-id="439cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="439cc-104">SYNTAX</span></span>

### <span data-ttu-id="439cc-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="439cc-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="439cc-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="439cc-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="439cc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="439cc-107">DESCRIPTION</span></span>
<span data-ttu-id="439cc-108">Il cmdlet **Get-AzRecoveryServicesAsrProtectionContainerMapping** ottiene le informazioni sul contenitore di protezione per i mapping dei criteri di replica (Association) nel Vault per il contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="439cc-108">The **Get-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="439cc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="439cc-109">EXAMPLES</span></span>

### <span data-ttu-id="439cc-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="439cc-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="439cc-111">Elenco di mapping dei contenitori di protezione per container.</span><span class="sxs-lookup"><span data-stu-id="439cc-111">List of protection container mappings for container.</span></span>

### <span data-ttu-id="439cc-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="439cc-112">Example 2</span></span>
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

<span data-ttu-id="439cc-113">Ottiene tutti i mapping dei contenitori di protezione per il contenitore di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="439cc-113">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="439cc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="439cc-114">PARAMETERS</span></span>

### <span data-ttu-id="439cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439cc-115">-DefaultProfile</span></span>
<span data-ttu-id="439cc-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="439cc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="439cc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="439cc-117">-Name</span></span>
<span data-ttu-id="439cc-118">Specifica il nome del mapping del contenitore di protezione da ottenere.</span><span class="sxs-lookup"><span data-stu-id="439cc-118">Specifies the name of the protection container mapping to get.</span></span>

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

### <span data-ttu-id="439cc-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="439cc-119">-ProtectionContainer</span></span>
<span data-ttu-id="439cc-120">Ottenere mapping contenitore di protezione corrispondente all'oggetto contenitore di protezione ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="439cc-120">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

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

### <span data-ttu-id="439cc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439cc-121">CommonParameters</span></span>
<span data-ttu-id="439cc-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="439cc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439cc-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="439cc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439cc-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="439cc-124">INPUTS</span></span>

### <span data-ttu-id="439cc-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="439cc-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="439cc-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="439cc-126">OUTPUTS</span></span>

### <span data-ttu-id="439cc-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="439cc-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="439cc-128">Note</span><span class="sxs-lookup"><span data-stu-id="439cc-128">NOTES</span></span>

## <span data-ttu-id="439cc-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="439cc-129">RELATED LINKS</span></span>

[<span data-ttu-id="439cc-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="439cc-130">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="439cc-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="439cc-131">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)