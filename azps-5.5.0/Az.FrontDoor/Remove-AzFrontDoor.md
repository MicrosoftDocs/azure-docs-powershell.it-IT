---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185927"
---
# <span data-ttu-id="1c3b2-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="1c3b2-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="1c3b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c3b2-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3b2-103">Rimuovere il bilanciamento del carico anteriore</span><span class="sxs-lookup"><span data-stu-id="1c3b2-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="1c3b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c3b2-104">SYNTAX</span></span>

### <span data-ttu-id="1c3b2-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c3b2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c3b2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c3b2-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c3b2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c3b2-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c3b2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c3b2-108">DESCRIPTION</span></span>
<span data-ttu-id="1c3b2-109">Il cmdlet **Remove-AzFrontDoor** rimuove una bilanciamento del carico front-door nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="1c3b2-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="1c3b2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c3b2-110">EXAMPLES</span></span>

### <span data-ttu-id="1c3b2-111">Esempio 1: Rimuovere "frontdoor1" nel gruppo di risorse "rg1" nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="1c3b2-112">Rimuovere "frontdoor1" nel gruppo di risorse "rg1" nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="1c3b2-113">Esempio 2: Rimuovere tutti i FrontDoor nel gruppo di risorse "rg1" nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="1c3b2-114">Rimuovere tutti i FrontDoor del gruppo di risorse "rg1" nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="1c3b2-115">Esempio 3: Rimuovere tutti i FrontDoor dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="1c3b2-116">Rimuovere tutti i FrontDoor dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="1c3b2-117">Esempio 4: Rimuovere tutti i FrontDoor con nome "frontdoor1" nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="1c3b2-118">Rimuovere tutti i FrontDoor con nome "frontdoor1" nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="1c3b2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c3b2-119">PARAMETERS</span></span>

### <span data-ttu-id="1c3b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3b2-120">-DefaultProfile</span></span>
<span data-ttu-id="1c3b2-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c3b2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c3b2-122">-InputObject</span></span>
<span data-ttu-id="1c3b2-123">L'oggetto Porta anteriore da eliminare.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c3b2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1c3b2-124">-Name</span></span>
<span data-ttu-id="1c3b2-125">Nome della porta anteriore da eliminare.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="1c3b2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c3b2-126">-PassThru</span></span>
<span data-ttu-id="1c3b2-127">Oggetto restituito (se specificato).</span><span class="sxs-lookup"><span data-stu-id="1c3b2-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="1c3b2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3b2-128">-ResourceGroupName</span></span>
<span data-ttu-id="1c3b2-129">Gruppo di risorse a cui appartiene la porta davanti.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="1c3b2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c3b2-130">-ResourceId</span></span>
<span data-ttu-id="1c3b2-131">ID risorsa della porta anteriore da eliminare</span><span class="sxs-lookup"><span data-stu-id="1c3b2-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="1c3b2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c3b2-132">-Confirm</span></span>
<span data-ttu-id="1c3b2-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c3b2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c3b2-134">-WhatIf</span></span>
<span data-ttu-id="1c3b2-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c3b2-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c3b2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3b2-137">CommonParameters</span></span>
<span data-ttu-id="1c3b2-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3b2-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c3b2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3b2-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c3b2-140">INPUTS</span></span>

### <span data-ttu-id="1c3b2-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="1c3b2-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="1c3b2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1c3b2-142">System.String</span></span>

## <span data-ttu-id="1c3b2-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c3b2-143">OUTPUTS</span></span>

### <span data-ttu-id="1c3b2-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1c3b2-144">System.Boolean</span></span>

## <span data-ttu-id="1c3b2-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c3b2-145">NOTES</span></span>

## <span data-ttu-id="1c3b2-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c3b2-146">RELATED LINKS</span></span>

<span data-ttu-id="1c3b2-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="1c3b2-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>