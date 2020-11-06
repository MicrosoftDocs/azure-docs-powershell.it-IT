---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: d3e33e8bf6dea2e06e8ee72199e040a563d0d974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510071"
---
# <span data-ttu-id="0813f-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0813f-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="0813f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0813f-102">SYNOPSIS</span></span>
<span data-ttu-id="0813f-103">Ottiene un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="0813f-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0813f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0813f-104">SYNTAX</span></span>

### <span data-ttu-id="0813f-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0813f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0813f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0813f-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0813f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0813f-107">DESCRIPTION</span></span>
<span data-ttu-id="0813f-108">Il cmdlet **Get-AzureRMCdnEndpoint** ottiene un endpoint della rete di distribuzione del contenuto di Azure (CDN) e i dati di configurazione associati.</span><span class="sxs-lookup"><span data-stu-id="0813f-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="0813f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0813f-109">EXAMPLES</span></span>

## <span data-ttu-id="0813f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0813f-110">PARAMETERS</span></span>

### <span data-ttu-id="0813f-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="0813f-111">-CdnProfile</span></span>
<span data-ttu-id="0813f-112">Specifica l'oggetto del profilo CDN a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="0813f-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0813f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0813f-113">-DefaultProfile</span></span>
<span data-ttu-id="0813f-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0813f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0813f-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0813f-115">-EndpointName</span></span>
<span data-ttu-id="0813f-116">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="0813f-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="0813f-117">Il nome dell'endpoint non è il nome host dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="0813f-117">The name of the endpoint is not the host name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0813f-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0813f-118">-ProfileName</span></span>
<span data-ttu-id="0813f-119">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="0813f-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="0813f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0813f-120">-ResourceGroupName</span></span>
<span data-ttu-id="0813f-121">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="0813f-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="0813f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0813f-122">CommonParameters</span></span>
<span data-ttu-id="0813f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0813f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0813f-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0813f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0813f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0813f-125">INPUTS</span></span>

### <span data-ttu-id="0813f-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="0813f-126">PSProfile</span></span>
<span data-ttu-id="0813f-127">Il parametro ' CdnProfile ' accetta il valore di tipo ' PSProfile ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0813f-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="0813f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0813f-128">OUTPUTS</span></span>

###  
<span data-ttu-id="0813f-129">Questo cmdlet restituisce un oggetto endpoint.</span><span class="sxs-lookup"><span data-stu-id="0813f-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="0813f-130">Note</span><span class="sxs-lookup"><span data-stu-id="0813f-130">NOTES</span></span>

## <span data-ttu-id="0813f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0813f-131">RELATED LINKS</span></span>

[<span data-ttu-id="0813f-132">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0813f-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0813f-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0813f-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0813f-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0813f-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0813f-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0813f-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0813f-136">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0813f-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


