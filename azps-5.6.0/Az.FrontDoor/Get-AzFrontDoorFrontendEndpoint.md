---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/get-azfrontdoorfrontendendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorFrontendEndpoint.md
ms.openlocfilehash: 2887c343c9498eb2b8bde51b51226bffc5795ff3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954702"
---
# <span data-ttu-id="e81b9-101">Get-AzFrontDoorFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="e81b9-101">Get-AzFrontDoorFrontendEndpoint</span></span>

## <span data-ttu-id="e81b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e81b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e81b9-103">Ottieni un'estremità frontale.</span><span class="sxs-lookup"><span data-stu-id="e81b9-103">Get a front door frontend endpoint.</span></span>

## <span data-ttu-id="e81b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e81b9-104">SYNTAX</span></span>

### <span data-ttu-id="e81b9-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e81b9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e81b9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e81b9-106">ByObjectParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint [-Name <String>] -FrontDoorObject <PSFrontDoor>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e81b9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e81b9-107">ByResourceIdParameterSet</span></span>
```
Get-AzFrontDoorFrontendEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e81b9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e81b9-108">DESCRIPTION</span></span>
<span data-ttu-id="e81b9-109">Il cmdlet **Get-AzFrontDoorFrontendEndpoint** ottiene tutti gli endpoint frontend esistenti nella risorsa Front Door corrente che corrispondono alle informazioni fornite.</span><span class="sxs-lookup"><span data-stu-id="e81b9-109">The **Get-AzFrontDoorFrontendEndpoint** cmdlet gets all existing frontend endpoints in the current Front Door resource that matches provided information.</span></span>

## <span data-ttu-id="e81b9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e81b9-110">EXAMPLES</span></span>

### <span data-ttu-id="e81b9-111">Esempio 1: Ottenere tutti gli endpoint frontend in Front Door "frontdoor1", che fa parte del gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="e81b9-111">Example 1: Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontendpointname1-custom-xyz
Name                             : frontendpointname1-custom-xyz
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="e81b9-112">Ottenere tutti gli endpoint di frontend in Front Door "frontdoor1", che fa parte del gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="e81b9-112">Get all frontend endpoints in Front Door "frontdoor1" which is part of resource group "rg1".</span></span>

### <span data-ttu-id="e81b9-113">Esempio 2: Ottenere l'endpoint frontend con il nome "frontdoor1-azurefd-net" in Front Door "frontdoor1", che fa parte del gruppo di risorse "rg1"</span><span class="sxs-lookup"><span data-stu-id="e81b9-113">Example 2: Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "rg1" -FrontDoorName "frontdoor1" -Name "frontdoor1-azurefd-net"


HostName                         : frontdoor1.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabled
CustomHttpsProvisioningSubstate  : None
CertificateSource                :
ProtocolType                     :
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    : Enabled
Id                               : /subscriptions/{guid}/resourcegroups/resourcegroup1
                                   /providers/Microsoft.Network/frontdoors/frontdoor1/frontendendpoints/frontdoor1-azurefd-net
Name                             : frontdoor1-azurefd-net
Type                             : Microsoft.Network/frontdoors/frontendendpoints
```

<span data-ttu-id="e81b9-114">Ottenere l'endpoint di frontend con il nome "frontdoor1-azurefd-net" in Front Door "frontdoor1", che fa parte del gruppo di risorse "rg1"</span><span class="sxs-lookup"><span data-stu-id="e81b9-114">Get frontend endpoint with name "frontdoor1-azurefd-net" in Front Door "frontdoor1" which is part of resource group "rg1"</span></span>

## <span data-ttu-id="e81b9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e81b9-115">PARAMETERS</span></span>

### <span data-ttu-id="e81b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81b9-116">-DefaultProfile</span></span>
<span data-ttu-id="e81b9-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e81b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e81b9-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e81b9-118">-FrontDoorName</span></span>
<span data-ttu-id="e81b9-119">Nome della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="e81b9-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81b9-120">-FrontDoorObject</span><span class="sxs-lookup"><span data-stu-id="e81b9-120">-FrontDoorObject</span></span>
<span data-ttu-id="e81b9-121">Oggetto FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e81b9-121">The FrontDoor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e81b9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e81b9-122">-Name</span></span>
<span data-ttu-id="e81b9-123">Nome dell'endpoint frontend.</span><span class="sxs-lookup"><span data-stu-id="e81b9-123">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e81b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="e81b9-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e81b9-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e81b9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e81b9-126">-ResourceId</span></span>
<span data-ttu-id="e81b9-127">ID risorsa della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="e81b9-127">Resource Id of the Front Door</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81b9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81b9-128">CommonParameters</span></span>
<span data-ttu-id="e81b9-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e81b9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81b9-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e81b9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81b9-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e81b9-131">INPUTS</span></span>

### <span data-ttu-id="e81b9-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e81b9-132">None</span></span>

## <span data-ttu-id="e81b9-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e81b9-133">OUTPUTS</span></span>

### <span data-ttu-id="e81b9-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="e81b9-134">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="e81b9-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="e81b9-135">NOTES</span></span>

## <span data-ttu-id="e81b9-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e81b9-136">RELATED LINKS</span></span>
