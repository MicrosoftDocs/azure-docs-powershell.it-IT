---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: aeceb76fe2f1faf6e7e1f2ddf09ee9262370e8ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518584"
---
# <span data-ttu-id="2a635-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="2a635-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="2a635-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a635-102">SYNOPSIS</span></span>
<span data-ttu-id="2a635-103">Ottiene i criteri di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="2a635-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a635-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a635-104">SYNTAX</span></span>

### <span data-ttu-id="2a635-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a635-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a635-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2a635-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a635-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2a635-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a635-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a635-108">DESCRIPTION</span></span>
<span data-ttu-id="2a635-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrPolicy** Ottiene l'elenco dei criteri di replica del ripristino del sito Azure configurati o di un criterio di replica specifico per nome.</span><span class="sxs-lookup"><span data-stu-id="2a635-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="2a635-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a635-110">EXAMPLES</span></span>

### <span data-ttu-id="2a635-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2a635-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy
```

<span data-ttu-id="2a635-112">Restituisce l'elenco dei criteri di replica</span><span class="sxs-lookup"><span data-stu-id="2a635-112">Retuns the list of replication policies</span></span>

### <span data-ttu-id="2a635-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2a635-113">Example 2</span></span>
```
PS C:\>  Get-AzureRmRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="2a635-114">Criteri di replica restituisce con nome.</span><span class="sxs-lookup"><span data-stu-id="2a635-114">Retuns replication policy with name.</span></span>

### <span data-ttu-id="2a635-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="2a635-115">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="2a635-116">Restituisce i criteri di replica con il nome descrittivo specificato.</span><span class="sxs-lookup"><span data-stu-id="2a635-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="2a635-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a635-117">PARAMETERS</span></span>

### <span data-ttu-id="2a635-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a635-118">-DefaultProfile</span></span>
<span data-ttu-id="2a635-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a635-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a635-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2a635-120">-FriendlyName</span></span>
<span data-ttu-id="2a635-121">Specifica il nome descrittivo dei criteri di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="2a635-121">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="2a635-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a635-122">-Name</span></span>
<span data-ttu-id="2a635-123">Specifica il nome del criterio di replica ASR.</span><span class="sxs-lookup"><span data-stu-id="2a635-123">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="2a635-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a635-124">CommonParameters</span></span>
<span data-ttu-id="2a635-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a635-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a635-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a635-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a635-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a635-127">INPUTS</span></span>

### <span data-ttu-id="2a635-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2a635-128">None</span></span>

## <span data-ttu-id="2a635-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a635-129">OUTPUTS</span></span>

### <span data-ttu-id="2a635-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2a635-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2a635-131">Note</span><span class="sxs-lookup"><span data-stu-id="2a635-131">NOTES</span></span>

## <span data-ttu-id="2a635-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a635-132">RELATED LINKS</span></span>

[<span data-ttu-id="2a635-133">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="2a635-133">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="2a635-134">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="2a635-134">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)