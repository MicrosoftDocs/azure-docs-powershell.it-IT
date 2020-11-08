---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 441e47b4ef2a796fcdf5ee802cba83f0fce7e352
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031214"
---
# <span data-ttu-id="064fc-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="064fc-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="064fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="064fc-102">SYNOPSIS</span></span>
<span data-ttu-id="064fc-103">Creare criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="064fc-103">Create WAF policy</span></span>

## <span data-ttu-id="064fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="064fc-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="064fc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="064fc-105">DESCRIPTION</span></span>
<span data-ttu-id="064fc-106">Il cmdlet **New-AzFrontDoorWafPolicy** crea un nuovo criterio di Azure WAF nel gruppo di risorse specificato in abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="064fc-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="064fc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="064fc-107">EXAMPLES</span></span>

### <span data-ttu-id="064fc-108">Esempio 1: creare criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="064fc-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="064fc-109">Creare criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="064fc-109">Create WAF policy</span></span>

## <span data-ttu-id="064fc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="064fc-110">PARAMETERS</span></span>

### <span data-ttu-id="064fc-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="064fc-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="064fc-112">Corpo della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="064fc-112">Custom Response Body</span></span>

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

### <span data-ttu-id="064fc-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="064fc-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="064fc-114">Codice di stato della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="064fc-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="064fc-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="064fc-115">-Customrule</span></span>
<span data-ttu-id="064fc-116">Regole personalizzate all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="064fc-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="064fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="064fc-117">-DefaultProfile</span></span>
<span data-ttu-id="064fc-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="064fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="064fc-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="064fc-119">-EnabledState</span></span>
<span data-ttu-id="064fc-120">Se il criterio si trova in stato abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="064fc-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="064fc-121">I valori possibili includono:' disabled ',' Enabled '</span><span class="sxs-lookup"><span data-stu-id="064fc-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="064fc-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="064fc-122">-ManagedRule</span></span>
<span data-ttu-id="064fc-123">Regole gestite all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="064fc-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="064fc-124">-Modalità</span><span class="sxs-lookup"><span data-stu-id="064fc-124">-Mode</span></span>
<span data-ttu-id="064fc-125">Descrive se è in modalità di rilevamento o prevenzione a livello di criteri.</span><span class="sxs-lookup"><span data-stu-id="064fc-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="064fc-126">I valori possibili includono: "prevenzione", "rilevamento"</span><span class="sxs-lookup"><span data-stu-id="064fc-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="064fc-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="064fc-127">-Name</span></span>
<span data-ttu-id="064fc-128">Nome WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="064fc-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="064fc-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="064fc-129">-RedirectUrl</span></span>
<span data-ttu-id="064fc-130">URL di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="064fc-130">Redirect URL</span></span>

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

### <span data-ttu-id="064fc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="064fc-131">-ResourceGroupName</span></span>
<span data-ttu-id="064fc-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="064fc-132">The resource group name</span></span>

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

### <span data-ttu-id="064fc-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="064fc-133">-Confirm</span></span>
<span data-ttu-id="064fc-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="064fc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="064fc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="064fc-135">-WhatIf</span></span>
<span data-ttu-id="064fc-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="064fc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="064fc-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="064fc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="064fc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="064fc-138">CommonParameters</span></span>
<span data-ttu-id="064fc-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="064fc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="064fc-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="064fc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="064fc-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="064fc-141">INPUTS</span></span>

### <span data-ttu-id="064fc-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="064fc-142">None</span></span>

## <span data-ttu-id="064fc-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="064fc-143">OUTPUTS</span></span>

### <span data-ttu-id="064fc-144">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="064fc-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="064fc-145">Note</span><span class="sxs-lookup"><span data-stu-id="064fc-145">NOTES</span></span>

## <span data-ttu-id="064fc-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="064fc-146">RELATED LINKS</span></span>

<span data-ttu-id="064fc-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="064fc-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
