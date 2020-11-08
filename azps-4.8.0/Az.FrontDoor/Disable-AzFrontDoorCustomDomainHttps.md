---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/disable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Disable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 65c9bca6eb678ff3f3cb0a61d815f8415c715e43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192487"
---
# <span data-ttu-id="14efd-101">Disable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="14efd-101">Disable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="14efd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14efd-102">SYNOPSIS</span></span>
<span data-ttu-id="14efd-103">Disabilitare HTTPS per un dominio personalizzato</span><span class="sxs-lookup"><span data-stu-id="14efd-103">Disable HTTPS for a custom domain</span></span>

## <span data-ttu-id="14efd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14efd-104">SYNTAX</span></span>

### <span data-ttu-id="14efd-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14efd-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14efd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14efd-106">ByResourceIdParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14efd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14efd-107">ByObjectParameterSet</span></span>
```
Disable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14efd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14efd-108">DESCRIPTION</span></span>
<span data-ttu-id="14efd-109">Il **Disable-AzFrontDoorCustomDomainHttps Disabilita** HTTPS per un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="14efd-109">The **Disable-AzFrontDoorCustomDomainHttps** disables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="14efd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14efd-110">EXAMPLES</span></span>

### <span data-ttu-id="14efd-111">Esempio 1: disabilitare HTTPS per un dominio personalizzato con FrontDoorName e ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="14efd-111">Example 1: Disable HTTPS for a custom domain with FrontDoorName and ResourceGroupName.</span></span>
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

<span data-ttu-id="14efd-112">Disabilitare HTTPS per un dominio personalizzato "frontendpointname1-Custom-XYZ" con FrontDoorName come "frontdoor1" e ResourceGroupName come "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="14efd-112">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with FrontDoorName as "frontdoor1" and ResourceGroupName as "resourcegroup1".</span></span>

### <span data-ttu-id="14efd-113">Esempio 2: disabilitare HTTPS per un dominio personalizzato con l'oggetto PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="14efd-113">Example 2: Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>
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

<span data-ttu-id="14efd-114">Disabilitare HTTPS per un dominio personalizzato con l'oggetto PSFrontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="14efd-114">Disable HTTPS for a custom domain with PSFrontendEndpoint object.</span></span>

### <span data-ttu-id="14efd-115">Esempio 3: disabilitare HTTPS per un dominio personalizzato con ResourceId.</span><span class="sxs-lookup"><span data-stu-id="14efd-115">Example 3: Disable HTTPS for a custom domain with ResourceId.</span></span>
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

<span data-ttu-id="14efd-116">Disabilitare HTTPS per un dominio personalizzato "frontendpointname1-Custom-XYZ" con ResourceId come $resourceId.</span><span class="sxs-lookup"><span data-stu-id="14efd-116">Disable HTTPS for a custom domain "frontendpointname1-custom-xyz" with ResourceId as $resourceId.</span></span>

## <span data-ttu-id="14efd-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14efd-117">PARAMETERS</span></span>

### <span data-ttu-id="14efd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14efd-118">-DefaultProfile</span></span>
<span data-ttu-id="14efd-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14efd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14efd-120">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="14efd-120">-FrontDoorName</span></span>
<span data-ttu-id="14efd-121">Il nome della porta d'ingresso.</span><span class="sxs-lookup"><span data-stu-id="14efd-121">The name of the Front Door.</span></span>

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

### <span data-ttu-id="14efd-122">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="14efd-122">-FrontendEndpointName</span></span>
<span data-ttu-id="14efd-123">Nome endpoint frontend.</span><span class="sxs-lookup"><span data-stu-id="14efd-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="14efd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14efd-124">-InputObject</span></span>
<span data-ttu-id="14efd-125">L'oggetto endpoint frontend da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="14efd-125">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="14efd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14efd-126">-ResourceGroupName</span></span>
<span data-ttu-id="14efd-127">Gruppo di risorse a cui appartiene la porta principale.</span><span class="sxs-lookup"><span data-stu-id="14efd-127">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="14efd-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14efd-128">-ResourceId</span></span>
<span data-ttu-id="14efd-129">ID risorsa dell'endpoint della porta principale per disabilitare https</span><span class="sxs-lookup"><span data-stu-id="14efd-129">Resource Id of the Front Door endpoint to disable https</span></span>

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

### <span data-ttu-id="14efd-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="14efd-130">-Confirm</span></span>
<span data-ttu-id="14efd-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14efd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14efd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14efd-132">-WhatIf</span></span>
<span data-ttu-id="14efd-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14efd-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14efd-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14efd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14efd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14efd-135">CommonParameters</span></span>
<span data-ttu-id="14efd-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14efd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14efd-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14efd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14efd-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14efd-138">INPUTS</span></span>

### <span data-ttu-id="14efd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="14efd-139">System.String</span></span>

## <span data-ttu-id="14efd-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14efd-140">OUTPUTS</span></span>

### <span data-ttu-id="14efd-141">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="14efd-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="14efd-142">Note</span><span class="sxs-lookup"><span data-stu-id="14efd-142">NOTES</span></span>

## <span data-ttu-id="14efd-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14efd-143">RELATED LINKS</span></span>