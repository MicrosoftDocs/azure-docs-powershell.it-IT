---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 5c39a86b29ce27ea57d51e7e3bfb048560ef1ee6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970830"
---
# <span data-ttu-id="58e38-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="58e38-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="58e38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58e38-102">SYNOPSIS</span></span>
<span data-ttu-id="58e38-103">Creare criteri WAF</span><span class="sxs-lookup"><span data-stu-id="58e38-103">Create WAF policy</span></span>

## <span data-ttu-id="58e38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58e38-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58e38-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="58e38-105">DESCRIPTION</span></span>
<span data-ttu-id="58e38-106">Il cmdlet **New-AzFrontDoorWafPolicy** crea un nuovo criterio WAF di Azure nel gruppo di risorse specificato nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="58e38-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="58e38-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58e38-107">EXAMPLES</span></span>

### <span data-ttu-id="58e38-108">Esempio 1: Creare criteri WAF</span><span class="sxs-lookup"><span data-stu-id="58e38-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="58e38-109">Creare criteri WAF</span><span class="sxs-lookup"><span data-stu-id="58e38-109">Create WAF policy</span></span>

## <span data-ttu-id="58e38-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58e38-110">PARAMETERS</span></span>

### <span data-ttu-id="58e38-111">-CustomBlockResponseBlockBlock</span><span class="sxs-lookup"><span data-stu-id="58e38-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="58e38-112">Corpo della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="58e38-112">Custom Response Body</span></span>

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

### <span data-ttu-id="58e38-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="58e38-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="58e38-114">Codice di stato della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="58e38-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="58e38-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="58e38-115">-Customrule</span></span>
<span data-ttu-id="58e38-116">Regole personalizzate all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="58e38-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="58e38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e38-117">-DefaultProfile</span></span>
<span data-ttu-id="58e38-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58e38-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58e38-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="58e38-119">-EnabledState</span></span>
<span data-ttu-id="58e38-120">Se il criterio è in stato abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="58e38-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="58e38-121">I valori possibili includono: "Disabilitato", "Abilitato"</span><span class="sxs-lookup"><span data-stu-id="58e38-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="58e38-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="58e38-122">-ManagedRule</span></span>
<span data-ttu-id="58e38-123">Regole gestite all'interno dei criteri</span><span class="sxs-lookup"><span data-stu-id="58e38-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="58e38-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="58e38-124">-Mode</span></span>
<span data-ttu-id="58e38-125">Descrive se è in modalità di rilevamento o prevenzione a livello di criteri.</span><span class="sxs-lookup"><span data-stu-id="58e38-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="58e38-126">I valori possibili includono:'Prevenzione', 'Rilevamento'</span><span class="sxs-lookup"><span data-stu-id="58e38-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="58e38-127">-Name</span><span class="sxs-lookup"><span data-stu-id="58e38-127">-Name</span></span>
<span data-ttu-id="58e38-128">Nome WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="58e38-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="58e38-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="58e38-129">-RedirectUrl</span></span>
<span data-ttu-id="58e38-130">Reindirizza URL</span><span class="sxs-lookup"><span data-stu-id="58e38-130">Redirect URL</span></span>

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

### <span data-ttu-id="58e38-131">-RequestCheckCheck</span><span class="sxs-lookup"><span data-stu-id="58e38-131">-RequestBodyCheck</span></span>
<span data-ttu-id="58e38-132">Definisce se il corpo deve essere esaminato dalle regole gestite.</span><span class="sxs-lookup"><span data-stu-id="58e38-132">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="58e38-133">I valori possibili includono: 'Abilitato', 'Disabilitato'</span><span class="sxs-lookup"><span data-stu-id="58e38-133">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="58e38-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e38-134">-ResourceGroupName</span></span>
<span data-ttu-id="58e38-135">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="58e38-135">The resource group name</span></span>

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

### <span data-ttu-id="58e38-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58e38-136">-Confirm</span></span>
<span data-ttu-id="58e38-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58e38-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58e38-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58e38-138">-WhatIf</span></span>
<span data-ttu-id="58e38-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58e38-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58e38-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58e38-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58e38-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e38-141">CommonParameters</span></span>
<span data-ttu-id="58e38-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e38-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e38-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="58e38-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e38-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="58e38-144">INPUTS</span></span>

### <span data-ttu-id="58e38-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58e38-145">None</span></span>

## <span data-ttu-id="58e38-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58e38-146">OUTPUTS</span></span>

### <span data-ttu-id="58e38-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="58e38-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="58e38-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="58e38-148">NOTES</span></span>

## <span data-ttu-id="58e38-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58e38-149">RELATED LINKS</span></span>

<span data-ttu-id="58e38-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="58e38-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
