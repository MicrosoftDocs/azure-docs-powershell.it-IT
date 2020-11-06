---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/unpublish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Unpublish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: bb55b858e4c2464cced362357ffbc91a3969b1f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516912"
---
# <span data-ttu-id="50562-101">Unpublish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="50562-101">Unpublish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="50562-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50562-102">SYNOPSIS</span></span>
<span data-ttu-id="50562-103">Elimina un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="50562-103">Purges a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50562-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50562-104">SYNTAX</span></span>

### <span data-ttu-id="50562-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50562-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50562-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50562-106">ByObjectParameterSet</span></span>
```
Unpublish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50562-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50562-107">DESCRIPTION</span></span>
<span data-ttu-id="50562-108">Il cmdlet **Unpublish-AzureRmCdnEndpointContent** Elimina il contenuto da un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="50562-108">The **Unpublish-AzureRmCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="50562-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50562-109">EXAMPLES</span></span>

## <span data-ttu-id="50562-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50562-110">PARAMETERS</span></span>

### <span data-ttu-id="50562-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="50562-111">-CdnEndpoint</span></span>
<span data-ttu-id="50562-112">Specifica l'endpoint che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="50562-112">Specifies the endpoint that this cmdlet purges.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50562-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50562-113">-DefaultProfile</span></span>
<span data-ttu-id="50562-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="50562-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50562-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="50562-115">-EndpointName</span></span>
<span data-ttu-id="50562-116">Specifica il nome dell'endpoint che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="50562-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50562-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50562-117">-PassThru</span></span>
<span data-ttu-id="50562-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="50562-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="50562-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="50562-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50562-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="50562-120">-ProfileName</span></span>
<span data-ttu-id="50562-121">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="50562-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50562-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="50562-122">-PurgeContent</span></span>
<span data-ttu-id="50562-123">Specifica una matrice di percorsi relativi per il contenuto nel server di origine che questo cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="50562-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50562-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50562-124">-ResourceGroupName</span></span>
<span data-ttu-id="50562-125">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="50562-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50562-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50562-126">-Confirm</span></span>
<span data-ttu-id="50562-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50562-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50562-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50562-128">-WhatIf</span></span>
<span data-ttu-id="50562-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50562-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50562-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50562-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50562-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50562-131">CommonParameters</span></span>
<span data-ttu-id="50562-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50562-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50562-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50562-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50562-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50562-134">INPUTS</span></span>

### <span data-ttu-id="50562-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="50562-135">PSEndpoint</span></span>
<span data-ttu-id="50562-136">Il parametro ' CdnEndpoint ' accetta il valore di tipo ' PSEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="50562-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="50562-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50562-137">OUTPUTS</span></span>

### <span data-ttu-id="50562-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50562-138">System.Boolean</span></span>

## <span data-ttu-id="50562-139">Note</span><span class="sxs-lookup"><span data-stu-id="50562-139">NOTES</span></span>

## <span data-ttu-id="50562-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50562-140">RELATED LINKS</span></span>

[<span data-ttu-id="50562-141">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="50562-141">Publish-AzureRmCdnEndpointContent</span></span>](./Publish-AzureRmCdnEndpointContent.md)


