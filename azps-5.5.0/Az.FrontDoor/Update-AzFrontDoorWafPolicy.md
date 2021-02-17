---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: a3358681fd501602833f0168a6920dc2c3ec7864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209450"
---
# <span data-ttu-id="c7023-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="c7023-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="c7023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7023-102">SYNOPSIS</span></span>
<span data-ttu-id="c7023-103">Aggiornare i criteri WAF</span><span class="sxs-lookup"><span data-stu-id="c7023-103">Update WAF policy</span></span>

## <span data-ttu-id="c7023-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7023-104">SYNTAX</span></span>

### <span data-ttu-id="c7023-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7023-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7023-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7023-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7023-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7023-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7023-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c7023-108">DESCRIPTION</span></span>
<span data-ttu-id="c7023-109">Il cmdlet **Update-AzFrontDoorWafPolicy** aggiorna un criterio WAF esistente.</span><span class="sxs-lookup"><span data-stu-id="c7023-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="c7023-110">Se non vengono forniti parametri di input, verranno usati i vecchi parametri del criterio WAF esistente.</span><span class="sxs-lookup"><span data-stu-id="c7023-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="c7023-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7023-111">EXAMPLES</span></span>

### <span data-ttu-id="c7023-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c7023-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="c7023-113">Aggiornare un codice di stato personalizzato dei criteri WAF esistenti.</span><span class="sxs-lookup"><span data-stu-id="c7023-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="c7023-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c7023-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="c7023-115">Aggiornare una modalità criterio WAF esistente.</span><span class="sxs-lookup"><span data-stu-id="c7023-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="c7023-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c7023-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="c7023-117">Aggiornare uno stato e una modalità abilitati per un criterio WAF esistente.</span><span class="sxs-lookup"><span data-stu-id="c7023-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="c7023-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="c7023-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="c7023-119">Aggiornare tutti i criteri WAF in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7023-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="c7023-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7023-120">PARAMETERS</span></span>

### <span data-ttu-id="c7023-121">-CustomBlockResponseBlock</span><span class="sxs-lookup"><span data-stu-id="c7023-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="c7023-122">Corpo della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="c7023-122">Custom Response Body</span></span>

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

### <span data-ttu-id="c7023-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="c7023-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="c7023-124">Codice di stato della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="c7023-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7023-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="c7023-125">-Customrule</span></span>
<span data-ttu-id="c7023-126">Regole personalizzate all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="c7023-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="c7023-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7023-127">-DefaultProfile</span></span>
<span data-ttu-id="c7023-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7023-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7023-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c7023-129">-EnabledState</span></span>
<span data-ttu-id="c7023-130">Se il criterio è in stato abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="c7023-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="c7023-131">I valori possibili includono: "Disabilitato", "Abilitato"</span><span class="sxs-lookup"><span data-stu-id="c7023-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="c7023-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7023-132">-InputObject</span></span>
<span data-ttu-id="c7023-133">Oggetto FireWallPolicy da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c7023-133">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7023-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="c7023-134">-ManagedRule</span></span>
<span data-ttu-id="c7023-135">Regole gestite all'interno dei criteri</span><span class="sxs-lookup"><span data-stu-id="c7023-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="c7023-136">-Modalità</span><span class="sxs-lookup"><span data-stu-id="c7023-136">-Mode</span></span>
<span data-ttu-id="c7023-137">Descrive se è in modalità di rilevamento o prevenzione a livello di criteri.</span><span class="sxs-lookup"><span data-stu-id="c7023-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="c7023-138">I valori possibili includono:'Prevenzione', 'Rilevamento'</span><span class="sxs-lookup"><span data-stu-id="c7023-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="c7023-139">-Name</span><span class="sxs-lookup"><span data-stu-id="c7023-139">-Name</span></span>
<span data-ttu-id="c7023-140">Nome del valore FireWallPolicy da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="c7023-140">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7023-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="c7023-141">-RedirectUrl</span></span>
<span data-ttu-id="c7023-142">Reindirizza URL</span><span class="sxs-lookup"><span data-stu-id="c7023-142">Redirect URL</span></span>

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

### <span data-ttu-id="c7023-143">-RequestCheckCheck</span><span class="sxs-lookup"><span data-stu-id="c7023-143">-RequestBodyCheck</span></span>
<span data-ttu-id="c7023-144">Definisce se il corpo deve essere esaminato dalle regole gestite.</span><span class="sxs-lookup"><span data-stu-id="c7023-144">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="c7023-145">I valori possibili includono: 'Abilitato', 'Disabilitato'</span><span class="sxs-lookup"><span data-stu-id="c7023-145">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="c7023-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7023-146">-ResourceGroupName</span></span>
<span data-ttu-id="c7023-147">Gruppo di risorse a cui appartiene il campo FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="c7023-147">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7023-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7023-148">-ResourceId</span></span>
<span data-ttu-id="c7023-149">ID risorsa del valore FireWallPolicy da aggiornare</span><span class="sxs-lookup"><span data-stu-id="c7023-149">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7023-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7023-150">-Confirm</span></span>
<span data-ttu-id="c7023-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7023-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7023-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7023-152">-WhatIf</span></span>
<span data-ttu-id="c7023-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7023-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7023-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7023-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7023-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7023-155">CommonParameters</span></span>
<span data-ttu-id="c7023-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7023-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7023-157">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c7023-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7023-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="c7023-158">INPUTS</span></span>

### <span data-ttu-id="c7023-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c7023-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="c7023-160">System.String</span><span class="sxs-lookup"><span data-stu-id="c7023-160">System.String</span></span>

## <span data-ttu-id="c7023-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7023-161">OUTPUTS</span></span>

### <span data-ttu-id="c7023-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c7023-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="c7023-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="c7023-163">NOTES</span></span>

## <span data-ttu-id="c7023-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7023-164">RELATED LINKS</span></span>

<span data-ttu-id="c7023-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="c7023-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
