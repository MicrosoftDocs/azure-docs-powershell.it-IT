---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: fe7fb7c2c70563ef44cbdab6b3cfbf0ec7eeea7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674353"
---
# <span data-ttu-id="52f8f-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="52f8f-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="52f8f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="52f8f-103">Aggiornare i criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="52f8f-103">Update WAF policy</span></span>

## <span data-ttu-id="52f8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52f8f-104">SYNTAX</span></span>

### <span data-ttu-id="52f8f-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52f8f-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52f8f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52f8f-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52f8f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52f8f-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52f8f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52f8f-108">DESCRIPTION</span></span>
<span data-ttu-id="52f8f-109">Il cmdlet **Update-AzFrontDoorWafPolicy** aggiorna un criterio WAF esistente.</span><span class="sxs-lookup"><span data-stu-id="52f8f-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="52f8f-110">Se non vengono forniti parametri di input, verranno usati i parametri obsoleti dei criteri di WAF esistenti.</span><span class="sxs-lookup"><span data-stu-id="52f8f-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="52f8f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52f8f-111">EXAMPLES</span></span>

### <span data-ttu-id="52f8f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52f8f-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="52f8f-113">Aggiornare un codice di stato personalizzato di criteri di WAF esistente.</span><span class="sxs-lookup"><span data-stu-id="52f8f-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="52f8f-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="52f8f-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="52f8f-115">Aggiornare una modalità di criteri di WAF esistente.</span><span class="sxs-lookup"><span data-stu-id="52f8f-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="52f8f-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="52f8f-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="52f8f-117">Aggiornare un criterio di WAF esistente abilitato per lo stato e la modalità.</span><span class="sxs-lookup"><span data-stu-id="52f8f-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="52f8f-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="52f8f-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="52f8f-119">Aggiornare tutti i criteri di WAF in $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f8f-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="52f8f-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52f8f-120">PARAMETERS</span></span>

### <span data-ttu-id="52f8f-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="52f8f-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="52f8f-122">Corpo della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="52f8f-122">Custom Response Body</span></span>

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

### <span data-ttu-id="52f8f-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="52f8f-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="52f8f-124">Codice di stato della risposta personalizzato</span><span class="sxs-lookup"><span data-stu-id="52f8f-124">Custom Response Status Code</span></span>

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

### <span data-ttu-id="52f8f-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="52f8f-125">-Customrule</span></span>
<span data-ttu-id="52f8f-126">Regole personalizzate all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="52f8f-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="52f8f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f8f-127">-DefaultProfile</span></span>
<span data-ttu-id="52f8f-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52f8f-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52f8f-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="52f8f-129">-EnabledState</span></span>
<span data-ttu-id="52f8f-130">Se il criterio si trova in stato abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="52f8f-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="52f8f-131">I valori possibili includono:' disabled ',' Enabled '</span><span class="sxs-lookup"><span data-stu-id="52f8f-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="52f8f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52f8f-132">-InputObject</span></span>
<span data-ttu-id="52f8f-133">L'oggetto FireWallPolicy da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="52f8f-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="52f8f-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="52f8f-134">-ManagedRule</span></span>
<span data-ttu-id="52f8f-135">Regole gestite all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="52f8f-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="52f8f-136">-Modalità</span><span class="sxs-lookup"><span data-stu-id="52f8f-136">-Mode</span></span>
<span data-ttu-id="52f8f-137">Descrive se è in modalità di rilevamento o prevenzione a livello di criteri.</span><span class="sxs-lookup"><span data-stu-id="52f8f-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="52f8f-138">I valori possibili includono: "prevenzione", "rilevamento"</span><span class="sxs-lookup"><span data-stu-id="52f8f-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="52f8f-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="52f8f-139">-Name</span></span>
<span data-ttu-id="52f8f-140">Il nome del FireWallPolicy da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="52f8f-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="52f8f-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="52f8f-141">-RedirectUrl</span></span>
<span data-ttu-id="52f8f-142">URL di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="52f8f-142">Redirect URL</span></span>

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

### <span data-ttu-id="52f8f-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f8f-143">-ResourceGroupName</span></span>
<span data-ttu-id="52f8f-144">Il gruppo di risorse a cui appartiene FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="52f8f-144">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="52f8f-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52f8f-145">-ResourceId</span></span>
<span data-ttu-id="52f8f-146">ID risorsa di FireWallPolicy da aggiornare</span><span class="sxs-lookup"><span data-stu-id="52f8f-146">Resource Id of the FireWallPolicy to update</span></span>

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

### <span data-ttu-id="52f8f-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52f8f-147">-Confirm</span></span>
<span data-ttu-id="52f8f-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52f8f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52f8f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52f8f-149">-WhatIf</span></span>
<span data-ttu-id="52f8f-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52f8f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52f8f-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52f8f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52f8f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f8f-152">CommonParameters</span></span>
<span data-ttu-id="52f8f-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f8f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f8f-154">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52f8f-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f8f-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52f8f-155">INPUTS</span></span>

### <span data-ttu-id="52f8f-156">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="52f8f-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="52f8f-157">System. String</span><span class="sxs-lookup"><span data-stu-id="52f8f-157">System.String</span></span>

## <span data-ttu-id="52f8f-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52f8f-158">OUTPUTS</span></span>

### <span data-ttu-id="52f8f-159">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="52f8f-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="52f8f-160">Note</span><span class="sxs-lookup"><span data-stu-id="52f8f-160">NOTES</span></span>

## <span data-ttu-id="52f8f-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52f8f-161">RELATED LINKS</span></span>

<span data-ttu-id="52f8f-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="52f8f-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>