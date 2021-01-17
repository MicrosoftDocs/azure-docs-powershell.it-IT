---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478023"
---
# <span data-ttu-id="9f51b-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f51b-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="9f51b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f51b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f51b-103">Ottiene un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="9f51b-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="9f51b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f51b-104">SYNTAX</span></span>

### <span data-ttu-id="9f51b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9f51b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f51b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f51b-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f51b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f51b-107">DESCRIPTION</span></span>
<span data-ttu-id="9f51b-108">Il cmdlet **Get-AzCdnEndpoint** ottiene un endpoint della rete di distribuzione del contenuto di Azure (CDN) e i dati di configurazione associati.</span><span class="sxs-lookup"><span data-stu-id="9f51b-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="9f51b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f51b-109">EXAMPLES</span></span>

## <span data-ttu-id="9f51b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f51b-110">PARAMETERS</span></span>

### <span data-ttu-id="9f51b-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="9f51b-111">-CdnProfile</span></span>
<span data-ttu-id="9f51b-112">Specifica l'oggetto del profilo CDN a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="9f51b-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f51b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f51b-113">-DefaultProfile</span></span>
<span data-ttu-id="9f51b-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9f51b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f51b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9f51b-115">-EndpointName</span></span>
<span data-ttu-id="9f51b-116">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="9f51b-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="9f51b-117">Il nome dell'endpoint non è il nome host dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="9f51b-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="9f51b-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9f51b-118">-ProfileName</span></span>
<span data-ttu-id="9f51b-119">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="9f51b-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="9f51b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f51b-120">-ResourceGroupName</span></span>
<span data-ttu-id="9f51b-121">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="9f51b-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="9f51b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f51b-122">CommonParameters</span></span>
<span data-ttu-id="9f51b-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f51b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f51b-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f51b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f51b-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f51b-125">INPUTS</span></span>

### <span data-ttu-id="9f51b-126">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="9f51b-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="9f51b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f51b-127">OUTPUTS</span></span>

### <span data-ttu-id="9f51b-128">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f51b-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9f51b-129">Note</span><span class="sxs-lookup"><span data-stu-id="9f51b-129">NOTES</span></span>

## <span data-ttu-id="9f51b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f51b-130">RELATED LINKS</span></span>

[<span data-ttu-id="9f51b-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f51b-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="9f51b-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f51b-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="9f51b-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f51b-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="9f51b-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f51b-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="9f51b-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f51b-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


