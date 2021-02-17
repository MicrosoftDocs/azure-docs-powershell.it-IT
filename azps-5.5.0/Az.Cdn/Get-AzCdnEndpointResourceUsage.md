---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205122"
---
# <span data-ttu-id="60b1f-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="60b1f-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="60b1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="60b1f-103">Recupera l'uso delle risorse di un endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="60b1f-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="60b1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60b1f-104">SYNTAX</span></span>

### <span data-ttu-id="60b1f-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60b1f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60b1f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60b1f-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60b1f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60b1f-107">DESCRIPTION</span></span>
<span data-ttu-id="60b1f-108">{{Inserire la descrizione}}</span><span class="sxs-lookup"><span data-stu-id="60b1f-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="60b1f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60b1f-109">EXAMPLES</span></span>

### <span data-ttu-id="60b1f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60b1f-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="60b1f-111">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="60b1f-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="60b1f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60b1f-112">PARAMETERS</span></span>

### <span data-ttu-id="60b1f-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="60b1f-113">-CdnEndpoint</span></span>
<span data-ttu-id="60b1f-114">L'oggetto endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="60b1f-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="60b1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b1f-115">-DefaultProfile</span></span>
<span data-ttu-id="60b1f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="60b1f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60b1f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="60b1f-117">-EndpointName</span></span>
<span data-ttu-id="60b1f-118">Nome dell'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="60b1f-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="60b1f-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="60b1f-119">-ProfileName</span></span>
<span data-ttu-id="60b1f-120">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="60b1f-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="60b1f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b1f-121">-ResourceGroupName</span></span>
<span data-ttu-id="60b1f-122">Gruppo di risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="60b1f-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="60b1f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b1f-123">CommonParameters</span></span>
<span data-ttu-id="60b1f-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b1f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b1f-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60b1f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b1f-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="60b1f-126">INPUTS</span></span>

### <span data-ttu-id="60b1f-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="60b1f-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="60b1f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60b1f-128">OUTPUTS</span></span>

### <span data-ttu-id="60b1f-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="60b1f-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="60b1f-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="60b1f-130">NOTES</span></span>

## <span data-ttu-id="60b1f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60b1f-131">RELATED LINKS</span></span>
