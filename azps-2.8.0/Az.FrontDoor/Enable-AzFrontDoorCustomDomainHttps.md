---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/enable-azfrontdoorcustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Enable-AzFrontDoorCustomDomainHttps.md
ms.openlocfilehash: 6edf891d693e0c1cb2143236d12e623fdd2b4a3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674397"
---
# <span data-ttu-id="1aaba-101">Enable-AzFrontDoorCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="1aaba-101">Enable-AzFrontDoorCustomDomainHttps</span></span>

## <span data-ttu-id="1aaba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1aaba-102">SYNOPSIS</span></span>
<span data-ttu-id="1aaba-103">Abilitare HTTPS per un dominio personalizzato usando il certificato gestito da porta principale o usando un certificato di Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1aaba-103">Enable HTTPS for a custom domain using Front Door managed certificate or using own certificate from Azure Key Vault.</span></span>

## <span data-ttu-id="1aaba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1aaba-104">SYNTAX</span></span>

### <span data-ttu-id="1aaba-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1aaba-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1aaba-106">ByFieldsWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aaba-106">ByFieldsWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName <String> -FrontDoorName <String>
 -FrontendEndpointName <String> -VaultId <String> -SecretName <String> -SecretVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aaba-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aaba-107">ByResourceIdParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aaba-108">ByResourceIdWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aaba-108">ByResourceIdWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -ResourceId <String> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aaba-109">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aaba-109">ByObjectParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aaba-110">ByObjectWithVaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aaba-110">ByObjectWithVaultParameterSet</span></span>
```
Enable-AzFrontDoorCustomDomainHttps -InputObject <PSFrontendEndpoint> -VaultId <String> -SecretName <String>
 -SecretVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aaba-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1aaba-111">DESCRIPTION</span></span>
<span data-ttu-id="1aaba-112">**Enable-AzFrontDoorCustomDomainHttps** Abilita HTTPS per un dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1aaba-112">The **Enable-AzFrontDoorCustomDomainHttps** enables HTTPS for a custom domain.</span></span>

## <span data-ttu-id="1aaba-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1aaba-113">EXAMPLES</span></span>

### <span data-ttu-id="1aaba-114">Esempio 1: abilitare HTTPS per un dominio personalizzato con FrontDoorName e ResourceGroupName con il certificato gestito da porta principale.</span><span class="sxs-lookup"><span data-stu-id="1aaba-114">Example 1: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using Front Door managed certificate.</span></span>
```powershell
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz"


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
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

<span data-ttu-id="1aaba-115">Abilitare HTTPS per un dominio personalizzato "frontendpointname1-Custom-XYZ" che fa parte della porta d'ingresso "frontdoor1" nel gruppo di risorse "resourcegroup1" con il certificato gestito da porta principale.</span><span class="sxs-lookup"><span data-stu-id="1aaba-115">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="1aaba-116">Esempio 2: abilitare HTTPS per un dominio personalizzato con FrontDoorName e ResourceGroupName usando il proprio certificato in Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1aaba-116">Example 2: Enable HTTPS for a custom domain with FrontDoorName and ResourceGroupName using own certificate in Key Vault.</span></span>
```powershell
PS C:\> $vaultId = (Get-AzKeyVault -VaultName $vaultName).ResourceId
PS C:\> Enable-AzFrontDoorCustomDomainHttps -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" -Vault $vaultId -secretName $secretName -SecretVersion $secretVersion


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
CertificateSource                : AzureKeyVault
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

<span data-ttu-id="1aaba-117">Abilitare HTTPS per un dominio personalizzato "frontendpointname1-Custom-XYZ" che fa parte della porta d'ingresso "frontdoor1" nel gruppo di risorse "resourcegroup1" con il certificato gestito da porta principale.</span><span class="sxs-lookup"><span data-stu-id="1aaba-117">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" that is part of Front Door "frontdoor1" in resource group "resourcegroup1" using Front Door managed certificate.</span></span>

### <span data-ttu-id="1aaba-118">Esempio 3: abilitare HTTPS per un dominio personalizzato con l'oggetto PSFrontendEndpoint con il certificato gestito da porta principale.</span><span class="sxs-lookup"><span data-stu-id="1aaba-118">Example 3: Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>
```powershell
PS C:\> Get-AzFrontDoorFrontendEndpoint -ResourceGroupName "resourcegroup1" -FrontDoorName "frontdoor1" -FrontendEndpointName "frontendpointname1-custom-xyz" | Enable-AzFrontDoorCustomDomainHttps 


HostName                         : frontendpointname1.custom.xyz
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     : Enabling
CustomHttpsProvisioningSubstate  : SubmittingDomainControlValidationRequest
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

