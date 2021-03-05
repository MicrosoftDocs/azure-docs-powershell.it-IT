---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 5d3acb8c03ceae44024ed8c6c52a8ee962c9861c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986185"
---
# <span data-ttu-id="4ee2e-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4ee2e-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="4ee2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ee2e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee2e-103">Creare un oggetto in memoria per LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ee2e-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="4ee2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ee2e-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="4ee2e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4ee2e-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee2e-106">Creare un oggetto in memoria per LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ee2e-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="4ee2e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ee2e-107">EXAMPLES</span></span>

### <span data-ttu-id="4ee2e-108">Esempio 1: Creare un oggetto di configurazione di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="4ee2e-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="4ee2e-109">Questo comando crea un oggetto di configurazione di bilanciamento del carico usato per creare o aggiornare un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="4ee2e-110">Per altre informazioni, vedere New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="4ee2e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ee2e-111">PARAMETERS</span></span>

### <span data-ttu-id="4ee2e-112">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ee2e-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="4ee2e-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="4ee2e-114">Per creare, vedere la sezione NOTES per le proprietà FRONTENDIPCONFIGURATION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ILoadBalancerFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee2e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4ee2e-115">-Name</span></span>
<span data-ttu-id="4ee2e-116">Nome di LoadBalancerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-116">Name of LoadBalancerConfiguration.</span></span>

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

### <span data-ttu-id="4ee2e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee2e-117">CommonParameters</span></span>
<span data-ttu-id="4ee2e-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee2e-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee2e-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="4ee2e-120">INPUTS</span></span>

## <span data-ttu-id="4ee2e-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ee2e-121">OUTPUTS</span></span>

### <span data-ttu-id="4ee2e-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ee2e-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="4ee2e-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="4ee2e-123">NOTES</span></span>

<span data-ttu-id="4ee2e-124">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4ee2e-124">ALIASES</span></span>

<span data-ttu-id="4ee2e-125">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="4ee2e-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ee2e-126">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ee2e-127">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ee2e-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="4ee2e-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="4ee2e-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="4ee2e-130">`[PrivateIPAddress <String>]`: l'indirizzo IP privato a cui fa riferimento il servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="4ee2e-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="4ee2e-131">`[PublicIPAddressId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="4ee2e-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="4ee2e-132">`[SubnetId <String>]`: ID risorsa</span><span class="sxs-lookup"><span data-stu-id="4ee2e-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="4ee2e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ee2e-133">RELATED LINKS</span></span>

