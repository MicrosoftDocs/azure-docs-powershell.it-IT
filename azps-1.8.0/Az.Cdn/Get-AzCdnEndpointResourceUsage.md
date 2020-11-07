---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 1c9e83e8181d716024ae993ba0c3f5a9f75c6ef1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684882"
---
# <span data-ttu-id="10b97-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="10b97-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="10b97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10b97-102">SYNOPSIS</span></span>
<span data-ttu-id="10b97-103">Ottiene l'utilizzo delle risorse di un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="10b97-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="10b97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10b97-104">SYNTAX</span></span>

### <span data-ttu-id="10b97-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10b97-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10b97-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b97-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10b97-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10b97-107">DESCRIPTION</span></span>
<span data-ttu-id="10b97-108">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="10b97-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="10b97-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10b97-109">EXAMPLES</span></span>

### <span data-ttu-id="10b97-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="10b97-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="10b97-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="10b97-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="10b97-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10b97-112">PARAMETERS</span></span>

### <span data-ttu-id="10b97-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="10b97-113">-CdnEndpoint</span></span>
<span data-ttu-id="10b97-114">Oggetto endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="10b97-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="10b97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b97-115">-DefaultProfile</span></span>
<span data-ttu-id="10b97-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="10b97-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10b97-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="10b97-117">-EndpointName</span></span>
<span data-ttu-id="10b97-118">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="10b97-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="10b97-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="10b97-119">-ProfileName</span></span>
<span data-ttu-id="10b97-120">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="10b97-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="10b97-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10b97-121">-ResourceGroupName</span></span>
<span data-ttu-id="10b97-122">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="10b97-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="10b97-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b97-123">CommonParameters</span></span>
<span data-ttu-id="10b97-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10b97-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b97-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b97-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b97-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10b97-126">INPUTS</span></span>

### <span data-ttu-id="10b97-127">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="10b97-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="10b97-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10b97-128">OUTPUTS</span></span>

### <span data-ttu-id="10b97-129">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="10b97-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="10b97-130">Note</span><span class="sxs-lookup"><span data-stu-id="10b97-130">NOTES</span></span>

## <span data-ttu-id="10b97-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10b97-131">RELATED LINKS</span></span>
