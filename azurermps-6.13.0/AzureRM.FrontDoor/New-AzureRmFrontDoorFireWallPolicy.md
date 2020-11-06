---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: b18f17830dd08f95c3d887ce272ff31e080001a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521374"
---
# <span data-ttu-id="fb3d3-101">New-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="fb3d3-101">New-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="fb3d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb3d3-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3d3-103">Creare criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="fb3d3-103">Create WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb3d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb3d3-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb3d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb3d3-105">DESCRIPTION</span></span>
<span data-ttu-id="fb3d3-106">Il cmdlet **New-AzureRmFrontDoorFireWallPolicy** crea un nuovo criterio di Azure WAF nel gruppo di risorse specificato in abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="fb3d3-106">The **New-AzureRmFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="fb3d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb3d3-107">EXAMPLES</span></span>

### <span data-ttu-id="fb3d3-108">Esempio 1: creare criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="fb3d3-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroupName -Customrule $customRule1 -ManagedRule $managedRule1 -En
abledState Enabled -Mode Prevention


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

<span data-ttu-id="fb3d3-109">Creare criteri di WAF</span><span class="sxs-lookup"><span data-stu-id="fb3d3-109">Create WAF policy</span></span>

## <span data-ttu-id="fb3d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb3d3-110">PARAMETERS</span></span>

### <span data-ttu-id="fb3d3-111">-Customrule</span><span class="sxs-lookup"><span data-stu-id="fb3d3-111">-Customrule</span></span>
<span data-ttu-id="fb3d3-112">Regole personalizzate all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="fb3d3-112">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="fb3d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3d3-113">-DefaultProfile</span></span>
<span data-ttu-id="fb3d3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb3d3-115">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="fb3d3-115">-EnabledState</span></span>
<span data-ttu-id="fb3d3-116">Se il criterio si trova in stato abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-116">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="fb3d3-117">I valori possibili includono:' disabled ',' Enabled '</span><span class="sxs-lookup"><span data-stu-id="fb3d3-117">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="fb3d3-118">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="fb3d3-118">-ManagedRule</span></span>
<span data-ttu-id="fb3d3-119">Regole gestite all'interno del criterio</span><span class="sxs-lookup"><span data-stu-id="fb3d3-119">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="fb3d3-120">-Modalità</span><span class="sxs-lookup"><span data-stu-id="fb3d3-120">-Mode</span></span>
<span data-ttu-id="fb3d3-121">Descrive se è in modalità di rilevamento o prevenzione a livello di criteri.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-121">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="fb3d3-122">I valori possibili includono: "prevenzione", "rilevamento"</span><span class="sxs-lookup"><span data-stu-id="fb3d3-122">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="fb3d3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb3d3-123">-Name</span></span>
<span data-ttu-id="fb3d3-124">Nome WebApplicationFireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-124">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="fb3d3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3d3-125">-ResourceGroupName</span></span>
<span data-ttu-id="fb3d3-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fb3d3-126">The resource group name</span></span>

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

### <span data-ttu-id="fb3d3-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb3d3-127">-Confirm</span></span>
<span data-ttu-id="fb3d3-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb3d3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3d3-129">-WhatIf</span></span>
<span data-ttu-id="fb3d3-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb3d3-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb3d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3d3-132">CommonParameters</span></span>
<span data-ttu-id="fb3d3-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb3d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3d3-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb3d3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3d3-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb3d3-135">INPUTS</span></span>

### <span data-ttu-id="fb3d3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fb3d3-136">System.String</span></span>

## <span data-ttu-id="fb3d3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb3d3-137">OUTPUTS</span></span>

### <span data-ttu-id="fb3d3-138">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="fb3d3-138">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="fb3d3-139">Note</span><span class="sxs-lookup"><span data-stu-id="fb3d3-139">NOTES</span></span>

## <span data-ttu-id="fb3d3-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb3d3-140">RELATED LINKS</span></span>

<span data-ttu-id="fb3d3-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="fb3d3-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
