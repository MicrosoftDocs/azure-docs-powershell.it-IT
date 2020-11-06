---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRoutePort.md
ms.openlocfilehash: 5a9e4f7a4a3d7b8173cf7ef797edfc354d655cc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513636"
---
# <span data-ttu-id="f5a61-101">Remove-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f5a61-101">Remove-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="f5a61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f5a61-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a61-103">Rimuove un ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f5a61-103">Removes an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5a61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5a61-104">SYNTAX</span></span>

### <span data-ttu-id="f5a61-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f5a61-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a61-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5a61-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a61-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5a61-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5a61-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5a61-108">DESCRIPTION</span></span>
<span data-ttu-id="f5a61-109">Il cmdlet **Remove-AzureRmExpressRoutePort** rimuove un ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f5a61-109">The **Remove-AzureRmExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="f5a61-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5a61-110">EXAMPLES</span></span>

### <span data-ttu-id="f5a61-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f5a61-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="f5a61-112">Rimuove $PortName risorsa ExpressRoutePort in $rg gruppo di risorse nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f5a61-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="f5a61-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f5a61-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -InputObject $erPort
```
<span data-ttu-id="f5a61-114">Rimuove la risorsa ExpressRoutePort in InputObject.</span><span class="sxs-lookup"><span data-stu-id="f5a61-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="f5a61-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f5a61-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzureRmExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="f5a61-116">Rimuove la risorsa ExpressRoutePort con ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="f5a61-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="f5a61-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f5a61-117">PARAMETERS</span></span>

### <span data-ttu-id="f5a61-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5a61-118">-AsJob</span></span>
<span data-ttu-id="f5a61-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f5a61-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5a61-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a61-120">-DefaultProfile</span></span>
<span data-ttu-id="f5a61-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5a61-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5a61-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f5a61-122">-Force</span></span>
<span data-ttu-id="f5a61-123">Non chiedere conferma se si vuole eliminare una risorsa</span><span class="sxs-lookup"><span data-stu-id="f5a61-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="f5a61-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5a61-124">-InputObject</span></span>
<span data-ttu-id="f5a61-125">L'oggetto porta Route espressa</span><span class="sxs-lookup"><span data-stu-id="f5a61-125">The express route port object</span></span>

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

### <span data-ttu-id="f5a61-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5a61-126">-Name</span></span>
<span data-ttu-id="f5a61-127">Il nome del ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f5a61-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="f5a61-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5a61-128">-PassThru</span></span>
<span data-ttu-id="f5a61-129">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f5a61-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f5a61-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f5a61-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5a61-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a61-131">-ResourceGroupName</span></span>
<span data-ttu-id="f5a61-132">Nome del gruppo di risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="f5a61-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="f5a61-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5a61-133">-ResourceId</span></span>
<span data-ttu-id="f5a61-134">ResourceId della porta di route espressa.</span><span class="sxs-lookup"><span data-stu-id="f5a61-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="f5a61-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f5a61-135">-Confirm</span></span>
<span data-ttu-id="f5a61-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5a61-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5a61-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5a61-137">-WhatIf</span></span>
<span data-ttu-id="f5a61-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5a61-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5a61-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5a61-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5a61-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a61-140">CommonParameters</span></span>
<span data-ttu-id="f5a61-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5a61-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a61-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5a61-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a61-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f5a61-143">INPUTS</span></span>

### <span data-ttu-id="f5a61-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f5a61-144">System.String</span></span>

### <span data-ttu-id="f5a61-145">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f5a61-145">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="f5a61-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5a61-146">OUTPUTS</span></span>

### <span data-ttu-id="f5a61-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="f5a61-147">System.Object</span></span>
## <span data-ttu-id="f5a61-148">Note</span><span class="sxs-lookup"><span data-stu-id="f5a61-148">NOTES</span></span>

## <span data-ttu-id="f5a61-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5a61-149">RELATED LINKS</span></span>
