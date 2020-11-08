---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192736"
---
# <span data-ttu-id="1f25a-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1f25a-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="1f25a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f25a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f25a-103">Salva un criterio firewall di Azure modificato</span><span class="sxs-lookup"><span data-stu-id="1f25a-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="1f25a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f25a-104">SYNTAX</span></span>

### <span data-ttu-id="1f25a-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f25a-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f25a-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f25a-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f25a-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f25a-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f25a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f25a-108">DESCRIPTION</span></span>
<span data-ttu-id="1f25a-109">Il cmdlet **set-AzFirewallPolicy** aggiorna i criteri di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="1f25a-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="1f25a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f25a-110">EXAMPLES</span></span>

### <span data-ttu-id="1f25a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1f25a-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="1f25a-112">Questo esempio imposta i criteri del firewall con il nuovo valore dei criteri firewall</span><span class="sxs-lookup"><span data-stu-id="1f25a-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="1f25a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1f25a-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="1f25a-114">Questo esempio imposta i criteri del firewall con la nuova modalità Intel Threat</span><span class="sxs-lookup"><span data-stu-id="1f25a-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="1f25a-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1f25a-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="1f25a-116">Questo esempio imposta i criteri del firewall con il nuovo Threat Intel whitelist</span><span class="sxs-lookup"><span data-stu-id="1f25a-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="1f25a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f25a-117">PARAMETERS</span></span>

### <span data-ttu-id="1f25a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f25a-118">-AsJob</span></span>
<span data-ttu-id="1f25a-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1f25a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f25a-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="1f25a-120">-BasePolicy</span></span>
<span data-ttu-id="1f25a-121">Criteri di base per cui ereditare da</span><span class="sxs-lookup"><span data-stu-id="1f25a-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="1f25a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f25a-122">-DefaultProfile</span></span>
<span data-ttu-id="1f25a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f25a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f25a-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="1f25a-124">-DnsSetting</span></span>
<span data-ttu-id="1f25a-125">Impostazione DNS</span><span class="sxs-lookup"><span data-stu-id="1f25a-125">The DNS Setting</span></span>

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

### <span data-ttu-id="1f25a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f25a-126">-InputObject</span></span>
<span data-ttu-id="1f25a-127">Criteri AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1f25a-127">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="1f25a-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1f25a-128">-Location</span></span>
<span data-ttu-id="1f25a-129">posizione.</span><span class="sxs-lookup"><span data-stu-id="1f25a-129">location.</span></span>

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

### <span data-ttu-id="1f25a-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f25a-130">-Name</span></span>
<span data-ttu-id="1f25a-131">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f25a-131">The resource name.</span></span>

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

### <span data-ttu-id="1f25a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f25a-132">-ResourceGroupName</span></span>
<span data-ttu-id="1f25a-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f25a-133">The resource group name.</span></span>

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

### <span data-ttu-id="1f25a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f25a-134">-ResourceId</span></span>
<span data-ttu-id="1f25a-135">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f25a-135">The resource Id.</span></span>

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

### <span data-ttu-id="1f25a-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f25a-136">-Tag</span></span>
<span data-ttu-id="1f25a-137">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="1f25a-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1f25a-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="1f25a-138">-ThreatIntelMode</span></span>
<span data-ttu-id="1f25a-139">Modalità operativa per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="1f25a-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="1f25a-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="1f25a-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="1f25a-141">Whitelist per Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="1f25a-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="1f25a-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f25a-142">-Confirm</span></span>
<span data-ttu-id="1f25a-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f25a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f25a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f25a-144">-WhatIf</span></span>
<span data-ttu-id="1f25a-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f25a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f25a-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f25a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f25a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f25a-147">CommonParameters</span></span>
<span data-ttu-id="1f25a-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f25a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f25a-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f25a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f25a-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f25a-150">INPUTS</span></span>

### <span data-ttu-id="1f25a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="1f25a-151">System.String</span></span>

### <span data-ttu-id="1f25a-152">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1f25a-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="1f25a-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f25a-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1f25a-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f25a-154">OUTPUTS</span></span>

### <span data-ttu-id="1f25a-155">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1f25a-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="1f25a-156">Note</span><span class="sxs-lookup"><span data-stu-id="1f25a-156">NOTES</span></span>

## <span data-ttu-id="1f25a-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f25a-157">RELATED LINKS</span></span>
