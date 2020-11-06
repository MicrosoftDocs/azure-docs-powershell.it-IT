---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a774aec8114883d3ba2a5edf189f115f99d3eb4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516991"
---
# <span data-ttu-id="66520-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="66520-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="66520-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66520-102">SYNOPSIS</span></span>
<span data-ttu-id="66520-103">Elimina un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="66520-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66520-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66520-104">SYNTAX</span></span>

### <span data-ttu-id="66520-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="66520-105">Parameter Set for fields parameters (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66520-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="66520-106">Parameter Set for object parameters</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66520-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66520-107">DESCRIPTION</span></span>
<span data-ttu-id="66520-108">Il cmdlet **Unpublish-AzureRmCdnEndpointContent** Elimina il contenuto da un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="66520-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="66520-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66520-109">EXAMPLES</span></span>

## <span data-ttu-id="66520-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66520-110">PARAMETERS</span></span>

### <span data-ttu-id="66520-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="66520-111">-CdnEndpoint</span></span>
<span data-ttu-id="66520-112">Specifica l'endpoint che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="66520-112">Specifies the endpoint that this cmdlet purges.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66520-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="66520-113">-EndpointName</span></span>
<span data-ttu-id="66520-114">Specifica il nome dell'endpoint che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="66520-114">Specifies name of the endpoint that this cmdlet purges.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66520-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66520-115">-PassThru</span></span>
<span data-ttu-id="66520-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="66520-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="66520-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="66520-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="66520-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="66520-118">-ProfileName</span></span>
<span data-ttu-id="66520-119">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="66520-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66520-120">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="66520-120">-PurgeContent</span></span>
<span data-ttu-id="66520-121">Specifica una matrice di percorsi relativi per il contenuto nel server di origine che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="66520-121">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="66520-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66520-122">-ResourceGroupName</span></span>
<span data-ttu-id="66520-123">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="66520-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66520-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="66520-124">-Confirm</span></span>
<span data-ttu-id="66520-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66520-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66520-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66520-126">-WhatIf</span></span>
<span data-ttu-id="66520-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66520-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66520-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="66520-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66520-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66520-129">-DefaultProfile</span></span>
<span data-ttu-id="66520-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66520-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66520-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66520-131">CommonParameters</span></span>
<span data-ttu-id="66520-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66520-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66520-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66520-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66520-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66520-134">INPUTS</span></span>

### <span data-ttu-id="66520-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="66520-135">PSEndpoint</span></span>
<span data-ttu-id="66520-136">Il parametro ' CdnEndpoint ' accetta il valore di tipo ' PSEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="66520-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="66520-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66520-137">OUTPUTS</span></span>

### <span data-ttu-id="66520-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66520-138">System.Boolean</span></span>

## <span data-ttu-id="66520-139">Note</span><span class="sxs-lookup"><span data-stu-id="66520-139">NOTES</span></span>

## <span data-ttu-id="66520-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66520-140">RELATED LINKS</span></span>

[<span data-ttu-id="66520-141">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="66520-141">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)


