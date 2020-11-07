---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 67caf6c97c493ad1d19b95ef00c896cb96a47582
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836164"
---
# <span data-ttu-id="6324b-101">New-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="6324b-101">New-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="6324b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6324b-102">SYNOPSIS</span></span>
<span data-ttu-id="6324b-103">Creare criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="6324b-103">Create WAF policy</span></span>

## <span data-ttu-id="6324b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6324b-104">SYNTAX</span></span>

```
New-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6324b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6324b-105">DESCRIPTION</span></span>
<span data-ttu-id="6324b-106">Il cmdlet **New-AzFrontDoorFireWallPolicy** crea un nuovo criterio di Azure WAF nel gruppo di risorse specificato in abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="6324b-106">The **New-AzFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="6324b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6324b-107">EXAMPLES</span></span>

### <span data-ttu-id="6324b-108">Esempio 1: creare criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="6324b-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="6324b-109">Creare criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="6324b-109">Create WAF policy</span></span>

## <span data-ttu-id="6324b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6324b-110">PARAMETERS</span></span>

### <span data-ttu-id="6324b-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="6324b-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="6324b-112">Corpo della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="6324b-112">Custom Response Body</span></span>

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

### <span data-ttu-id="6324b-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="6324b-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="6324b-114">Codice di stato della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="6324b-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="6324b-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="6324b-115">-Customrule</span></span>
<span data-ttu-id="6324b-116">Regole personalizzate all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="6324b-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="6324b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6324b-117">-DefaultProfile</span></span>
<span data-ttu-id="6324b-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6324b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6324b-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="6324b-119">-EnabledState</span></span>
<span data-ttu-id="6324b-120">Se il criterio si trova in stato abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6324b-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="6324b-121">I valori possibili includono:' disabled ',' Enabled '</span><span class="sxs-lookup"><span data-stu-id="6324b-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="6324b-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="6324b-122">-ManagedRule</span></span>
<span data-ttu-id="6324b-123">Regole gestite all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="6324b-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="6324b-124">-Modalità</span><span class="sxs-lookup"><span data-stu-id="6324b-124">-Mode</span></span>
<span data-ttu-id="6324b-125">Descrive se è in modalità di rilevamento o prevenzione a livello di criteri.</span><span class="sxs-lookup"><span data-stu-id="6324b-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="6324b-126">I valori possibili includono: "prevenzione", "rilevamento"</span><span class="sxs-lookup"><span data-stu-id="6324b-126">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6324b-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="6324b-127">-Name</span></span>
<span data-ttu-id="6324b-128">Nome WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="6324b-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="6324b-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="6324b-129">-RedirectUrl</span></span>
<span data-ttu-id="6324b-130">URL di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="6324b-130">Redirect URL</span></span>

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

### <span data-ttu-id="6324b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6324b-131">-ResourceGroupName</span></span>
<span data-ttu-id="6324b-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6324b-132">The resource group name</span></span>

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

### <span data-ttu-id="6324b-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6324b-133">-Confirm</span></span>
<span data-ttu-id="6324b-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6324b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6324b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6324b-135">-WhatIf</span></span>
<span data-ttu-id="6324b-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6324b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6324b-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6324b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6324b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6324b-138">CommonParameters</span></span>
<span data-ttu-id="6324b-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6324b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6324b-140">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6324b-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6324b-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6324b-141">INPUTS</span></span>

### <span data-ttu-id="6324b-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6324b-142">None</span></span>

## <span data-ttu-id="6324b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6324b-143">OUTPUTS</span></span>

### <span data-ttu-id="6324b-144">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="6324b-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="6324b-145">Note</span><span class="sxs-lookup"><span data-stu-id="6324b-145">NOTES</span></span>

## <span data-ttu-id="6324b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6324b-146">RELATED LINKS</span></span>

<span data-ttu-id="6324b-147">[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="6324b-147">[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
