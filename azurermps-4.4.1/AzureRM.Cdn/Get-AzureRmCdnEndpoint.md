---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: 088f9ff5ee1c41b4529353b2740bf9ef1fa8e33c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519625"
---
# <span data-ttu-id="372f9-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="372f9-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="372f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="372f9-102">SYNOPSIS</span></span>
<span data-ttu-id="372f9-103">Ottiene un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="372f9-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="372f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="372f9-104">SYNTAX</span></span>

### <span data-ttu-id="372f9-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="372f9-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="372f9-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="372f9-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="372f9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="372f9-107">DESCRIPTION</span></span>
<span data-ttu-id="372f9-108">Il cmdlet **Get-AzureRMCdnEndpoint** ottiene un endpoint della rete di distribuzione del contenuto di Azure (CDN) e i dati di configurazione associati.</span><span class="sxs-lookup"><span data-stu-id="372f9-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="372f9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="372f9-109">EXAMPLES</span></span>

## <span data-ttu-id="372f9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="372f9-110">PARAMETERS</span></span>

### <span data-ttu-id="372f9-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="372f9-111">-CdnProfile</span></span>
<span data-ttu-id="372f9-112">Specifica l'oggetto del profilo CDN a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="372f9-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="372f9-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="372f9-113">-EndpointName</span></span>
<span data-ttu-id="372f9-114">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="372f9-114">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="372f9-115">Il nome dell'endpoint non è il nome host dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="372f9-115">The name of the endpoint is not the host name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372f9-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="372f9-116">-ProfileName</span></span>
<span data-ttu-id="372f9-117">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="372f9-117">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="372f9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372f9-118">-ResourceGroupName</span></span>
<span data-ttu-id="372f9-119">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="372f9-119">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="372f9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372f9-120">-DefaultProfile</span></span>
<span data-ttu-id="372f9-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="372f9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="372f9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372f9-122">CommonParameters</span></span>
<span data-ttu-id="372f9-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="372f9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372f9-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="372f9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372f9-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="372f9-125">INPUTS</span></span>

### <span data-ttu-id="372f9-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="372f9-126">PSProfile</span></span>
<span data-ttu-id="372f9-127">Il parametro ' CdnProfile ' accetta il valore di tipo ' PSProfile ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="372f9-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="372f9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="372f9-128">OUTPUTS</span></span>

###  
<span data-ttu-id="372f9-129">Questo cmdlet restituisce un oggetto endpoint.</span><span class="sxs-lookup"><span data-stu-id="372f9-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="372f9-130">Note</span><span class="sxs-lookup"><span data-stu-id="372f9-130">NOTES</span></span>

## <span data-ttu-id="372f9-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="372f9-131">RELATED LINKS</span></span>

[<span data-ttu-id="372f9-132">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="372f9-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="372f9-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="372f9-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="372f9-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="372f9-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="372f9-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="372f9-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="372f9-136">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="372f9-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


