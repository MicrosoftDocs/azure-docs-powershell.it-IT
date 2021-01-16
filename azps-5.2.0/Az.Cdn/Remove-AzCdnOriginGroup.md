---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336760"
---
# <span data-ttu-id="1962a-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="1962a-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="1962a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1962a-102">SYNOPSIS</span></span>
<span data-ttu-id="1962a-103">Rimuove un gruppo di origini CDN</span><span class="sxs-lookup"><span data-stu-id="1962a-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="1962a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1962a-104">SYNTAX</span></span>

### <span data-ttu-id="1962a-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1962a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1962a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1962a-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1962a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1962a-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1962a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1962a-108">DESCRIPTION</span></span>
<span data-ttu-id="1962a-109">Remove-AzCdnOriginGroup rimuoverà un gruppo di origine CDN dall'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="1962a-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="1962a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1962a-110">EXAMPLES</span></span>

### <span data-ttu-id="1962a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1962a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="1962a-112">Questo cmdlet rimuoverà il gruppo di origine specificato dall'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="1962a-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="1962a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1962a-113">PARAMETERS</span></span>

### <span data-ttu-id="1962a-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="1962a-114">-CdnOriginGroup</span></span>
<span data-ttu-id="1962a-115">Oggetto gruppo origine CDN.</span><span class="sxs-lookup"><span data-stu-id="1962a-115">The CDN origin group object.</span></span>

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

### <span data-ttu-id="1962a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1962a-116">-DefaultProfile</span></span>
<span data-ttu-id="1962a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1962a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1962a-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1962a-118">-EndpointName</span></span>
<span data-ttu-id="1962a-119">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="1962a-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="1962a-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="1962a-120">-OriginGroupName</span></span>
<span data-ttu-id="1962a-121">Nome del gruppo origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="1962a-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="1962a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1962a-122">-PassThru</span></span>
<span data-ttu-id="1962a-123">Restituisce l'oggetto se specificato.</span><span class="sxs-lookup"><span data-stu-id="1962a-123">Return object if specified.</span></span>

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

### <span data-ttu-id="1962a-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1962a-124">-ProfileName</span></span>
<span data-ttu-id="1962a-125">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="1962a-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="1962a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1962a-126">-ResourceGroupName</span></span>
<span data-ttu-id="1962a-127">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="1962a-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="1962a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1962a-128">-ResourceId</span></span>
<span data-ttu-id="1962a-129">ID risorsa del gruppo di origini di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="1962a-129">The resource id of the Azure CDN origin group.</span></span>

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

### <span data-ttu-id="1962a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1962a-130">-Confirm</span></span>
<span data-ttu-id="1962a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1962a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1962a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1962a-132">-WhatIf</span></span>
<span data-ttu-id="1962a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1962a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1962a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1962a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1962a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1962a-135">CommonParameters</span></span>
<span data-ttu-id="1962a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1962a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1962a-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1962a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1962a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1962a-138">INPUTS</span></span>

### <span data-ttu-id="1962a-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1962a-139">None</span></span>

## <span data-ttu-id="1962a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1962a-140">OUTPUTS</span></span>

### <span data-ttu-id="1962a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1962a-141">System.Boolean</span></span>

## <span data-ttu-id="1962a-142">Note</span><span class="sxs-lookup"><span data-stu-id="1962a-142">NOTES</span></span>

## <span data-ttu-id="1962a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1962a-143">RELATED LINKS</span></span>
