---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189510"
---
# <span data-ttu-id="05cc7-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="05cc7-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="05cc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="05cc7-103">Salva un criterio firewall di Azure modificato</span><span class="sxs-lookup"><span data-stu-id="05cc7-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="05cc7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05cc7-104">SYNTAX</span></span>

### <span data-ttu-id="05cc7-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05cc7-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cc7-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05cc7-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05cc7-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05cc7-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05cc7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05cc7-108">DESCRIPTION</span></span>
<span data-ttu-id="05cc7-109">Il cmdlet **Set-AzFirewallPolicy** aggiorna un criterio del firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="05cc7-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="05cc7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05cc7-110">EXAMPLES</span></span>

### <span data-ttu-id="05cc7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="05cc7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="05cc7-112">Questo esempio imposta il criterio del firewall con il nuovo valore del criterio firewall</span><span class="sxs-lookup"><span data-stu-id="05cc7-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="05cc7-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="05cc7-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="05cc7-114">Questo esempio imposta i criteri del firewall con la nuova modalità Threat Intel</span><span class="sxs-lookup"><span data-stu-id="05cc7-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="05cc7-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="05cc7-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="05cc7-116">Questo esempio imposta i criteri del firewall con la nuova minaccia intel whitelist</span><span class="sxs-lookup"><span data-stu-id="05cc7-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="05cc7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05cc7-117">PARAMETERS</span></span>

### <span data-ttu-id="05cc7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05cc7-118">-AsJob</span></span>
<span data-ttu-id="05cc7-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="05cc7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05cc7-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="05cc7-120">-BasePolicy</span></span>
<span data-ttu-id="05cc7-121">Criteri di base da cui ereditare</span><span class="sxs-lookup"><span data-stu-id="05cc7-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="05cc7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05cc7-122">-DefaultProfile</span></span>
<span data-ttu-id="05cc7-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05cc7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05cc7-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="05cc7-124">-DnsSetting</span></span>
<span data-ttu-id="05cc7-125">Impostazione DNS</span><span class="sxs-lookup"><span data-stu-id="05cc7-125">The DNS Setting</span></span>

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

### <span data-ttu-id="05cc7-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05cc7-126">-InputObject</span></span>
<span data-ttu-id="05cc7-127">Criteri di AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="05cc7-127">The AzureFirewall Policy</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05cc7-128">-Location</span><span class="sxs-lookup"><span data-stu-id="05cc7-128">-Location</span></span>
<span data-ttu-id="05cc7-129">posizione.</span><span class="sxs-lookup"><span data-stu-id="05cc7-129">location.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05cc7-130">-Name</span><span class="sxs-lookup"><span data-stu-id="05cc7-130">-Name</span></span>
<span data-ttu-id="05cc7-131">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="05cc7-131">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05cc7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05cc7-132">-ResourceGroupName</span></span>
<span data-ttu-id="05cc7-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="05cc7-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05cc7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05cc7-134">-ResourceId</span></span>
<span data-ttu-id="05cc7-135">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="05cc7-135">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05cc7-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="05cc7-136">-Tag</span></span>
<span data-ttu-id="05cc7-137">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="05cc7-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="05cc7-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="05cc7-138">-ThreatIntelMode</span></span>
<span data-ttu-id="05cc7-139">Modalità di operazione per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="05cc7-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="05cc7-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="05cc7-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="05cc7-141">Elenco degli indirizzi vuoti per Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="05cc7-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="05cc7-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05cc7-142">-Confirm</span></span>
<span data-ttu-id="05cc7-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05cc7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05cc7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05cc7-144">-WhatIf</span></span>
<span data-ttu-id="05cc7-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05cc7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05cc7-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05cc7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05cc7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05cc7-147">CommonParameters</span></span>
<span data-ttu-id="05cc7-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05cc7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05cc7-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05cc7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05cc7-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="05cc7-150">INPUTS</span></span>

### <span data-ttu-id="05cc7-151">System.String</span><span class="sxs-lookup"><span data-stu-id="05cc7-151">System.String</span></span>

### <span data-ttu-id="05cc7-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="05cc7-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="05cc7-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="05cc7-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="05cc7-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05cc7-154">OUTPUTS</span></span>

### <span data-ttu-id="05cc7-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="05cc7-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="05cc7-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="05cc7-156">NOTES</span></span>

## <span data-ttu-id="05cc7-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05cc7-157">RELATED LINKS</span></span>
