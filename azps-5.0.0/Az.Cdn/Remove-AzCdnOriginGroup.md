---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202557"
---
# <span data-ttu-id="6173b-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="6173b-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="6173b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6173b-102">SYNOPSIS</span></span>
<span data-ttu-id="6173b-103">Rimuove un gruppo di origini CDN</span><span class="sxs-lookup"><span data-stu-id="6173b-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="6173b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6173b-104">SYNTAX</span></span>

### <span data-ttu-id="6173b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6173b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6173b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6173b-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6173b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6173b-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6173b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6173b-108">DESCRIPTION</span></span>
<span data-ttu-id="6173b-109">Remove-AzCdnOriginGroup rimuoverà un gruppo di origine CDN dall'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="6173b-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="6173b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6173b-110">EXAMPLES</span></span>

### <span data-ttu-id="6173b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6173b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="6173b-112">Questo cmdlet rimuoverà il gruppo di origine specificato dall'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="6173b-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="6173b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6173b-113">PARAMETERS</span></span>

### <span data-ttu-id="6173b-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="6173b-114">-CdnOriginGroup</span></span>
<span data-ttu-id="6173b-115">Oggetto gruppo origine CDN.</span><span class="sxs-lookup"><span data-stu-id="6173b-115">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6173b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6173b-116">-DefaultProfile</span></span>
<span data-ttu-id="6173b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6173b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6173b-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6173b-118">-EndpointName</span></span>
<span data-ttu-id="6173b-119">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="6173b-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="6173b-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="6173b-120">-OriginGroupName</span></span>
<span data-ttu-id="6173b-121">Nome del gruppo origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="6173b-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="6173b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6173b-122">-PassThru</span></span>
<span data-ttu-id="6173b-123">Restituisce l'oggetto se specificato.</span><span class="sxs-lookup"><span data-stu-id="6173b-123">Return object if specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6173b-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6173b-124">-ProfileName</span></span>
<span data-ttu-id="6173b-125">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="6173b-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="6173b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6173b-126">-ResourceGroupName</span></span>
<span data-ttu-id="6173b-127">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="6173b-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="6173b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6173b-128">-ResourceId</span></span>
<span data-ttu-id="6173b-129">ID risorsa del gruppo di origini di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="6173b-129">The resource id of the Azure CDN origin group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6173b-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6173b-130">-Confirm</span></span>
<span data-ttu-id="6173b-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6173b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6173b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6173b-132">-WhatIf</span></span>
<span data-ttu-id="6173b-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6173b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6173b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6173b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6173b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6173b-135">CommonParameters</span></span>
<span data-ttu-id="6173b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6173b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6173b-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6173b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6173b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6173b-138">INPUTS</span></span>

### <span data-ttu-id="6173b-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6173b-139">None</span></span>

## <span data-ttu-id="6173b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6173b-140">OUTPUTS</span></span>

### <span data-ttu-id="6173b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6173b-141">System.Boolean</span></span>

## <span data-ttu-id="6173b-142">Note</span><span class="sxs-lookup"><span data-stu-id="6173b-142">NOTES</span></span>

## <span data-ttu-id="6173b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6173b-143">RELATED LINKS</span></span>
