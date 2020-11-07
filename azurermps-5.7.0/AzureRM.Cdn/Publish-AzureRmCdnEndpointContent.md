---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/publish-azurermcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 09bd1ae2c4c16bdc6af5103ec4e2854005961094
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685632"
---
# <span data-ttu-id="a84f9-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="a84f9-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="a84f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a84f9-102">SYNOPSIS</span></span>
<span data-ttu-id="a84f9-103">Carica il contenuto in un endpoint.</span><span class="sxs-lookup"><span data-stu-id="a84f9-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a84f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a84f9-104">SYNTAX</span></span>

### <span data-ttu-id="a84f9-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a84f9-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a84f9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a84f9-106">ByObjectParameterSet</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a84f9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a84f9-107">DESCRIPTION</span></span>
<span data-ttu-id="a84f9-108">Il cmdlet **Publish-AzureRmCdnEndpointContent** carica il contenuto da un server di origine per l'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="a84f9-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a84f9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a84f9-109">EXAMPLES</span></span>

## <span data-ttu-id="a84f9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a84f9-110">PARAMETERS</span></span>

### <span data-ttu-id="a84f9-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a84f9-111">-CdnEndpoint</span></span>
<span data-ttu-id="a84f9-112">Sepcifies l'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="a84f9-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="a84f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a84f9-113">-DefaultProfile</span></span>
<span data-ttu-id="a84f9-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a84f9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a84f9-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a84f9-115">-EndpointName</span></span>
<span data-ttu-id="a84f9-116">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a84f9-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="a84f9-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="a84f9-117">-LoadContent</span></span>
<span data-ttu-id="a84f9-118">Specifica una matrice di percorsi relativi per il contenuto nel server di origine che questo cmdlet pubblica.</span><span class="sxs-lookup"><span data-stu-id="a84f9-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="a84f9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a84f9-119">-PassThru</span></span>
<span data-ttu-id="a84f9-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a84f9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a84f9-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a84f9-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a84f9-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a84f9-122">-ProfileName</span></span>
<span data-ttu-id="a84f9-123">Specifica il nome del profilo a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="a84f9-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a84f9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a84f9-124">-ResourceGroupName</span></span>
<span data-ttu-id="a84f9-125">Specifica il nome del gruppo di risorse a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="a84f9-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="a84f9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a84f9-126">CommonParameters</span></span>
<span data-ttu-id="a84f9-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a84f9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a84f9-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a84f9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a84f9-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a84f9-129">INPUTS</span></span>

### <span data-ttu-id="a84f9-130">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a84f9-130">PSEndpoint</span></span>
<span data-ttu-id="a84f9-131">Il parametro ' CdnEndpoint ' accetta il valore di tipo ' PSEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a84f9-131">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="a84f9-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a84f9-132">OUTPUTS</span></span>

### <span data-ttu-id="a84f9-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a84f9-133">System.Boolean</span></span>

## <span data-ttu-id="a84f9-134">Note</span><span class="sxs-lookup"><span data-stu-id="a84f9-134">NOTES</span></span>

## <span data-ttu-id="a84f9-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a84f9-135">RELATED LINKS</span></span>

[<span data-ttu-id="a84f9-136">Annulla pubblicazione-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="a84f9-136">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


