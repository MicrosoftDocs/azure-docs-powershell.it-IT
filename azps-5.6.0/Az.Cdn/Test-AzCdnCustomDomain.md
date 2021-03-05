---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: b2c061f7755c7891946bcf8ea8f3fa5cdb15439d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986956"
---
# <span data-ttu-id="bdb20-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bdb20-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="bdb20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdb20-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb20-103">Controlla se è possibile aggiungere un dominio personalizzato a un endpoint.</span><span class="sxs-lookup"><span data-stu-id="bdb20-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="bdb20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdb20-104">SYNTAX</span></span>

### <span data-ttu-id="bdb20-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bdb20-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdb20-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdb20-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdb20-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bdb20-107">DESCRIPTION</span></span>
<span data-ttu-id="bdb20-108">Il cmdlet **Test-AzCdnCustomDomain** controlla se è possibile aggiungere un dominio personalizzato a un endpoint convalidando il mapping CName.</span><span class="sxs-lookup"><span data-stu-id="bdb20-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="bdb20-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdb20-109">EXAMPLES</span></span>

## <span data-ttu-id="bdb20-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdb20-110">PARAMETERS</span></span>

### <span data-ttu-id="bdb20-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bdb20-111">-CdnEndpoint</span></span>
<span data-ttu-id="bdb20-112">Specifica l'endpoint a cui si vuole aggiungere il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="bdb20-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="bdb20-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="bdb20-113">-CustomDomainHostName</span></span>
<span data-ttu-id="bdb20-114">Specifica il nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="bdb20-114">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb20-115">-DefaultProfile</span></span>
<span data-ttu-id="bdb20-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bdb20-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdb20-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bdb20-117">-EndpointName</span></span>
<span data-ttu-id="bdb20-118">Specifica il nome dell'endpoint a cui si vuole aggiungere il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="bdb20-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="bdb20-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bdb20-119">-ProfileName</span></span>
<span data-ttu-id="bdb20-120">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="bdb20-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="bdb20-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb20-121">-ResourceGroupName</span></span>
<span data-ttu-id="bdb20-122">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bdb20-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bdb20-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb20-123">CommonParameters</span></span>
<span data-ttu-id="bdb20-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb20-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb20-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bdb20-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb20-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="bdb20-126">INPUTS</span></span>

### <span data-ttu-id="bdb20-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bdb20-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="bdb20-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdb20-128">OUTPUTS</span></span>

### <span data-ttu-id="bdb20-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="bdb20-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="bdb20-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="bdb20-130">NOTES</span></span>

## <span data-ttu-id="bdb20-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdb20-131">RELATED LINKS</span></span>

[<span data-ttu-id="bdb20-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bdb20-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="bdb20-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bdb20-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="bdb20-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bdb20-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


