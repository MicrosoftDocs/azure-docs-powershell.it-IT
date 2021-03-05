---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: cb5986d7e8d467c76b64baddb5fd389eda1b5b8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013645"
---
# <span data-ttu-id="a4795-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="a4795-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="a4795-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4795-102">SYNOPSIS</span></span>
<span data-ttu-id="a4795-103">Abilitare HTTPS per un dominio personalizzato usando il certificato gestito da Front Door o il proprio certificato del Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4795-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="a4795-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4795-104">SYNTAX</span></span>

### <span data-ttu-id="a4795-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4795-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4795-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4795-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4795-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4795-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4795-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4795-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4795-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4795-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4795-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4795-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4795-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a4795-111">DESCRIPTION</span></span>
<span data-ttu-id="a4795-112">**Enable-AzFrontDoorCustomDomainHttps abilita** HTTPS per un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a4795-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="a4795-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4795-113">EXAMPLES</span></span>

### <span data-ttu-id="a4795-114">Esempio 1: Abilitare HTTPS per un dominio personalizzato con FrontDoorName e ResourceGroupName usando il certificato gestito da Front Door.</span><span class="sxs-lookup"><span data-stu-id="a4795-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -MinimumTlsVersion "1.2"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="a4795-115">Abilitare HTTPS per un dominio personalizzato "frontendpointname1-custom-xyz" che fa parte di Front Door "frontdoor1" nel gruppo di risorse "resourcegroup1" usando il certificato gestito da Front Door.</span><span class="sxs-lookup"><span data-stu-id="a4795-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="a4795-116">Esempio 2: Abilitare HTTPS per un dominio personalizzato con FrontDoorName e ResourceGroupName usando il proprio certificato nel Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="a4795-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion -MinimumTlsVersion "1.0"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.0
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

<span data-ttu-id="a4795-117">Abilitare HTTPS per un dominio personalizzato "frontendpointname1-custom-xyz" che fa parte di Front Door "frontdoor1" nel gruppo di risorse "resourcegroup1" usando il certificato gestito da Front Door.</span><span class="sxs-lookup"><span data-stu-id="a4795-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="a4795-118">Esempio 3: Abilitare HTTPS per un dominio personalizzato con oggetto PSFrontendEndpoint usando il certificato gestito da Front Door.</span><span class="sxs-lookup"><span data-stu-id="a4795-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -Name "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="a4795-119">Abilitare HTTPS per un dominio personalizzato con l'oggetto PSFrontendEndpoint usando il certificato gestito da Front Door.</span><span class="sxs-lookup"><span data-stu-id="a4795-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="a4795-120">Esempio 4: Abilitare HTTPS per un dominio personalizzato con ID risorsa usando il certificato gestito da Front Door.</span><span class="sxs-lookup"><span data-stu-id="a4795-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceId $resourceId


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : FrontDoor
ProtocolType                     : ServerNameIndication
MinimumTlsVersion                : 1.2
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

<span data-ttu-id="a4795-121">Abilitare HTTPS per un dominio personalizzato "frontendpointname1-custom-xyz" con ID $resourceId usando il certificato gestito da Front Door.</span><span class="sxs-lookup"><span data-stu-id="a4795-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="a4795-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4795-122">PARAMETERS</span></span>

### <span data-ttu-id="a4795-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4795-123">-DefaultProfile</span></span>
<span data-ttu-id="a4795-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4795-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4795-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="a4795-125">-FrontDoorName</span></span>
<span data-ttu-id="a4795-126">Il nome della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="a4795-126">The name of the Front Door.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4795-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="a4795-127">-FrontendEndpointName</span></span>
<span data-ttu-id="a4795-128">Nome dell'endpoint frontend.</span><span class="sxs-lookup"><span data-stu-id="a4795-128">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4795-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4795-129">-InputObject</span></span>
<span data-ttu-id="a4795-130">Oggetto endpoint Frontend da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="a4795-130">The Frontend endpoint object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint
Parameter Sets: ByObjectParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4795-131">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a4795-131">-MinimumTlsVersion</span></span>
<span data-ttu-id="a4795-132">La versione minima di TLS richiesta dai client per stabilire un handshake SSL con Front Door.</span><span class="sxs-lookup"><span data-stu-id="a4795-132">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="a4795-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4795-133">-ResourceGroupName</span></span>
<span data-ttu-id="a4795-134">Gruppo di risorse a cui appartiene la porta davanti.</span><span class="sxs-lookup"><span data-stu-id="a4795-134">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4795-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4795-135">-ResourceId</span></span>
<span data-ttu-id="a4795-136">ID risorsa dell'endpoint Front Door per abilitare https</span><span class="sxs-lookup"><span data-stu-id="a4795-136">Resource Id of the Front Door endpoint to enable https</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4795-137">-SecretName</span><span class="sxs-lookup"><span data-stu-id="a4795-137">-SecretName</span></span>
<span data-ttu-id="a4795-138">Nome del segreto del Vault delle chiavi che rappresenta il certificato completo PFX</span><span class="sxs-lookup"><span data-stu-id="a4795-138">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4795-139">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="a4795-139">-SecretVersion</span></span>
<span data-ttu-id="a4795-140">Versione del segreto del Vault delle chiavi che rappresenta il certificato completo PFX</span><span class="sxs-lookup"><span data-stu-id="a4795-140">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4795-141">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a4795-141">-VaultId</span></span>
<span data-ttu-id="a4795-142">ID del Vault delle chiavi che contiene il certificato SSL</span><span class="sxs-lookup"><span data-stu-id="a4795-142">The Key Vault id containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithVaultParameterSet, ByResourceIdWithVaultParameterSet, ByObjectWithVaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4795-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4795-143">-Confirm</span></span>
<span data-ttu-id="a4795-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4795-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4795-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4795-145">-WhatIf</span></span>
<span data-ttu-id="a4795-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4795-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4795-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4795-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4795-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4795-148">CommonParameters</span></span>
<span data-ttu-id="a4795-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4795-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4795-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4795-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4795-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="a4795-151">INPUTS</span></span>

### <span data-ttu-id="a4795-152">System.String</span><span class="sxs-lookup"><span data-stu-id="a4795-152">System.String</span></span>
## <span data-ttu-id="a4795-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4795-153">OUTPUTS</span></span>

### <span data-ttu-id="a4795-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="a4795-154">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="a4795-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="a4795-155">NOTES</span></span>

## <span data-ttu-id="a4795-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4795-156">RELATED LINKS</span></span>
