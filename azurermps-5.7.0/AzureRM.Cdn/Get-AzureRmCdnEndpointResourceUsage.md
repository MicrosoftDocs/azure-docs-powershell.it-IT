---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 82daa7f202dce698a84d17292a199fbd8f85bca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521100"
---
# <span data-ttu-id="3ee37-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="3ee37-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="3ee37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ee37-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee37-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="3ee37-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ee37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ee37-104">SYNTAX</span></span>

### <span data-ttu-id="3ee37-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3ee37-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ee37-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ee37-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ee37-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ee37-107">DESCRIPTION</span></span>
<span data-ttu-id="3ee37-108">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="3ee37-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="3ee37-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ee37-109">EXAMPLES</span></span>

### <span data-ttu-id="3ee37-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3ee37-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3ee37-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="3ee37-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="3ee37-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ee37-112">PARAMETERS</span></span>

### <span data-ttu-id="3ee37-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ee37-113">-CdnEndpoint</span></span>
<span data-ttu-id="3ee37-114">Oggetto endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="3ee37-114">The CDN endpoint object.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee37-115">-DefaultProfile</span></span>
<span data-ttu-id="3ee37-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3ee37-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee37-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3ee37-117">-EndpointName</span></span>
<span data-ttu-id="3ee37-118">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ee37-118">Azure CDN endpoint name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee37-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3ee37-119">-ProfileName</span></span>
<span data-ttu-id="3ee37-120">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ee37-120">Azure CDN profile name.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee37-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee37-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ee37-122">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ee37-122">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee37-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee37-123">CommonParameters</span></span>
<span data-ttu-id="3ee37-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee37-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee37-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee37-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee37-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ee37-126">INPUTS</span></span>

### <span data-ttu-id="3ee37-127">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ee37-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="3ee37-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ee37-128">OUTPUTS</span></span>

### <span data-ttu-id="3ee37-129">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="3ee37-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="3ee37-130">Note</span><span class="sxs-lookup"><span data-stu-id="3ee37-130">NOTES</span></span>

## <span data-ttu-id="3ee37-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ee37-131">RELATED LINKS</span></span>

