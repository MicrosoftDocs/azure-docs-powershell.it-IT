---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 2d3811b5605b6f4923abd58c64d8d870ede8d334
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403851"
---
# <span data-ttu-id="c3b58-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="c3b58-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="c3b58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3b58-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b58-103">Creare criteri WAF</span><span class="sxs-lookup"><span data-stu-id="c3b58-103">Create WAF policy</span></span>

## <span data-ttu-id="c3b58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3b58-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3b58-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3b58-105">DESCRIPTION</span></span>
<span data-ttu-id="c3b58-106">Il cmdlet **New-AzFrontDoorWafPolicy** crea un nuovo criterio WAF di Azure nel gruppo di risorse specificato nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="c3b58-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="c3b58-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3b58-107">EXAMPLES</span></span>

### <span data-ttu-id="c3b58-108">Esempio 1: Creare criteri WAF</span><span class="sxs-lookup"><span data-stu-id="c3b58-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="c3b58-109">Creare criteri WAF</span><span class="sxs-lookup"><span data-stu-id="c3b58-109">Create WAF policy</span></span>

## <span data-ttu-id="c3b58-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3b58-110">PARAMETERS</span></span>

### <span data-ttu-id="c3b58-111">-CustomBlockResponseBlock</span><span class="sxs-lookup"><span data-stu-id="c3b58-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="c3b58-112">Corpo della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="c3b58-112">Custom Response Body</span></span>

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

### <span data-ttu-id="c3b58-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="c3b58-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="c3b58-114">Codice di stato della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="c3b58-114">Custom Response Status Code</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b58-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="c3b58-115">-Customrule</span></span>
<span data-ttu-id="c3b58-116">Regole personalizzate all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="c3b58-116">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b58-117">-DefaultProfile</span></span>
<span data-ttu-id="c3b58-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3b58-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3b58-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c3b58-119">-EnabledState</span></span>
<span data-ttu-id="c3b58-120">Se il criterio è in stato abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c3b58-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="c3b58-121">I valori possibili includono: "Disabilitato", "Abilitato"</span><span class="sxs-lookup"><span data-stu-id="c3b58-121">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b58-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="c3b58-122">-ManagedRule</span></span>
<span data-ttu-id="c3b58-123">Regole gestite all'interno dei criteri</span><span class="sxs-lookup"><span data-stu-id="c3b58-123">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b58-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="c3b58-124">-Mode</span></span>
<span data-ttu-id="c3b58-125">Descrive se è in modalità di rilevamento o prevenzione a livello di criteri.</span><span class="sxs-lookup"><span data-stu-id="c3b58-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="c3b58-126">I valori possibili includono:'Prevenzione', 'Rilevamento'</span><span class="sxs-lookup"><span data-stu-id="c3b58-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="c3b58-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c3b58-127">-Name</span></span>
<span data-ttu-id="c3b58-128">Nome WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="c3b58-128">WebApplicationFireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b58-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="c3b58-129">-RedirectUrl</span></span>
<span data-ttu-id="c3b58-130">Reindirizza URL</span><span class="sxs-lookup"><span data-stu-id="c3b58-130">Redirect URL</span></span>

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

### <span data-ttu-id="c3b58-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3b58-131">-ResourceGroupName</span></span>
<span data-ttu-id="c3b58-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c3b58-132">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b58-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3b58-133">-Confirm</span></span>
<span data-ttu-id="c3b58-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3b58-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3b58-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3b58-135">-WhatIf</span></span>
<span data-ttu-id="c3b58-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3b58-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3b58-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c3b58-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3b58-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b58-138">CommonParameters</span></span>
<span data-ttu-id="c3b58-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3b58-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b58-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c3b58-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b58-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3b58-141">INPUTS</span></span>

### <span data-ttu-id="c3b58-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c3b58-142">None</span></span>

## <span data-ttu-id="c3b58-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3b58-143">OUTPUTS</span></span>

### <span data-ttu-id="c3b58-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c3b58-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="c3b58-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3b58-145">NOTES</span></span>

## <span data-ttu-id="c3b58-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3b58-146">RELATED LINKS</span></span>

<span data-ttu-id="c3b58-147">[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="c3b58-147">[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
