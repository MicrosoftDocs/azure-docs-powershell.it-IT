---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488668"
---
# <span data-ttu-id="8b5ee-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="8b5ee-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="8b5ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b5ee-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5ee-103">Ottiene un server di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="8b5ee-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="8b5ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b5ee-104">SYNTAX</span></span>

### <span data-ttu-id="8b5ee-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b5ee-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b5ee-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b5ee-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b5ee-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b5ee-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b5ee-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b5ee-108">DESCRIPTION</span></span>
<span data-ttu-id="8b5ee-109">Il cmdlet **Get-AzCdnOrigin** ottiene un server di origine della rete CDN (Azure Content Delivery Network) e i relativi dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="8b5ee-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="8b5ee-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b5ee-110">EXAMPLES</span></span>

## <span data-ttu-id="8b5ee-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b5ee-111">PARAMETERS</span></span>

### <span data-ttu-id="8b5ee-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b5ee-112">-CdnEndpoint</span></span>
<span data-ttu-id="8b5ee-113">Specifica l'oggetto endpoint CDN a cui appartiene l'origine.</span><span class="sxs-lookup"><span data-stu-id="8b5ee-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="8b5ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b5ee-114">-DefaultProfile</span></span>
<span data-ttu-id="8b5ee-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8b5ee-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b5ee-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8b5ee-116">-EndpointName</span></span>
<span data-ttu-id="8b5ee-117">Specifica il nome dell'endpoint a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="8b5ee-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="8b5ee-118">-Originname</span><span class="sxs-lookup"><span data-stu-id="8b5ee-118">-OriginName</span></span>
<span data-ttu-id="8b5ee-119">Specifica il nome del server di origine.</span><span class="sxs-lookup"><span data-stu-id="8b5ee-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="8b5ee-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8b5ee-120">-ProfileName</span></span>
<span data-ttu-id="8b5ee-121">Specifica il nome del profilo a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="8b5ee-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="8b5ee-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b5ee-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b5ee-123">Specifica il nome del gruppo di risorse a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="8b5ee-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="8b5ee-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b5ee-124">-ResourceId</span></span>
<span data-ttu-id="8b5ee-125">ID risorsa dell'origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="8b5ee-125">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="8b5ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5ee-126">CommonParameters</span></span>
<span data-ttu-id="8b5ee-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b5ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5ee-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b5ee-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5ee-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b5ee-129">INPUTS</span></span>

### <span data-ttu-id="8b5ee-130">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="8b5ee-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="8b5ee-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b5ee-131">OUTPUTS</span></span>

### <span data-ttu-id="8b5ee-132">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="8b5ee-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="8b5ee-133">Note</span><span class="sxs-lookup"><span data-stu-id="8b5ee-133">NOTES</span></span>

## <span data-ttu-id="8b5ee-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b5ee-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b5ee-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="8b5ee-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


