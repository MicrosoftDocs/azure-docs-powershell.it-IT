---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: e9559993e122e5b713228630b3b783b1f0e6a981
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005838"
---
# <span data-ttu-id="94ad4-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="94ad4-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="94ad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="94ad4-103">Recupera i criteri di replica asr.</span><span class="sxs-lookup"><span data-stu-id="94ad4-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="94ad4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94ad4-104">SYNTAX</span></span>

### <span data-ttu-id="94ad4-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94ad4-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94ad4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="94ad4-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94ad4-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="94ad4-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94ad4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94ad4-108">DESCRIPTION</span></span>
<span data-ttu-id="94ad4-109">Il cmdlet **Get-AzRecoveryServicesAsrPolicy** ottiene l'elenco dei criteri di replica di Azure Site Recovery configurati o uno specifico criterio di replica in base al nome.</span><span class="sxs-lookup"><span data-stu-id="94ad4-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="94ad4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94ad4-110">EXAMPLES</span></span>

### <span data-ttu-id="94ad4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94ad4-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="94ad4-112">restituisce l'elenco dei criteri di replica</span><span class="sxs-lookup"><span data-stu-id="94ad4-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="94ad4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="94ad4-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="94ad4-114">Restituisce i criteri di replica con nome.</span><span class="sxs-lookup"><span data-stu-id="94ad4-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="94ad4-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="94ad4-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="94ad4-116">Restituisce i criteri di replica con il nome descrittivo specificato.</span><span class="sxs-lookup"><span data-stu-id="94ad4-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="94ad4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94ad4-117">PARAMETERS</span></span>

### <span data-ttu-id="94ad4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ad4-118">-DefaultProfile</span></span>
<span data-ttu-id="94ad4-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94ad4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="94ad4-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="94ad4-120">-FriendlyName</span></span>
<span data-ttu-id="94ad4-121">Specifica il nome descrittivo del criterio di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="94ad4-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ad4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="94ad4-122">-Name</span></span>
<span data-ttu-id="94ad4-123">Specifica il nome del criterio di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="94ad4-123">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ad4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ad4-124">CommonParameters</span></span>
<span data-ttu-id="94ad4-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ad4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ad4-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94ad4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ad4-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="94ad4-127">INPUTS</span></span>

### <span data-ttu-id="94ad4-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="94ad4-128">None</span></span>

## <span data-ttu-id="94ad4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94ad4-129">OUTPUTS</span></span>

### <span data-ttu-id="94ad4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="94ad4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="94ad4-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="94ad4-131">NOTES</span></span>

## <span data-ttu-id="94ad4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94ad4-132">RELATED LINKS</span></span>

[<span data-ttu-id="94ad4-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="94ad4-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="94ad4-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="94ad4-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
