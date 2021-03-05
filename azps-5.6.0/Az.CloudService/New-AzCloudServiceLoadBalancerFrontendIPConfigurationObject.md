---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerFrontendIPConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
ms.openlocfilehash: 5628b7819789ba97ee56a0c69f65e371f9b35e7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986172"
---
# <span data-ttu-id="e41ea-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="e41ea-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>

## <span data-ttu-id="e41ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e41ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e41ea-103">Creare un oggetto in memoria per LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e41ea-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="e41ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e41ea-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject [-Name <String>] [-PublicIPAddressId <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e41ea-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e41ea-105">DESCRIPTION</span></span>
<span data-ttu-id="e41ea-106">Creare un oggetto in memoria per LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e41ea-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="e41ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e41ea-107">EXAMPLES</span></span>

### <span data-ttu-id="e41ea-108">Esempio 1: Creare un oggetto di configurazione IP frontend di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="e41ea-108">Example 1: Create load balancer frontend IP configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="e41ea-109">Questo comando crea un oggetto configurazione IP frontend di bilanciamento del carico usato per creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="e41ea-109">This command creates load balancer frontend IP configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="e41ea-110">Per altre informazioni, vedere New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="e41ea-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="e41ea-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e41ea-111">PARAMETERS</span></span>

### <span data-ttu-id="e41ea-112">-Name</span><span class="sxs-lookup"><span data-stu-id="e41ea-112">-Name</span></span>
<span data-ttu-id="e41ea-113">Nome di FrontendIpConfigration.</span><span class="sxs-lookup"><span data-stu-id="e41ea-113">Name of FrontendIpConfigration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e41ea-114">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="e41ea-114">-PublicIPAddressId</span></span>
<span data-ttu-id="e41ea-115">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e41ea-115">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e41ea-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e41ea-116">CommonParameters</span></span>
<span data-ttu-id="e41ea-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e41ea-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e41ea-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e41ea-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e41ea-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="e41ea-119">INPUTS</span></span>

## <span data-ttu-id="e41ea-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e41ea-120">OUTPUTS</span></span>

### <span data-ttu-id="e41ea-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e41ea-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="e41ea-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="e41ea-122">NOTES</span></span>

<span data-ttu-id="e41ea-123">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e41ea-123">ALIASES</span></span>

## <span data-ttu-id="e41ea-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e41ea-124">RELATED LINKS</span></span>

