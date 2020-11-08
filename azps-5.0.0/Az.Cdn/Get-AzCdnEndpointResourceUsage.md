---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203000"
---
# <span data-ttu-id="bb13b-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="bb13b-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="bb13b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb13b-102">SYNOPSIS</span></span>
<span data-ttu-id="bb13b-103">Ottiene l'utilizzo delle risorse di un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="bb13b-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="bb13b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb13b-104">SYNTAX</span></span>

### <span data-ttu-id="bb13b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bb13b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb13b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb13b-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb13b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb13b-107">DESCRIPTION</span></span>
<span data-ttu-id="bb13b-108">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="bb13b-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="bb13b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb13b-109">EXAMPLES</span></span>

### <span data-ttu-id="bb13b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb13b-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="bb13b-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="bb13b-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="bb13b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb13b-112">PARAMETERS</span></span>

### <span data-ttu-id="bb13b-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb13b-113">-CdnEndpoint</span></span>
<span data-ttu-id="bb13b-114">Oggetto endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="bb13b-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="bb13b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb13b-115">-DefaultProfile</span></span>
<span data-ttu-id="bb13b-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bb13b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb13b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bb13b-117">-EndpointName</span></span>
<span data-ttu-id="bb13b-118">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb13b-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="bb13b-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bb13b-119">-ProfileName</span></span>
<span data-ttu-id="bb13b-120">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb13b-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="bb13b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb13b-121">-ResourceGroupName</span></span>
<span data-ttu-id="bb13b-122">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb13b-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="bb13b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb13b-123">CommonParameters</span></span>
<span data-ttu-id="bb13b-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb13b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb13b-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb13b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb13b-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb13b-126">INPUTS</span></span>

### <span data-ttu-id="bb13b-127">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb13b-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="bb13b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb13b-128">OUTPUTS</span></span>

### <span data-ttu-id="bb13b-129">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="bb13b-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="bb13b-130">Note</span><span class="sxs-lookup"><span data-stu-id="bb13b-130">NOTES</span></span>

## <span data-ttu-id="bb13b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb13b-131">RELATED LINKS</span></span>
