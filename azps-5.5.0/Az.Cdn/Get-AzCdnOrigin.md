---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181855"
---
# <span data-ttu-id="2e74d-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2e74d-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="2e74d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e74d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e74d-103">Ottiene un server di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="2e74d-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="2e74d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e74d-104">SYNTAX</span></span>

### <span data-ttu-id="2e74d-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2e74d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e74d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e74d-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e74d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e74d-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e74d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e74d-108">DESCRIPTION</span></span>
<span data-ttu-id="2e74d-109">Il cmdlet **Get-AzCdnOrigin** ottiene un server di origine della rete per la distribuzione di contenuti (CDN) di Azure e i relativi dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2e74d-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="2e74d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e74d-110">EXAMPLES</span></span>

## <span data-ttu-id="2e74d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e74d-111">PARAMETERS</span></span>

### <span data-ttu-id="2e74d-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e74d-112">-CdnEndpoint</span></span>
<span data-ttu-id="2e74d-113">Specifica l'oggetto endpoint della rete CDN a cui appartiene l'origine.</span><span class="sxs-lookup"><span data-stu-id="2e74d-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="2e74d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e74d-114">-DefaultProfile</span></span>
<span data-ttu-id="2e74d-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="2e74d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e74d-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2e74d-116">-EndpointName</span></span>
<span data-ttu-id="2e74d-117">Specifica il nome dell'endpoint a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="2e74d-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2e74d-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="2e74d-118">-OriginName</span></span>
<span data-ttu-id="2e74d-119">Specifica il nome del server di origine.</span><span class="sxs-lookup"><span data-stu-id="2e74d-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="2e74d-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2e74d-120">-ProfileName</span></span>
<span data-ttu-id="2e74d-121">Specifica il nome del profilo a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="2e74d-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2e74d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e74d-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e74d-123">Specifica il nome del gruppo di risorse a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="2e74d-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2e74d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e74d-124">-ResourceId</span></span>
<span data-ttu-id="2e74d-125">ID risorsa dell'origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="2e74d-125">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="2e74d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e74d-126">CommonParameters</span></span>
<span data-ttu-id="2e74d-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e74d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e74d-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e74d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e74d-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e74d-129">INPUTS</span></span>

### <span data-ttu-id="2e74d-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2e74d-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="2e74d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e74d-131">OUTPUTS</span></span>

### <span data-ttu-id="2e74d-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="2e74d-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="2e74d-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e74d-133">NOTES</span></span>

## <span data-ttu-id="2e74d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e74d-134">RELATED LINKS</span></span>

[<span data-ttu-id="2e74d-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2e74d-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


