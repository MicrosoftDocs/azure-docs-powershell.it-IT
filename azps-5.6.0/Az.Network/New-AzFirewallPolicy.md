---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 3e60546992957a027dd5bbb94281e19e74e42274
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976686"
---
# <span data-ttu-id="f5ab3-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f5ab3-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="f5ab3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ab3-103">Crea un nuovo criterio del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="f5ab3-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="f5ab3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5ab3-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-IntrusionDetection <PSAzureFirewallPolicyIntrusionDetection>] [-TransportSecurityName <String>]
 [-TransportSecurityKeyVaultSecretId <String>] [-SkuTier <String>] [-UserAssignedIdentityId <String>]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5ab3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f5ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ab3-106">Il cmdlet **New-AzFirewallPolicy crea** un criterio del firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="f5ab3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5ab3-107">EXAMPLES</span></span>

### <span data-ttu-id="f5ab3-108">Esempio 1: 1.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-108">Example 1: 1.</span></span> <span data-ttu-id="f5ab3-109">Creare un criterio vuoto</span><span class="sxs-lookup"><span data-stu-id="f5ab3-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="f5ab3-110">Questo esempio crea un criterio firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="f5ab3-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="f5ab3-111">Esempio 2: 2.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-111">Example 2: 2.</span></span> <span data-ttu-id="f5ab3-112">Creare un criterio vuoto con la modalità ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="f5ab3-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="f5ab3-113">Questo esempio crea un criterio del firewall di Azure con una modalità Threat Intel</span><span class="sxs-lookup"><span data-stu-id="f5ab3-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="f5ab3-114">Esempio 3: 3.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-114">Example 3: 3.</span></span> <span data-ttu-id="f5ab3-115">Creare un criterio vuoto con l'elenco degli elementi di ThreatIntel Whitelist</span><span class="sxs-lookup"><span data-stu-id="f5ab3-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="f5ab3-116">Questo esempio crea un criterio firewall azure con una minaccia intel whitelist</span><span class="sxs-lookup"><span data-stu-id="f5ab3-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

### <span data-ttu-id="f5ab3-117">Esempio 4: 4.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-117">Example 4: 4.</span></span> <span data-ttu-id="f5ab3-118">Creare criteri con il rilevamento delle intrusioni, l'identità e la sicurezza del trasporto</span><span class="sxs-lookup"><span data-stu-id="f5ab3-118">Create policy with intrusion detection, identity and transport security</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride -BypassTraffic $bypass
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/TestRg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/user-assign-identity'
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection -TransportSecurityName tsName -TransportSecurityKeyVaultSecretId "https://<keyvaultname>.vault.azure.net/secrets/cacert"  -UserAssignedIdentityId $userAssignedIdentity
```

<span data-ttu-id="f5ab3-119">Questo esempio crea un criterio del firewall di Azure con un avviso di rilevamento delle intrusioni in modalità, un'identità assegnata dall'utente e la sicurezza del trasporto</span><span class="sxs-lookup"><span data-stu-id="f5ab3-119">This example creates an azure firewall policy with a intrusion detection in mode alert, user assigned identity and transport security</span></span>

## <span data-ttu-id="f5ab3-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5ab3-120">PARAMETERS</span></span>

### <span data-ttu-id="f5ab3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5ab3-121">-AsJob</span></span>
<span data-ttu-id="f5ab3-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f5ab3-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-123">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="f5ab3-123">-BasePolicy</span></span>
<span data-ttu-id="f5ab3-124">Criteri di base da cui ereditare</span><span class="sxs-lookup"><span data-stu-id="f5ab3-124">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ab3-125">-DefaultProfile</span></span>
<span data-ttu-id="f5ab3-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-127">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="f5ab3-127">-DnsSetting</span></span>
<span data-ttu-id="f5ab3-128">Impostazione DNS</span><span class="sxs-lookup"><span data-stu-id="f5ab3-128">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-129">-Force</span><span class="sxs-lookup"><span data-stu-id="f5ab3-129">-Force</span></span>
<span data-ttu-id="f5ab3-130">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="f5ab3-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-131">-Identity</span><span class="sxs-lookup"><span data-stu-id="f5ab3-131">-Identity</span></span>
<span data-ttu-id="f5ab3-132">Identità dei criteri del firewall da assegnare ai criteri firewall.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-132">Firewall Policy Identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-133">-IntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="f5ab3-133">-IntrusionDetection</span></span>
<span data-ttu-id="f5ab3-134">Impostazione del rilevamento delle intrusioni</span><span class="sxs-lookup"><span data-stu-id="f5ab3-134">The Intrusion Detection Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-135">-Location</span><span class="sxs-lookup"><span data-stu-id="f5ab3-135">-Location</span></span>
<span data-ttu-id="f5ab3-136">posizione.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-136">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f5ab3-137">-Name</span></span>
<span data-ttu-id="f5ab3-138">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ab3-139">-ResourceGroupName</span></span>
<span data-ttu-id="f5ab3-140">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-140">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-141">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="f5ab3-141">-SkuTier</span></span>
<span data-ttu-id="f5ab3-142">Livello SKU dei criteri del firewall</span><span class="sxs-lookup"><span data-stu-id="f5ab3-142">Firewall policy sku tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="f5ab3-143">-Tag</span></span>
<span data-ttu-id="f5ab3-144">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-144">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-145">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="f5ab3-145">-ThreatIntelMode</span></span>
<span data-ttu-id="f5ab3-146">Modalità di operazione per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-146">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-147">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="f5ab3-147">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="f5ab3-148">Elenco degli indirizzi vuoti per Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="f5ab3-148">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-149">-TransportSecurityKeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="f5ab3-149">-TransportSecurityKeyVaultSecretId</span></span>
<span data-ttu-id="f5ab3-150">ID segreto di (oggetto pfx non crittografato codificato in base 64) di oggetto "Segreto" o "Certificato" archiviato in KeyVault</span><span class="sxs-lookup"><span data-stu-id="f5ab3-150">Secret Id of (base-64 encoded unencrypted pfx) 'Secret' or 'Certificate' object stored in KeyVault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-151">-TransportSecurityName</span><span class="sxs-lookup"><span data-stu-id="f5ab3-151">-TransportSecurityName</span></span>
<span data-ttu-id="f5ab3-152">Nome della sicurezza del trasporto</span><span class="sxs-lookup"><span data-stu-id="f5ab3-152">Transport security name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-153">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="f5ab3-153">-UserAssignedIdentityId</span></span>
<span data-ttu-id="f5ab3-154">ResourceId dell'identità assegnata all'utente da assegnare ai criteri del firewall.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-154">ResourceId of the user assigned identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5ab3-155">-Confirm</span></span>
<span data-ttu-id="f5ab3-156">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ab3-157">-WhatIf</span></span>
<span data-ttu-id="f5ab3-158">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5ab3-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ab3-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ab3-160">CommonParameters</span></span>
<span data-ttu-id="f5ab3-161">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ab3-162">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f5ab3-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ab3-163">INPUT</span><span class="sxs-lookup"><span data-stu-id="f5ab3-163">INPUTS</span></span>

### <span data-ttu-id="f5ab3-164">System.String</span><span class="sxs-lookup"><span data-stu-id="f5ab3-164">System.String</span></span>

### <span data-ttu-id="f5ab3-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f5ab3-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f5ab3-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5ab3-166">OUTPUTS</span></span>

### <span data-ttu-id="f5ab3-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f5ab3-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="f5ab3-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="f5ab3-168">NOTES</span></span>

## <span data-ttu-id="f5ab3-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5ab3-169">RELATED LINKS</span></span>
