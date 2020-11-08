---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: f648d347e45b6394776a25735efbb06157cc5611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190393"
---
# <span data-ttu-id="5e299-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5e299-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="5e299-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e299-102">SYNOPSIS</span></span>
<span data-ttu-id="5e299-103">Ottiene un server di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="5e299-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="5e299-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e299-104">SYNTAX</span></span>

### <span data-ttu-id="5e299-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e299-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e299-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e299-106">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e299-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e299-107">DESCRIPTION</span></span>
<span data-ttu-id="5e299-108">Il cmdlet **Get-AzCdnOrigin** ottiene un server di origine della rete CDN (Azure Content Delivery Network) e i relativi dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="5e299-108">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="5e299-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e299-109">EXAMPLES</span></span>

## <span data-ttu-id="5e299-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e299-110">PARAMETERS</span></span>

### <span data-ttu-id="5e299-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e299-111">-CdnEndpoint</span></span>
<span data-ttu-id="5e299-112">Specifica l'oggetto endpoint CDN a cui appartiene l'origine.</span><span class="sxs-lookup"><span data-stu-id="5e299-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="5e299-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e299-113">-DefaultProfile</span></span>
<span data-ttu-id="5e299-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5e299-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e299-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5e299-115">-EndpointName</span></span>
<span data-ttu-id="5e299-116">Specifica il nome dell'endpoint a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="5e299-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="5e299-117">-Originname</span><span class="sxs-lookup"><span data-stu-id="5e299-117">-OriginName</span></span>
<span data-ttu-id="5e299-118">Specifica il nome del server di origine.</span><span class="sxs-lookup"><span data-stu-id="5e299-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="5e299-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5e299-119">-ProfileName</span></span>
<span data-ttu-id="5e299-120">Specifica il nome del profilo a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="5e299-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="5e299-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e299-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e299-122">Specifica il nome del gruppo di risorse a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="5e299-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="5e299-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e299-123">CommonParameters</span></span>
<span data-ttu-id="5e299-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e299-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e299-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e299-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e299-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e299-126">INPUTS</span></span>

### <span data-ttu-id="5e299-127">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5e299-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="5e299-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e299-128">OUTPUTS</span></span>

### <span data-ttu-id="5e299-129">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="5e299-129">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="5e299-130">Note</span><span class="sxs-lookup"><span data-stu-id="5e299-130">NOTES</span></span>

## <span data-ttu-id="5e299-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e299-131">RELATED LINKS</span></span>

[<span data-ttu-id="5e299-132">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5e299-132">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


