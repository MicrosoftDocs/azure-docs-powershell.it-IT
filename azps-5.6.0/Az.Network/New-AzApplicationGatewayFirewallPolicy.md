---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e643bf488073f6da685265cea4a2a0c6cb7cebf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970510"
---
# <span data-ttu-id="54c35-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="54c35-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="54c35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c35-102">SYNOPSIS</span></span>
<span data-ttu-id="54c35-103">Crea un criterio firewall del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="54c35-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="54c35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54c35-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c35-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="54c35-105">DESCRIPTION</span></span>
<span data-ttu-id="54c35-106">Il cmdlet **New-AzApplicationGatewayFirewallPolicy crea** un criterio firewall del gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="54c35-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="54c35-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54c35-107">EXAMPLES</span></span>

### <span data-ttu-id="54c35-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="54c35-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="54c35-109">Questo comando crea un nuovo criterio firewall del Gateway di applicazione Azure denominato "wafResource1" nel gruppo di risorse "rg1" nella posizione "westus" con regole personalizzate definite nella variabile $customRule></span><span class="sxs-lookup"><span data-stu-id="54c35-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="54c35-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54c35-110">PARAMETERS</span></span>

### <span data-ttu-id="54c35-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54c35-111">-AsJob</span></span>
<span data-ttu-id="54c35-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="54c35-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54c35-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="54c35-113">-CustomRule</span></span>
<span data-ttu-id="54c35-114">Elenco Di Regole Personalizzate</span><span class="sxs-lookup"><span data-stu-id="54c35-114">The list of CustomRules</span></span>

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

### <span data-ttu-id="54c35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c35-115">-DefaultProfile</span></span>
<span data-ttu-id="54c35-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54c35-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c35-117">-Force</span><span class="sxs-lookup"><span data-stu-id="54c35-117">-Force</span></span>
<span data-ttu-id="54c35-118">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="54c35-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="54c35-119">-Location</span><span class="sxs-lookup"><span data-stu-id="54c35-119">-Location</span></span>
<span data-ttu-id="54c35-120">posizione.</span><span class="sxs-lookup"><span data-stu-id="54c35-120">location.</span></span>

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

### <span data-ttu-id="54c35-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="54c35-121">-ManagedRule</span></span>
<span data-ttu-id="54c35-122">Impostazione regole gestite</span><span class="sxs-lookup"><span data-stu-id="54c35-122">Managed Rule Setting</span></span>

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

### <span data-ttu-id="54c35-123">-Name</span><span class="sxs-lookup"><span data-stu-id="54c35-123">-Name</span></span>
<span data-ttu-id="54c35-124">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="54c35-124">The resource name.</span></span>

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

### <span data-ttu-id="54c35-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="54c35-125">-PolicySetting</span></span>
<span data-ttu-id="54c35-126">Impostazioni dei criteri per Firewall applicazione Web</span><span class="sxs-lookup"><span data-stu-id="54c35-126">Policy Settings for Web Application Firewall</span></span>

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

### <span data-ttu-id="54c35-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c35-127">-ResourceGroupName</span></span>
<span data-ttu-id="54c35-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54c35-128">The resource group name.</span></span>

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

### <span data-ttu-id="54c35-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="54c35-129">-Tag</span></span>
<span data-ttu-id="54c35-130">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="54c35-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="54c35-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54c35-131">-Confirm</span></span>
<span data-ttu-id="54c35-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c35-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c35-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c35-133">-WhatIf</span></span>
<span data-ttu-id="54c35-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54c35-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c35-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54c35-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c35-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c35-136">CommonParameters</span></span>
<span data-ttu-id="54c35-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c35-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c35-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="54c35-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c35-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="54c35-139">INPUTS</span></span>

### <span data-ttu-id="54c35-140">System.String</span><span class="sxs-lookup"><span data-stu-id="54c35-140">System.String</span></span>

### <span data-ttu-id="54c35-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span><span class="sxs-lookup"><span data-stu-id="54c35-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="54c35-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="54c35-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="54c35-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="54c35-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="54c35-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="54c35-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="54c35-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54c35-145">OUTPUTS</span></span>

### <span data-ttu-id="54c35-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="54c35-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="54c35-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="54c35-147">NOTES</span></span>

## <span data-ttu-id="54c35-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54c35-148">RELATED LINKS</span></span>
