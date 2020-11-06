---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Publish-AzureRmCdnEndpointContent.md
ms.openlocfilehash: 1df36c7816894f8ccfc642eac307a84b485ba7ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519615"
---
# <span data-ttu-id="3b81f-101">Publish-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3b81f-101">Publish-AzureRmCdnEndpointContent</span></span>

## <span data-ttu-id="3b81f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b81f-102">SYNOPSIS</span></span>
<span data-ttu-id="3b81f-103">Carica il contenuto in un endpoint.</span><span class="sxs-lookup"><span data-stu-id="3b81f-103">Loads content to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b81f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b81f-104">SYNTAX</span></span>

### <span data-ttu-id="3b81f-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b81f-105">Parameter Set for fields parameters (Default)</span></span>
```
Publish-AzureRmCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b81f-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="3b81f-106">Parameter Set for object parameters</span></span>
```
Publish-AzureRmCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b81f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b81f-107">DESCRIPTION</span></span>
<span data-ttu-id="3b81f-108">Il cmdlet **Publish-AzureRmCdnEndpointContent** carica il contenuto da un server di origine per l'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="3b81f-108">The **Publish-AzureRmCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="3b81f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b81f-109">EXAMPLES</span></span>

## <span data-ttu-id="3b81f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b81f-110">PARAMETERS</span></span>

### <span data-ttu-id="3b81f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b81f-111">-CdnEndpoint</span></span>
<span data-ttu-id="3b81f-112">Sepcifies l'endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="3b81f-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="3b81f-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3b81f-113">-EndpointName</span></span>
<span data-ttu-id="3b81f-114">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="3b81f-114">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="3b81f-115">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="3b81f-115">-LoadContent</span></span>
<span data-ttu-id="3b81f-116">Specifica una matrice di percorsi relativi per il contenuto nel server di origine che questo cmdlet pubblica.</span><span class="sxs-lookup"><span data-stu-id="3b81f-116">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="3b81f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b81f-117">-PassThru</span></span>
<span data-ttu-id="3b81f-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="3b81f-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3b81f-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3b81f-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3b81f-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3b81f-120">-ProfileName</span></span>
<span data-ttu-id="3b81f-121">Specifica il nome del profilo a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="3b81f-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="3b81f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b81f-122">-ResourceGroupName</span></span>
<span data-ttu-id="3b81f-123">Specifica il nome del gruppo di risorse a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="3b81f-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="3b81f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b81f-124">-DefaultProfile</span></span>
<span data-ttu-id="3b81f-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b81f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b81f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b81f-126">CommonParameters</span></span>
<span data-ttu-id="3b81f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b81f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b81f-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b81f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b81f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b81f-129">INPUTS</span></span>

### <span data-ttu-id="3b81f-130">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b81f-130">PSEndpoint</span></span>
<span data-ttu-id="3b81f-131">Il parametro ' CdnEndpoint ' accetta il valore di tipo ' PSEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="3b81f-131">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="3b81f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b81f-132">OUTPUTS</span></span>

### <span data-ttu-id="3b81f-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b81f-133">System.Boolean</span></span>

## <span data-ttu-id="3b81f-134">Note</span><span class="sxs-lookup"><span data-stu-id="3b81f-134">NOTES</span></span>

## <span data-ttu-id="3b81f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b81f-135">RELATED LINKS</span></span>

[<span data-ttu-id="3b81f-136">Annulla pubblicazione-AzureRmCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3b81f-136">Unpublish-AzureRmCdnEndpointContent</span></span>](./Unpublish-AzureRmCdnEndpointContent.md)


