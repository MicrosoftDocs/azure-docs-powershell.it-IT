---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332224"
---
# <span data-ttu-id="660f0-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="660f0-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="660f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="660f0-102">SYNOPSIS</span></span>
<span data-ttu-id="660f0-103">Rimuovere il bilanciamento del carico della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="660f0-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="660f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="660f0-104">SYNTAX</span></span>

### <span data-ttu-id="660f0-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="660f0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="660f0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="660f0-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="660f0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="660f0-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="660f0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="660f0-108">DESCRIPTION</span></span>
<span data-ttu-id="660f0-109">Il cmdlet **Remove-AzFrontDoor** rimuove un bilanciamento del carico della porta anteriore sotto l'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="660f0-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="660f0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="660f0-110">EXAMPLES</span></span>

### <span data-ttu-id="660f0-111">Esempio 1: rimuovere "frontdoor1" nel gruppo di risorse "RG1" sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="660f0-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="660f0-112">Rimuovere "frontdoor1" nel gruppo di risorse "RG1" sotto l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="660f0-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="660f0-113">Esempio 2: rimuovere tutti i FrontDoors nel gruppo di risorse "RG1" sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="660f0-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="660f0-114">Rimuovere tutti i FrontDoors nel gruppo di risorse "RG1" sotto l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="660f0-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="660f0-115">Esempio 3: rimuovere tutti i FrontDoors sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="660f0-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="660f0-116">Rimuovere tutti i FrontDoors sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="660f0-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="660f0-117">Esempio 4: rimuovere tutti i FrontDoors con il nome "frontdoor1" sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="660f0-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="660f0-118">Rimuovere tutti i FrontDoors con il nome "frontdoor1" sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="660f0-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="660f0-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="660f0-119">PARAMETERS</span></span>

### <span data-ttu-id="660f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660f0-120">-DefaultProfile</span></span>
<span data-ttu-id="660f0-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="660f0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="660f0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="660f0-122">-InputObject</span></span>
<span data-ttu-id="660f0-123">L'oggetto porta principale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="660f0-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="660f0-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="660f0-124">-Name</span></span>
<span data-ttu-id="660f0-125">Il nome della porta principale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="660f0-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="660f0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="660f0-126">-PassThru</span></span>
<span data-ttu-id="660f0-127">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="660f0-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="660f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="660f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="660f0-129">Gruppo di risorse a cui appartiene la porta principale.</span><span class="sxs-lookup"><span data-stu-id="660f0-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="660f0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="660f0-130">-ResourceId</span></span>
<span data-ttu-id="660f0-131">ID risorsa della porta principale da eliminare</span><span class="sxs-lookup"><span data-stu-id="660f0-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="660f0-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="660f0-132">-Confirm</span></span>
<span data-ttu-id="660f0-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="660f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="660f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="660f0-134">-WhatIf</span></span>
<span data-ttu-id="660f0-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="660f0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="660f0-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="660f0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="660f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660f0-137">CommonParameters</span></span>
<span data-ttu-id="660f0-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660f0-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="660f0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660f0-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="660f0-140">INPUTS</span></span>

### <span data-ttu-id="660f0-141">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="660f0-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="660f0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="660f0-142">System.String</span></span>

## <span data-ttu-id="660f0-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="660f0-143">OUTPUTS</span></span>

### <span data-ttu-id="660f0-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="660f0-144">System.Boolean</span></span>

## <span data-ttu-id="660f0-145">Note</span><span class="sxs-lookup"><span data-stu-id="660f0-145">NOTES</span></span>

## <span data-ttu-id="660f0-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="660f0-146">RELATED LINKS</span></span>

<span data-ttu-id="660f0-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="660f0-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>