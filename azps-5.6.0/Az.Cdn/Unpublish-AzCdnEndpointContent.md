---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: 403c91802c70d7d5e6cfb844909dee1ca6956847
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969630"
---
# <span data-ttu-id="dfbeb-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="dfbeb-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="dfbeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfbeb-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbeb-103">Eliminazione dell'endpoint di una rete CDN.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="dfbeb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfbeb-104">SYNTAX</span></span>

### <span data-ttu-id="dfbeb-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dfbeb-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfbeb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfbeb-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfbeb-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dfbeb-107">DESCRIPTION</span></span>
<span data-ttu-id="dfbeb-108">Il cmdlet **Unpublish-AzCdnEndpointContent** elimina il contenuto da un endpoint della rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="dfbeb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfbeb-109">EXAMPLES</span></span>

## <span data-ttu-id="dfbeb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfbeb-110">PARAMETERS</span></span>

### <span data-ttu-id="dfbeb-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dfbeb-111">-CdnEndpoint</span></span>
<span data-ttu-id="dfbeb-112">Specifica l'endpoint che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-112">Specifies the endpoint that this cmdlet purges.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbeb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbeb-113">-DefaultProfile</span></span>
<span data-ttu-id="dfbeb-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dfbeb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfbeb-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dfbeb-115">-EndpointName</span></span>
<span data-ttu-id="dfbeb-116">Specifica il nome dell'endpoint che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="dfbeb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfbeb-117">-PassThru</span></span>
<span data-ttu-id="dfbeb-118">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dfbeb-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dfbeb-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="dfbeb-120">-ProfileName</span></span>
<span data-ttu-id="dfbeb-121">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="dfbeb-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="dfbeb-122">-PurgeContent</span></span>
<span data-ttu-id="dfbeb-123">Specifica una matrice di percorsi relativi per il contenuto nel server di origine che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbeb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfbeb-124">-ResourceGroupName</span></span>
<span data-ttu-id="dfbeb-125">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="dfbeb-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfbeb-126">-Confirm</span></span>
<span data-ttu-id="dfbeb-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbeb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfbeb-128">-WhatIf</span></span>
<span data-ttu-id="dfbeb-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfbeb-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbeb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbeb-131">CommonParameters</span></span>
<span data-ttu-id="dfbeb-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbeb-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dfbeb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbeb-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="dfbeb-134">INPUTS</span></span>

### <span data-ttu-id="dfbeb-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="dfbeb-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="dfbeb-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dfbeb-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dfbeb-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfbeb-137">OUTPUTS</span></span>

### <span data-ttu-id="dfbeb-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dfbeb-138">System.Boolean</span></span>

## <span data-ttu-id="dfbeb-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="dfbeb-139">NOTES</span></span>

## <span data-ttu-id="dfbeb-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfbeb-140">RELATED LINKS</span></span>

[<span data-ttu-id="dfbeb-141">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="dfbeb-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


