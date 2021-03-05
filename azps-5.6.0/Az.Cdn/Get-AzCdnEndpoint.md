---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 21aead3d3dd17b380f466ffdeaf2e5c36c9b1235
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994501"
---
# <span data-ttu-id="cb23b-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb23b-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="cb23b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb23b-102">SYNOPSIS</span></span>
<span data-ttu-id="cb23b-103">Ottiene un endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="cb23b-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="cb23b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb23b-104">SYNTAX</span></span>

### <span data-ttu-id="cb23b-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb23b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb23b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb23b-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cb23b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cb23b-107">DESCRIPTION</span></span>
<span data-ttu-id="cb23b-108">Il cmdlet **Get-AzCdnEndpoint** ottiene un endpoint della rete per la distribuzione di contenuti (CDN) di Azure e i dati di configurazione associati.</span><span class="sxs-lookup"><span data-stu-id="cb23b-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="cb23b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb23b-109">EXAMPLES</span></span>

## <span data-ttu-id="cb23b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb23b-110">PARAMETERS</span></span>

### <span data-ttu-id="cb23b-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="cb23b-111">-CdnProfile</span></span>
<span data-ttu-id="cb23b-112">Specifica l'oggetto profilo CDN a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="cb23b-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="cb23b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb23b-113">-DefaultProfile</span></span>
<span data-ttu-id="cb23b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="cb23b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb23b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cb23b-115">-EndpointName</span></span>
<span data-ttu-id="cb23b-116">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="cb23b-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="cb23b-117">Il nome dell'endpoint non è il nome host dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="cb23b-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="cb23b-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cb23b-118">-ProfileName</span></span>
<span data-ttu-id="cb23b-119">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="cb23b-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="cb23b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb23b-120">-ResourceGroupName</span></span>
<span data-ttu-id="cb23b-121">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="cb23b-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="cb23b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb23b-122">CommonParameters</span></span>
<span data-ttu-id="cb23b-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb23b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb23b-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb23b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb23b-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="cb23b-125">INPUTS</span></span>

### <span data-ttu-id="cb23b-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="cb23b-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="cb23b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb23b-127">OUTPUTS</span></span>

### <span data-ttu-id="cb23b-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb23b-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="cb23b-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="cb23b-129">NOTES</span></span>

## <span data-ttu-id="cb23b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb23b-130">RELATED LINKS</span></span>

[<span data-ttu-id="cb23b-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb23b-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="cb23b-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb23b-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="cb23b-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb23b-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="cb23b-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb23b-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="cb23b-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cb23b-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


