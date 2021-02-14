---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195159"
---
# <span data-ttu-id="0e766-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="0e766-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="0e766-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e766-102">SYNOPSIS</span></span>
<span data-ttu-id="0e766-103">Rimuove un gruppo di origini CDN</span><span class="sxs-lookup"><span data-stu-id="0e766-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="0e766-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e766-104">SYNTAX</span></span>

### <span data-ttu-id="0e766-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0e766-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e766-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e766-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e766-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e766-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e766-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0e766-108">DESCRIPTION</span></span>
<span data-ttu-id="0e766-109">Remove-AzCdnOriginGroup rimuoverà un gruppo di origini CDN dall'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="0e766-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="0e766-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e766-110">EXAMPLES</span></span>

### <span data-ttu-id="0e766-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0e766-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="0e766-112">Questo cmdlet rimuoverà il gruppo di origine specificato dall'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="0e766-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="0e766-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e766-113">PARAMETERS</span></span>

### <span data-ttu-id="0e766-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="0e766-114">-CdnOriginGroup</span></span>
<span data-ttu-id="0e766-115">Oggetto gruppo origine CDN.</span><span class="sxs-lookup"><span data-stu-id="0e766-115">The CDN origin group object.</span></span>

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

### <span data-ttu-id="0e766-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e766-116">-DefaultProfile</span></span>
<span data-ttu-id="0e766-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e766-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e766-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0e766-118">-EndpointName</span></span>
<span data-ttu-id="0e766-119">Nome dell'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e766-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="0e766-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="0e766-120">-OriginGroupName</span></span>
<span data-ttu-id="0e766-121">Nome del gruppo di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e766-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="0e766-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e766-122">-PassThru</span></span>
<span data-ttu-id="0e766-123">Oggetto restituito, se specificato.</span><span class="sxs-lookup"><span data-stu-id="0e766-123">Return object if specified.</span></span>

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

### <span data-ttu-id="0e766-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0e766-124">-ProfileName</span></span>
<span data-ttu-id="0e766-125">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e766-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="0e766-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e766-126">-ResourceGroupName</span></span>
<span data-ttu-id="0e766-127">Gruppo di risorse del profilo della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e766-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="0e766-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e766-128">-ResourceId</span></span>
<span data-ttu-id="0e766-129">ID risorsa del gruppo di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e766-129">The resource id of the Azure CDN origin group.</span></span>

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

### <span data-ttu-id="0e766-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e766-130">-Confirm</span></span>
<span data-ttu-id="0e766-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e766-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e766-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e766-132">-WhatIf</span></span>
<span data-ttu-id="0e766-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e766-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e766-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e766-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e766-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e766-135">CommonParameters</span></span>
<span data-ttu-id="0e766-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e766-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e766-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0e766-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e766-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="0e766-138">INPUTS</span></span>

### <span data-ttu-id="0e766-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0e766-139">None</span></span>

## <span data-ttu-id="0e766-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e766-140">OUTPUTS</span></span>

### <span data-ttu-id="0e766-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0e766-141">System.Boolean</span></span>

## <span data-ttu-id="0e766-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="0e766-142">NOTES</span></span>

## <span data-ttu-id="0e766-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e766-143">RELATED LINKS</span></span>
