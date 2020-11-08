---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a7cd359714be965c232019310ac2f2abfe0fe233
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018574"
---
# <span data-ttu-id="cfaa5-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cfaa5-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="cfaa5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cfaa5-102">SYNOPSIS</span></span>
<span data-ttu-id="cfaa5-103">Ottiene i criteri di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="cfaa5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfaa5-104">SYNTAX</span></span>

### <span data-ttu-id="cfaa5-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfaa5-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfaa5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cfaa5-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfaa5-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="cfaa5-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfaa5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfaa5-108">DESCRIPTION</span></span>
<span data-ttu-id="cfaa5-109">Il cmdlet **Get-AzRecoveryServicesAsrPolicy** Ottiene l'elenco dei criteri di replica del ripristino del sito Azure configurati o di un criterio di replica specifico per nome.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="cfaa5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfaa5-110">EXAMPLES</span></span>

### <span data-ttu-id="cfaa5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cfaa5-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="cfaa5-112">Restituisce l'elenco dei criteri di replica</span><span class="sxs-lookup"><span data-stu-id="cfaa5-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="cfaa5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cfaa5-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="cfaa5-114">Restituisce i criteri di replica con nome.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="cfaa5-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="cfaa5-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="cfaa5-116">Restituisce i criteri di replica con il nome descrittivo specificato.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="cfaa5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cfaa5-117">PARAMETERS</span></span>

### <span data-ttu-id="cfaa5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfaa5-118">-DefaultProfile</span></span>
<span data-ttu-id="cfaa5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cfaa5-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cfaa5-120">-FriendlyName</span></span>
<span data-ttu-id="cfaa5-121">Specifica il nome descrittivo dei criteri di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="cfaa5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfaa5-122">-Name</span></span>
<span data-ttu-id="cfaa5-123">Specifica il nome del criterio di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="cfaa5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfaa5-124">CommonParameters</span></span>
<span data-ttu-id="cfaa5-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfaa5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfaa5-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfaa5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfaa5-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cfaa5-127">INPUTS</span></span>

### <span data-ttu-id="cfaa5-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cfaa5-128">None</span></span>

## <span data-ttu-id="cfaa5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfaa5-129">OUTPUTS</span></span>

### <span data-ttu-id="cfaa5-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="cfaa5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="cfaa5-131">Note</span><span class="sxs-lookup"><span data-stu-id="cfaa5-131">NOTES</span></span>

## <span data-ttu-id="cfaa5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfaa5-132">RELATED LINKS</span></span>

[<span data-ttu-id="cfaa5-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cfaa5-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="cfaa5-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="cfaa5-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
