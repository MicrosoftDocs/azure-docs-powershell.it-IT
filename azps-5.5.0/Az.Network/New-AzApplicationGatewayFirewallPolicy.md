---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187094"
---
# <span data-ttu-id="a2a15-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a2a15-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="a2a15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2a15-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a15-103">Crea un criterio firewall del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="a2a15-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="a2a15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2a15-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2a15-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a2a15-105">DESCRIPTION</span></span>
<span data-ttu-id="a2a15-106">Il cmdlet **New-AzApplicationGatewayFirewallPolicy** crea un criterio firewall del gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="a2a15-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="a2a15-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2a15-107">EXAMPLES</span></span>

### <span data-ttu-id="a2a15-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2a15-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="a2a15-109">Questo comando crea un nuovo criterio firewall del Gateway di applicazione Azure denominato "wafResource1" nel gruppo di risorse "rg1" nella posizione "westus" con regole personalizzate definite nella variabile $customRule></span><span class="sxs-lookup"><span data-stu-id="a2a15-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="a2a15-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2a15-110">PARAMETERS</span></span>

### <span data-ttu-id="a2a15-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2a15-111">-AsJob</span></span>
<span data-ttu-id="a2a15-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a2a15-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a15-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="a2a15-113">-CustomRule</span></span>
<span data-ttu-id="a2a15-114">Elenco Delle Regole Personalizzate</span><span class="sxs-lookup"><span data-stu-id="a2a15-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a15-115">-DefaultProfile</span></span>
<span data-ttu-id="a2a15-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2a15-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a2a15-117">-Force</span></span>
<span data-ttu-id="a2a15-118">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="a2a15-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2a15-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a2a15-119">-Location</span></span>
<span data-ttu-id="a2a15-120">posizione.</span><span class="sxs-lookup"><span data-stu-id="a2a15-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a15-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="a2a15-121">-ManagedRule</span></span>
<span data-ttu-id="a2a15-122">Impostazione regole gestite</span><span class="sxs-lookup"><span data-stu-id="a2a15-122">Managed Rule Setting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a15-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a2a15-123">-Name</span></span>
<span data-ttu-id="a2a15-124">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2a15-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a15-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="a2a15-125">-PolicySetting</span></span>
<span data-ttu-id="a2a15-126">Impostazioni dei criteri per Firewall applicazione Web</span><span class="sxs-lookup"><span data-stu-id="a2a15-126">Policy Settings for Web Application Firewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a15-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2a15-127">-ResourceGroupName</span></span>
<span data-ttu-id="a2a15-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a2a15-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a15-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="a2a15-129">-Tag</span></span>
<span data-ttu-id="a2a15-130">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="a2a15-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2a15-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2a15-131">-Confirm</span></span>
<span data-ttu-id="a2a15-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2a15-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2a15-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2a15-133">-WhatIf</span></span>
<span data-ttu-id="a2a15-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2a15-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2a15-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2a15-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2a15-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a15-136">CommonParameters</span></span>
<span data-ttu-id="a2a15-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2a15-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a15-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a2a15-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a15-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="a2a15-139">INPUTS</span></span>

### <span data-ttu-id="a2a15-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a2a15-140">System.String</span></span>

### <span data-ttu-id="a2a15-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span><span class="sxs-lookup"><span data-stu-id="a2a15-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="a2a15-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="a2a15-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="a2a15-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="a2a15-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="a2a15-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2a15-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a2a15-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2a15-145">OUTPUTS</span></span>

### <span data-ttu-id="a2a15-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a2a15-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="a2a15-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="a2a15-147">NOTES</span></span>

## <span data-ttu-id="a2a15-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2a15-148">RELATED LINKS</span></span>
