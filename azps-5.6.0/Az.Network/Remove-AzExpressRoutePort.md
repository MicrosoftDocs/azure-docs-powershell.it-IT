---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: c0110186277df7e41b9110b1cfdf2fa7b948b50e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996378"
---
# <span data-ttu-id="b7ab0-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b7ab0-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="b7ab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ab0-103">Rimuove un expressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="b7ab0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7ab0-104">SYNTAX</span></span>

### <span data-ttu-id="b7ab0-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7ab0-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ab0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ab0-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ab0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ab0-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7ab0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b7ab0-108">DESCRIPTION</span></span>
<span data-ttu-id="b7ab0-109">Il cmdlet **Remove-AzExpressRoutePort** rimuove un ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="b7ab0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7ab0-110">EXAMPLES</span></span>

### <span data-ttu-id="b7ab0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b7ab0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="b7ab0-112">Rimuove $PortName risorsa ExpressRoutePort nel $rg risorse della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="b7ab0-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b7ab0-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="b7ab0-114">Rimuove la risorsa ExpressRoutePort in InputObject.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="b7ab0-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b7ab0-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="b7ab0-116">Rimuove la risorsa ExpressRoutePort con resourceId $id.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="b7ab0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7ab0-117">PARAMETERS</span></span>

### <span data-ttu-id="b7ab0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7ab0-118">-AsJob</span></span>
<span data-ttu-id="b7ab0-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b7ab0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7ab0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ab0-120">-DefaultProfile</span></span>
<span data-ttu-id="b7ab0-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7ab0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b7ab0-122">-Force</span></span>
<span data-ttu-id="b7ab0-123">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="b7ab0-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="b7ab0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7ab0-124">-InputObject</span></span>
<span data-ttu-id="b7ab0-125">Oggetto porta Express Route</span><span class="sxs-lookup"><span data-stu-id="b7ab0-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ab0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b7ab0-126">-Name</span></span>
<span data-ttu-id="b7ab0-127">Nome di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-127">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ab0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7ab0-128">-PassThru</span></span>
<span data-ttu-id="b7ab0-129">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b7ab0-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7ab0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ab0-131">-ResourceGroupName</span></span>
<span data-ttu-id="b7ab0-132">Nome del gruppo di risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ab0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ab0-133">-ResourceId</span></span>
<span data-ttu-id="b7ab0-134">ResourceId della porta express route.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="b7ab0-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7ab0-135">-Confirm</span></span>
<span data-ttu-id="b7ab0-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7ab0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ab0-137">-WhatIf</span></span>
<span data-ttu-id="b7ab0-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7ab0-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7ab0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ab0-140">CommonParameters</span></span>
<span data-ttu-id="b7ab0-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ab0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ab0-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7ab0-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ab0-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="b7ab0-143">INPUTS</span></span>

### <span data-ttu-id="b7ab0-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b7ab0-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="b7ab0-145">System.String</span><span class="sxs-lookup"><span data-stu-id="b7ab0-145">System.String</span></span>

## <span data-ttu-id="b7ab0-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7ab0-146">OUTPUTS</span></span>

### <span data-ttu-id="b7ab0-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b7ab0-147">System.Boolean</span></span>

## <span data-ttu-id="b7ab0-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="b7ab0-148">NOTES</span></span>

## <span data-ttu-id="b7ab0-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7ab0-149">RELATED LINKS</span></span>

[<span data-ttu-id="b7ab0-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b7ab0-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="b7ab0-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b7ab0-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="b7ab0-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b7ab0-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
