---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: 0912ba8913bae430c3878dc0bde578420a5ea429
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509315"
---
# <span data-ttu-id="48f21-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="48f21-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="48f21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48f21-102">SYNOPSIS</span></span>
<span data-ttu-id="48f21-103">Ottiene un server di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="48f21-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48f21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48f21-104">SYNTAX</span></span>

### <span data-ttu-id="48f21-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48f21-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48f21-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48f21-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48f21-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48f21-107">DESCRIPTION</span></span>
<span data-ttu-id="48f21-108">Il cmdlet **Get-AzureRmCdnOrigin** ottiene un server di origine della rete CDN (Azure Content Delivery Network) e i relativi dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="48f21-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="48f21-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48f21-109">EXAMPLES</span></span>

## <span data-ttu-id="48f21-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48f21-110">PARAMETERS</span></span>

### <span data-ttu-id="48f21-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="48f21-111">-CdnEndpoint</span></span>
<span data-ttu-id="48f21-112">Specifica l'oggetto endpoint CDN a cui appartiene l'origine.</span><span class="sxs-lookup"><span data-stu-id="48f21-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="48f21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f21-113">-DefaultProfile</span></span>
<span data-ttu-id="48f21-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="48f21-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48f21-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="48f21-115">-EndpointName</span></span>
<span data-ttu-id="48f21-116">Specifica il nome dell'endpoint a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="48f21-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="48f21-117">-Originname</span><span class="sxs-lookup"><span data-stu-id="48f21-117">-OriginName</span></span>
<span data-ttu-id="48f21-118">Specifica il nome del server di origine.</span><span class="sxs-lookup"><span data-stu-id="48f21-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="48f21-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="48f21-119">-ProfileName</span></span>
<span data-ttu-id="48f21-120">Specifica il nome del profilo a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="48f21-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="48f21-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48f21-121">-ResourceGroupName</span></span>
<span data-ttu-id="48f21-122">Specifica il nome del gruppo di risorse a cui appartiene il server di origine.</span><span class="sxs-lookup"><span data-stu-id="48f21-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="48f21-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f21-123">CommonParameters</span></span>
<span data-ttu-id="48f21-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48f21-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f21-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48f21-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f21-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48f21-126">INPUTS</span></span>

### <span data-ttu-id="48f21-127">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="48f21-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="48f21-128">Parametri: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48f21-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="48f21-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48f21-129">OUTPUTS</span></span>

### <span data-ttu-id="48f21-130">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="48f21-130">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="48f21-131">Note</span><span class="sxs-lookup"><span data-stu-id="48f21-131">NOTES</span></span>

## <span data-ttu-id="48f21-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48f21-132">RELATED LINKS</span></span>

[<span data-ttu-id="48f21-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="48f21-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