<span data-ttu-id="1aaba-119">Abilitare HTTPS per un dominio personalizzato con l'oggetto PSFrontendEndpoint con il certificato gestito da porta principale.</span><span class="sxs-lookup"><span data-stu-id="1aaba-119">Enable HTTPS for a custom domain with PSFrontendEndpoint object using Front Door managed certificate.</span></span>

### <span data-ttu-id="1aaba-120">Esempio 4: abilitare HTTPS per un dominio personalizzato con ID risorsa con certificato gestito da porta principale.</span><span class="sxs-lookup"><span data-stu-id="1aaba-120">Example 4: Enable HTTPS for a custom domain with resource id using Front Door managed certificate.</span></span>
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

<span data-ttu-id="1aaba-121">Abilitare HTTPS per un dominio personalizzato "frontendpointname1-Custom-XYZ" con ID risorsa $resourceId con il certificato gestito da porta principale.</span><span class="sxs-lookup"><span data-stu-id="1aaba-121">Enable HTTPS for a custom domain "frontendpointname1-custom-xyz" with resource id $resourceId using Front Door managed certificate.</span></span>

## <span data-ttu-id="1aaba-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1aaba-122">PARAMETERS</span></span>

### <span data-ttu-id="1aaba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aaba-123">-DefaultProfile</span></span>
<span data-ttu-id="1aaba-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1aaba-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aaba-125">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="1aaba-125">-FrontDoorName</span></span>
<span data-ttu-id="1aaba-126">Il nome della porta d'ingresso.</span><span class="sxs-lookup"><span data-stu-id="1aaba-126">The name of the Front Door.</span></span>

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

### <span data-ttu-id="1aaba-127">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="1aaba-127">-FrontendEndpointName</span></span>
<span data-ttu-id="1aaba-128">Nome endpoint frontend.</span><span class="sxs-lookup"><span data-stu-id="1aaba-128">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="1aaba-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1aaba-129">-InputObject</span></span>
<span data-ttu-id="1aaba-130">L'oggetto endpoint frontend da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1aaba-130">The Frontend endpoint object to update.</span></span>

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

### <span data-ttu-id="1aaba-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aaba-131">-ResourceGroupName</span></span>
<span data-ttu-id="1aaba-132">Gruppo di risorse a cui appartiene la porta principale.</span><span class="sxs-lookup"><span data-stu-id="1aaba-132">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="1aaba-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1aaba-133">-ResourceId</span></span>
<span data-ttu-id="1aaba-134">ID risorsa dell'endpoint della porta principale per abilitare HTTPS</span><span class="sxs-lookup"><span data-stu-id="1aaba-134">Resource Id of the Front Door endpoint to enable https</span></span>

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

### <span data-ttu-id="1aaba-135">-Secretname</span><span class="sxs-lookup"><span data-stu-id="1aaba-135">-SecretName</span></span>
<span data-ttu-id="1aaba-136">Nome del segreto del Vault chiave che rappresenta il PFX completo del certificato</span><span class="sxs-lookup"><span data-stu-id="1aaba-136">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="1aaba-137">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="1aaba-137">-SecretVersion</span></span>
<span data-ttu-id="1aaba-138">La versione del segreto del Vault Key che rappresenta il PFX completo del certificato</span><span class="sxs-lookup"><span data-stu-id="1aaba-138">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="1aaba-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1aaba-139">-VaultId</span></span>
<span data-ttu-id="1aaba-140">ID del Vault chiave contenente il certificato SSL</span><span class="sxs-lookup"><span data-stu-id="1aaba-140">The Key Vault id containing the SSL certificate</span></span>

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

### <span data-ttu-id="1aaba-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1aaba-141">-Confirm</span></span>
<span data-ttu-id="1aaba-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1aaba-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aaba-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aaba-143">-WhatIf</span></span>
<span data-ttu-id="1aaba-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1aaba-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1aaba-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1aaba-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aaba-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aaba-146">CommonParameters</span></span>
<span data-ttu-id="1aaba-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aaba-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aaba-148">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1aaba-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aaba-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1aaba-149">INPUTS</span></span>

### <span data-ttu-id="1aaba-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1aaba-150">System.String</span></span>

## <span data-ttu-id="1aaba-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1aaba-151">OUTPUTS</span></span>

### <span data-ttu-id="1aaba-152">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="1aaba-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="1aaba-153">Note</span><span class="sxs-lookup"><span data-stu-id="1aaba-153">NOTES</span></span>

## <span data-ttu-id="1aaba-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1aaba-154">RELATED LINKS</span></span>
