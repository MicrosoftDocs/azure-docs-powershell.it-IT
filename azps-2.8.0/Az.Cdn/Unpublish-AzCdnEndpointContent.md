---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: 6a5a0925967895514de8b7e5294c81571b1cbaba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675515"
---
# <span data-ttu-id="4211b-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="4211b-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="4211b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4211b-102">SYNOPSIS</span></span>
<span data-ttu-id="4211b-103">Elimina un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="4211b-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="4211b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4211b-104">SYNTAX</span></span>

### <span data-ttu-id="4211b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4211b-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4211b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4211b-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4211b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4211b-107">DESCRIPTION</span></span>
<span data-ttu-id="4211b-108">Il cmdlet **Unpublish-AzCdnEndpointContent** Elimina il contenuto da un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="4211b-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="4211b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4211b-109">EXAMPLES</span></span>

## <span data-ttu-id="4211b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4211b-110">PARAMETERS</span></span>

### <span data-ttu-id="4211b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4211b-111">-CdnEndpoint</span></span>
<span data-ttu-id="4211b-112">Specifica l'endpoint che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="4211b-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="4211b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4211b-113">-DefaultProfile</span></span>
<span data-ttu-id="4211b-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4211b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4211b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4211b-115">-EndpointName</span></span>
<span data-ttu-id="4211b-116">Specifica il nome dell'endpoint che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="4211b-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="4211b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4211b-117">-PassThru</span></span>
<span data-ttu-id="4211b-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="4211b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4211b-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="4211b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4211b-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4211b-120">-ProfileName</span></span>
<span data-ttu-id="4211b-121">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="4211b-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="4211b-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="4211b-122">-PurgeContent</span></span>
<span data-ttu-id="4211b-123">Specifica una matrice di percorsi relativi per il contenuto nel server di origine che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="4211b-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="4211b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4211b-124">-ResourceGroupName</span></span>
<span data-ttu-id="4211b-125">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="4211b-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="4211b-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4211b-126">-Confirm</span></span>
<span data-ttu-id="4211b-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4211b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4211b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4211b-128">-WhatIf</span></span>
<span data-ttu-id="4211b-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4211b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4211b-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4211b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4211b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4211b-131">CommonParameters</span></span>
<span data-ttu-id="4211b-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4211b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4211b-133">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4211b-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4211b-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4211b-134">INPUTS</span></span>

### <span data-ttu-id="4211b-135">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4211b-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="4211b-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4211b-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4211b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4211b-137">OUTPUTS</span></span>

### <span data-ttu-id="4211b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4211b-138">System.Boolean</span></span>

## <span data-ttu-id="4211b-139">Note</span><span class="sxs-lookup"><span data-stu-id="4211b-139">NOTES</span></span>

## <span data-ttu-id="4211b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4211b-140">RELATED LINKS</span></span>

[<span data-ttu-id="4211b-141">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="4211b-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)

