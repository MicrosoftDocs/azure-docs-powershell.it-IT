---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: f9d9d307959d53748afe7219ccb4cbce631c5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521980"
---
# <span data-ttu-id="6d9f9-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="6d9f9-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="6d9f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9f9-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="6d9f9-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d9f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d9f9-104">SYNTAX</span></span>

### <span data-ttu-id="6d9f9-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d9f9-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d9f9-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="6d9f9-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d9f9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d9f9-107">DESCRIPTION</span></span>
<span data-ttu-id="6d9f9-108">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="6d9f9-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="6d9f9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d9f9-109">EXAMPLES</span></span>

### <span data-ttu-id="6d9f9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6d9f9-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6d9f9-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="6d9f9-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="6d9f9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d9f9-112">PARAMETERS</span></span>

### <span data-ttu-id="6d9f9-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d9f9-113">-CdnEndpoint</span></span>
<span data-ttu-id="6d9f9-114">Oggetto endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="6d9f9-114">The CDN endpoint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d9f9-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6d9f9-115">-EndpointName</span></span>
<span data-ttu-id="6d9f9-116">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9f9-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="6d9f9-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6d9f9-117">-ProfileName</span></span>
<span data-ttu-id="6d9f9-118">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9f9-118">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="6d9f9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9f9-119">-ResourceGroupName</span></span>
<span data-ttu-id="6d9f9-120">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9f9-120">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="6d9f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9f9-121">-DefaultProfile</span></span>
<span data-ttu-id="6d9f9-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9f9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d9f9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9f9-123">CommonParameters</span></span>
<span data-ttu-id="6d9f9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9f9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9f9-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d9f9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9f9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d9f9-126">INPUTS</span></span>

### <span data-ttu-id="6d9f9-127">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d9f9-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="6d9f9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d9f9-128">OUTPUTS</span></span>

### <span data-ttu-id="6d9f9-129">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="6d9f9-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="6d9f9-130">Note</span><span class="sxs-lookup"><span data-stu-id="6d9f9-130">NOTES</span></span>

## <span data-ttu-id="6d9f9-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d9f9-131">RELATED LINKS</span></span>

