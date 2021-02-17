---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 65c9bca6eb678ff3f3cb0a61d815f8415c715e43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200350"
---
# <span data-ttu-id="639f8-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="639f8-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="639f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="639f8-102">SYNOPSIS</span></span>
<span data-ttu-id="639f8-103">Disabilitare HTTPS per un dominio personalizzato</span><span class="sxs-lookup"><span data-stu-id="639f8-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="639f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="639f8-104">SYNTAX</span></span>

### <span data-ttu-id="639f8-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="639f8-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="639f8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="639f8-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="639f8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="639f8-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="639f8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="639f8-108">DESCRIPTION</span></span>
<span data-ttu-id="639f8-109">**Disable-AzFrontDoorCustomDomainHttps** disabilita HTTPS per un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="639f8-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="639f8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="639f8-110">EXAMPLES</span></span>

### <span data-ttu-id="639f8-111">Esempio 1: Disabilitare HTTPS per un dominio personalizzato con FrontDoorName e ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="639f8-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="639f8-112">Disabilitare HTTPS per un dominio personalizzato "frontendpointname1-custom-xyz" con FrontDoorName come "frontdoor1" e ResourceGroupName come "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="639f8-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="639f8-113">Esempio 2: Disabilitare HTTPS per un dominio personalizzato con oggetto PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="639f8-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Disable-AzFrontDoorCustomDomainHttps -InputObject $frontendEndpointObj 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="639f8-114">Disabilitare HTTPS per un dominio personalizzato con oggetto PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="639f8-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="639f8-115">Esempio 3: Disabilitare HTTPS per un dominio personalizzato con ResourceId.</span><span class="sxs-lookup"><span data-stu-id="639f8-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
```powershell
PS C:\> Disable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId 

HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Disabling
CustomHttpsProvisioningSubstate  : DeletingCertificate
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
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

<span data-ttu-id="639f8-116">Disabilitare HTTPS per un dominio personalizzato "frontendpointname1-custom-xyz" con ResourceId come $resourceId.</span><span class="sxs-lookup"><span data-stu-id="639f8-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="639f8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="639f8-117">PARAMETERS</span></span>

### <span data-ttu-id="639f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="639f8-118">-DefaultProfile</span></span>
<span data-ttu-id="639f8-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="639f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="639f8-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="639f8-120">-FrontDoorName</span></span>
<span data-ttu-id="639f8-121">Il nome della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="639f8-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="639f8-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="639f8-122">-FrontendEndpointName</span></span>
<span data-ttu-id="639f8-123">Nome dell'endpoint frontend.</span><span class="sxs-lookup"><span data-stu-id="639f8-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="639f8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="639f8-124">-InputObject</span></span>
<span data-ttu-id="639f8-125">Oggetto endpoint Frontend da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="639f8-125">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="639f8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="639f8-126">-ResourceGroupName</span></span>
<span data-ttu-id="639f8-127">Gruppo di risorse a cui appartiene la porta davanti.</span><span class="sxs-lookup"><span data-stu-id="639f8-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="639f8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="639f8-128">-ResourceId</span></span>
<span data-ttu-id="639f8-129">ID risorsa dell'endpoint Front Door per disabilitare https</span><span class="sxs-lookup"><span data-stu-id="639f8-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="639f8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="639f8-130">-Confirm</span></span>
<span data-ttu-id="639f8-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="639f8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="639f8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="639f8-132">-WhatIf</span></span>
<span data-ttu-id="639f8-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="639f8-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="639f8-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="639f8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="639f8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="639f8-135">CommonParameters</span></span>
<span data-ttu-id="639f8-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="639f8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="639f8-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="639f8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="639f8-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="639f8-138">INPUTS</span></span>

### <span data-ttu-id="639f8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="639f8-139">System.String</span></span>

## <span data-ttu-id="639f8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="639f8-140">OUTPUTS</span></span>

### <span data-ttu-id="639f8-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="639f8-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="639f8-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="639f8-142">NOTES</span></span>

## <span data-ttu-id="639f8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="639f8-143">RELATED LINKS</span></span>
