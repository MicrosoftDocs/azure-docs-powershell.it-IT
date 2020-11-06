---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 3fe740fc8643ab6ef4f010feeee57b3339426c21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516680"
---
# <span data-ttu-id="809ef-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="809ef-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="809ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="809ef-102">SYNOPSIS</span></span>
<span data-ttu-id="809ef-103">Ottiene l'utilizzo delle risorse di un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="809ef-103">Gets the resource usage of a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="809ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="809ef-104">SYNTAX</span></span>

### <span data-ttu-id="809ef-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="809ef-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="809ef-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="809ef-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="809ef-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="809ef-107">DESCRIPTION</span></span>
<span data-ttu-id="809ef-108">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="809ef-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="809ef-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="809ef-109">EXAMPLES</span></span>

### <span data-ttu-id="809ef-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="809ef-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="809ef-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="809ef-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="809ef-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="809ef-112">PARAMETERS</span></span>

### <span data-ttu-id="809ef-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="809ef-113">-CdnEndpoint</span></span>
<span data-ttu-id="809ef-114">Oggetto endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="809ef-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="809ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="809ef-115">-DefaultProfile</span></span>
<span data-ttu-id="809ef-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="809ef-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="809ef-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="809ef-117">-EndpointName</span></span>
<span data-ttu-id="809ef-118">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="809ef-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="809ef-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="809ef-119">-ProfileName</span></span>
<span data-ttu-id="809ef-120">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="809ef-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="809ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="809ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="809ef-122">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="809ef-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="809ef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="809ef-123">CommonParameters</span></span>
<span data-ttu-id="809ef-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="809ef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="809ef-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="809ef-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="809ef-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="809ef-126">INPUTS</span></span>

### <span data-ttu-id="809ef-127">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="809ef-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="809ef-128">Parametri: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="809ef-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="809ef-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="809ef-129">OUTPUTS</span></span>

### <span data-ttu-id="809ef-130">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="809ef-130">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="809ef-131">Note</span><span class="sxs-lookup"><span data-stu-id="809ef-131">NOTES</span></span>

## <span data-ttu-id="809ef-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="809ef-132">RELATED LINKS</span></span>
