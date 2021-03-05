---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 703b01ef012f77126e0db3d425cd892fa7256317
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964718"
---
# <span data-ttu-id="0fa8d-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0fa8d-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="0fa8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fa8d-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa8d-103">Rimuove un dominio della griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="0fa8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fa8d-104">SYNTAX</span></span>

### <span data-ttu-id="0fa8d-105">DomainNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0fa8d-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fa8d-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa8d-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fa8d-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fa8d-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fa8d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0fa8d-108">DESCRIPTION</span></span>
<span data-ttu-id="0fa8d-109">Rimuove un dominio della griglia eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="0fa8d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fa8d-110">EXAMPLES</span></span>

### <span data-ttu-id="0fa8d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0fa8d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="0fa8d-112">Rimuove il dominio della griglia eventi \` Domain1 \` nel gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="0fa8d-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="0fa8d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0fa8d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="0fa8d-114">Rimuove il dominio della griglia eventi \` Domain1 \` nel gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="0fa8d-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="0fa8d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fa8d-115">PARAMETERS</span></span>

### <span data-ttu-id="0fa8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa8d-116">-DefaultProfile</span></span>
<span data-ttu-id="0fa8d-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fa8d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fa8d-118">-InputObject</span></span>
<span data-ttu-id="0fa8d-119">Oggetto Dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fa8d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0fa8d-120">-Name</span></span>
<span data-ttu-id="0fa8d-121">Nome di dominio EventGrid.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fa8d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fa8d-122">-PassThru</span></span>
<span data-ttu-id="0fa8d-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0fa8d-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0fa8d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fa8d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0fa8d-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fa8d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fa8d-126">-ResourceId</span></span>
<span data-ttu-id="0fa8d-127">Identificatore di risorsa che rappresenta il dominio della griglia eventi.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-127">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fa8d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fa8d-128">-Confirm</span></span>
<span data-ttu-id="0fa8d-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fa8d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fa8d-130">-WhatIf</span></span>
<span data-ttu-id="0fa8d-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fa8d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fa8d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa8d-133">CommonParameters</span></span>
<span data-ttu-id="0fa8d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa8d-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0fa8d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa8d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="0fa8d-136">INPUTS</span></span>

### <span data-ttu-id="0fa8d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0fa8d-137">System.String</span></span>

### <span data-ttu-id="0fa8d-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="0fa8d-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="0fa8d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fa8d-139">OUTPUTS</span></span>

### <span data-ttu-id="0fa8d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0fa8d-140">System.Boolean</span></span>

## <span data-ttu-id="0fa8d-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="0fa8d-141">NOTES</span></span>

## <span data-ttu-id="0fa8d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fa8d-142">RELATED LINKS</span></span>
