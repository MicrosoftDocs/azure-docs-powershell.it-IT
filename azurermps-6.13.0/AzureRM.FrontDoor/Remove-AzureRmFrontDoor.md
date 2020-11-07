---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685431"
---
# <span data-ttu-id="9012a-101">Remove-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="9012a-101">Remove-AzureRmFrontDoor</span></span>

## <span data-ttu-id="9012a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9012a-102">SYNOPSIS</span></span>
<span data-ttu-id="9012a-103">Rimuovere il bilanciamento del carico della porta anteriore</span><span class="sxs-lookup"><span data-stu-id="9012a-103">Remove Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9012a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9012a-104">SYNTAX</span></span>

### <span data-ttu-id="9012a-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9012a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9012a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9012a-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9012a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9012a-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9012a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9012a-108">DESCRIPTION</span></span>
<span data-ttu-id="9012a-109">Il cmdlet **Remove-AzureRmFrontDoor** rimuove un bilanciamento del carico della porta anteriore sotto l'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="9012a-109">The **Remove-AzureRmFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="9012a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9012a-110">EXAMPLES</span></span>

### <span data-ttu-id="9012a-111">Esempio 1: rimuovere "frontdoor1" nel gruppo di risorse "RG1" sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9012a-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="9012a-112">Rimuovere "frontdoor1" nel gruppo di risorse "RG1" sotto l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="9012a-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="9012a-113">Esempio 2: rimuovere tutti i FrontDoors nel gruppo di risorse "RG1" sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9012a-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="9012a-114">Rimuovere tutti i FrontDoors nel gruppo di risorse "RG1" sotto l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="9012a-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="9012a-115">Esempio 3: rimuovere tutti i FrontDoors sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9012a-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

<span data-ttu-id="9012a-116">Rimuovere tutti i FrontDoors sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9012a-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="9012a-117">Esempio 4: rimuovere tutti i FrontDoors con il nome "frontdoor1" sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9012a-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="9012a-118">Rimuovere tutti i FrontDoors con il nome "frontdoor1" sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9012a-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="9012a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9012a-119">PARAMETERS</span></span>

### <span data-ttu-id="9012a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9012a-120">-DefaultProfile</span></span>
<span data-ttu-id="9012a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9012a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9012a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9012a-122">-InputObject</span></span>
<span data-ttu-id="9012a-123">L'oggetto porta principale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="9012a-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="9012a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9012a-124">-Name</span></span>
<span data-ttu-id="9012a-125">Il nome della porta principale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="9012a-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="9012a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9012a-126">-PassThru</span></span>
<span data-ttu-id="9012a-127">Oggetto return (se specificato).</span><span class="sxs-lookup"><span data-stu-id="9012a-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="9012a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9012a-128">-ResourceGroupName</span></span>
<span data-ttu-id="9012a-129">Gruppo di risorse a cui appartiene la porta principale.</span><span class="sxs-lookup"><span data-stu-id="9012a-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="9012a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9012a-130">-ResourceId</span></span>
<span data-ttu-id="9012a-131">ID risorsa della porta principale da eliminare</span><span class="sxs-lookup"><span data-stu-id="9012a-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="9012a-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9012a-132">-Confirm</span></span>
<span data-ttu-id="9012a-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9012a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9012a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9012a-134">-WhatIf</span></span>
<span data-ttu-id="9012a-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9012a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9012a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9012a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9012a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9012a-137">CommonParameters</span></span>
<span data-ttu-id="9012a-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9012a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9012a-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9012a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9012a-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9012a-140">INPUTS</span></span>

### <span data-ttu-id="9012a-141">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="9012a-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="9012a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9012a-142">System.String</span></span>

### <span data-ttu-id="9012a-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9012a-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9012a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9012a-144">OUTPUTS</span></span>

### <span data-ttu-id="9012a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9012a-145">System.Boolean</span></span>

## <span data-ttu-id="9012a-146">Note</span><span class="sxs-lookup"><span data-stu-id="9012a-146">NOTES</span></span>

## <span data-ttu-id="9012a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9012a-147">RELATED LINKS</span></span>

<span data-ttu-id="9012a-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="9012a-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span></span>
