---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/publish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: a4a2479c6dc7c116ff7da9151fcd5dea5ec26660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517539"
---
# <span data-ttu-id="55121-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="55121-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="55121-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55121-102">SYNOPSIS</span></span>
<span data-ttu-id="55121-103">Carica il contenuto in un endpoint.</span><span class="sxs-lookup"><span data-stu-id="55121-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55121-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55121-104">SYNTAX</span></span>

### <span data-ttu-id="55121-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55121-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55121-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55121-106">ByObjectParameterSet</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55121-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55121-107">DESCRIPTION</span></span>
<span data-ttu-id="55121-108">Il cmdlet **Publish-AzureRmCdnEndpointContent** carica il contenuto da un server di origine per l'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="55121-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="55121-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55121-109">EXAMPLES</span></span>

## <span data-ttu-id="55121-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55121-110">PARAMETERS</span></span>

### <span data-ttu-id="55121-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="55121-111">-CdnEndpoint</span></span>
<span data-ttu-id="55121-112">Sepcifies l'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="55121-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="55121-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55121-113">-DefaultProfile</span></span>
<span data-ttu-id="55121-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="55121-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55121-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="55121-115">-EndpointName</span></span>
<span data-ttu-id="55121-116">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="55121-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="55121-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="55121-117">-LoadContent</span></span>
<span data-ttu-id="55121-118">Specifica una matrice di percorsi relativi per il contenuto nel server di origine che questo cmdlet pubblica.</span><span class="sxs-lookup"><span data-stu-id="55121-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="55121-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55121-119">-PassThru</span></span>
<span data-ttu-id="55121-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="55121-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="55121-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="55121-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55121-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="55121-122">-ProfileName</span></span>
<span data-ttu-id="55121-123">Specifica il nome del profilo a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="55121-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="55121-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55121-124">-ResourceGroupName</span></span>
<span data-ttu-id="55121-125">Specifica il nome del gruppo di risorse a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="55121-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="55121-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55121-126">CommonParameters</span></span>
<span data-ttu-id="55121-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55121-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55121-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55121-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55121-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55121-129">INPUTS</span></span>

### <span data-ttu-id="55121-130">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="55121-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="55121-131">Parametri: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="55121-131">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="55121-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55121-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="55121-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55121-133">OUTPUTS</span></span>

### <span data-ttu-id="55121-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55121-134">System.Boolean</span></span>

## <span data-ttu-id="55121-135">Note</span><span class="sxs-lookup"><span data-stu-id="55121-135">NOTES</span></span>

## <span data-ttu-id="55121-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55121-136">RELATED LINKS</span></span>

[<span data-ttu-id="55121-137">Annulla pubblicazione-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="55121-137">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


