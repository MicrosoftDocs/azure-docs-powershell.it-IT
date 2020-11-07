---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: a02510cc72b9e674f9d4fded1355ae5b2cadc807
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685430"
---
# <span data-ttu-id="82ef0-101">Set-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="82ef0-101">Set-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="82ef0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="82ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="82ef0-103">aggiornare i criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="82ef0-103">update WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82ef0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82ef0-104">SYNTAX</span></span>

### <span data-ttu-id="82ef0-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="82ef0-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ef0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82ef0-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ef0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82ef0-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ef0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82ef0-108">DESCRIPTION</span></span>
<span data-ttu-id="82ef0-109">Il cmdlet **set-AzureRmFrontDoor** aggiorna un criterio WAF esistente.</span><span class="sxs-lookup"><span data-stu-id="82ef0-109">The **Set-AzureRmFrontDoor** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="82ef0-110">Se non vengono forniti parametri di input, verranno usati i parametri obsoleti dei criteri di WAF esistenti.</span><span class="sxs-lookup"><span data-stu-id="82ef0-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="82ef0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82ef0-111">EXAMPLES</span></span>

### <span data-ttu-id="82ef0-112">Esempio 1: aggiornare un criterio di WAF esistente</span><span class="sxs-lookup"><span data-stu-id="82ef0-112">Example 1: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $node

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="82ef0-113">aggiornare un criterio di WAF esistente</span><span class="sxs-lookup"><span data-stu-id="82ef0-113">update an existing WAF policy</span></span>

### <span data-ttu-id="82ef0-114">Esempio 2: aggiornare un criterio di WAF esistente</span><span class="sxs-lookup"><span data-stu-id="82ef0-114">Example 2: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -InputObject $policy1 -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="82ef0-115">aggiornare un criterio di WAF esistente</span><span class="sxs-lookup"><span data-stu-id="82ef0-115">update an existing WAF policy</span></span>

### <span data-ttu-id="82ef0-116">Esempio 3: aggiornare un criterio di WAF esistente</span><span class="sxs-lookup"><span data-stu-id="82ef0-116">Example 3: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -ResourceId $resourcdId -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="82ef0-117">aggiornare un criterio di WAF esistente</span><span class="sxs-lookup"><span data-stu-id="82ef0-117">update an existing WAF policy</span></span>

### <span data-ttu-id="82ef0-118">Esempio 4: aggiornare tutti i criteri di WAF in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="82ef0-118">Example 4: update all WAF policies in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Set-AzureRmFrontDoorFireWallPolicy -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode
```

<span data-ttu-id="82ef0-119">aggiornare tutti i criteri di WAF in $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="82ef0-119">update all WAF policies in $resourceGroup</span></span>

## <span data-ttu-id="82ef0-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="82ef0-120">PARAMETERS</span></span>

### <span data-ttu-id="82ef0-121">-Customrule</span><span class="sxs-lookup"><span data-stu-id="82ef0-121">-Customrule</span></span>
<span data-ttu-id="82ef0-122">Regole personalizzate all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="82ef0-122">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="82ef0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ef0-123">-DefaultProfile</span></span>
<span data-ttu-id="82ef0-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82ef0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ef0-125">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="82ef0-125">-EnabledState</span></span>
<span data-ttu-id="82ef0-126">Se il criterio si trova in stato abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="82ef0-126">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="82ef0-127">I valori possibili includono:' disabled ',' Enabled '</span><span class="sxs-lookup"><span data-stu-id="82ef0-127">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="82ef0-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82ef0-128">-InputObject</span></span>
<span data-ttu-id="82ef0-129">L'oggetto FireWallPolicy da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="82ef0-129">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="82ef0-130">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="82ef0-130">-ManagedRule</span></span>
<span data-ttu-id="82ef0-131">Regole gestite all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="82ef0-131">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="82ef0-132">-Modalità</span><span class="sxs-lookup"><span data-stu-id="82ef0-132">-Mode</span></span>
<span data-ttu-id="82ef0-133">Descrive se è in modalità di rilevamento o prevenzione a livello di criteri.</span><span class="sxs-lookup"><span data-stu-id="82ef0-133">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="82ef0-134">I valori possibili includono: "prevenzione", "rilevamento"</span><span class="sxs-lookup"><span data-stu-id="82ef0-134">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="82ef0-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="82ef0-135">-Name</span></span>
<span data-ttu-id="82ef0-136">Il nome del FireWallPolicy da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="82ef0-136">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="82ef0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ef0-137">-ResourceGroupName</span></span>
<span data-ttu-id="82ef0-138">Il gruppo di risorse a cui appartiene FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="82ef0-138">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="82ef0-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82ef0-139">-ResourceId</span></span>
<span data-ttu-id="82ef0-140">ID risorsa di FireWallPolicy da aggiornare</span><span class="sxs-lookup"><span data-stu-id="82ef0-140">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82ef0-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="82ef0-141">-Confirm</span></span>
<span data-ttu-id="82ef0-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82ef0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82ef0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ef0-143">-WhatIf</span></span>
<span data-ttu-id="82ef0-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82ef0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82ef0-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="82ef0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82ef0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ef0-146">CommonParameters</span></span>
<span data-ttu-id="82ef0-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82ef0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ef0-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82ef0-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ef0-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="82ef0-149">INPUTS</span></span>

### <span data-ttu-id="82ef0-150">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="82ef0-150">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="82ef0-151">System. String</span><span class="sxs-lookup"><span data-stu-id="82ef0-151">System.String</span></span>

## <span data-ttu-id="82ef0-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82ef0-152">OUTPUTS</span></span>

### <span data-ttu-id="82ef0-153">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="82ef0-153">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="82ef0-154">Note</span><span class="sxs-lookup"><span data-stu-id="82ef0-154">NOTES</span></span>

## <span data-ttu-id="82ef0-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82ef0-155">RELATED LINKS</span></span>

<span data-ttu-id="82ef0-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="82ef0-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
