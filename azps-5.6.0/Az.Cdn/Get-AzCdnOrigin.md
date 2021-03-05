---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: 5c2aa677bd2f197cfae262ed54372d5172fe2a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009262"
---
# <span data-ttu-id="e5dee-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e5dee-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="e5dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5dee-102">SYNOPSIS</span></span>
<span data-ttu-id="e5dee-103">Ottiene un server di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="e5dee-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="e5dee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5dee-104">SYNTAX</span></span>

### <span data-ttu-id="e5dee-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5dee-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5dee-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5dee-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5dee-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5dee-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5dee-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e5dee-108">DESCRIPTION</span></span>
<span data-ttu-id="e5dee-109">Il cmdlet **Get-AzCdnOrigin** ottiene un server di origine della rete per la distribuzione di contenuti (CDN) di Azure e i relativi dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="e5dee-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="e5dee-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5dee-110">EXAMPLES</span></span>

## <span data-ttu-id="e5dee-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5dee-111">PARAMETERS</span></span>

### <span data-ttu-id="e5dee-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5dee-112">-CdnEndpoint</span></span>
<span data-ttu-id="e5dee-113">Specifica l'oggetto endpoint della rete CDN a cui appartiene l'origine.</span><span class="sxs-lookup"><span data-stu-id="e5dee-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="e5dee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5dee-114">-DefaultProfile</span></span>
<span data-ttu-id="e5dee-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e5dee-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5dee-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e5dee-116">-EndpointName</span></span>
<span data-ttu-id="e5dee-117">Specifica il nome dell'endpoint a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="e5dee-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e5dee-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="e5dee-118">-OriginName</span></span>
<span data-ttu-id="e5dee-119">Specifica il nome del server di origine.</span><span class="sxs-lookup"><span data-stu-id="e5dee-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="e5dee-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e5dee-120">-ProfileName</span></span>
<span data-ttu-id="e5dee-121">Specifica il nome del profilo a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="e5dee-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e5dee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5dee-122">-ResourceGroupName</span></span>
<span data-ttu-id="e5dee-123">Specifica il nome del gruppo di risorse a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="e5dee-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e5dee-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5dee-124">-ResourceId</span></span>
<span data-ttu-id="e5dee-125">ID risorsa dell'origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5dee-125">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5dee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5dee-126">CommonParameters</span></span>
<span data-ttu-id="e5dee-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5dee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5dee-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5dee-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5dee-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="e5dee-129">INPUTS</span></span>

### <span data-ttu-id="e5dee-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e5dee-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="e5dee-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5dee-131">OUTPUTS</span></span>

### <span data-ttu-id="e5dee-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="e5dee-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="e5dee-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="e5dee-133">NOTES</span></span>

## <span data-ttu-id="e5dee-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5dee-134">RELATED LINKS</span></span>

[<span data-ttu-id="e5dee-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e5dee-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


