---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 58e4d922d74f36f6f472cf3bfef8e0d0d45155d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010797"
---
# <span data-ttu-id="07f95-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07f95-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="07f95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f95-102">SYNOPSIS</span></span>
<span data-ttu-id="07f95-103">Crea un dominio personalizzato per un endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="07f95-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="07f95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07f95-104">SYNTAX</span></span>

### <span data-ttu-id="07f95-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07f95-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f95-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07f95-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f95-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="07f95-107">DESCRIPTION</span></span>
<span data-ttu-id="07f95-108">Il cmdlet **New-AzCdnCustomDomain** crea un dominio personalizzato per l'endpoint rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="07f95-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="07f95-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07f95-109">EXAMPLES</span></span>

## <span data-ttu-id="07f95-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07f95-110">PARAMETERS</span></span>

### <span data-ttu-id="07f95-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="07f95-111">-CdnEndpoint</span></span>
<span data-ttu-id="07f95-112">Specifica l'oggetto endpoint della rete CDN a cui viene aggiunto il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="07f95-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="07f95-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="07f95-113">-CustomDomainName</span></span>
<span data-ttu-id="07f95-114">Specifica il nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="07f95-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="07f95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f95-115">-DefaultProfile</span></span>
<span data-ttu-id="07f95-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="07f95-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07f95-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="07f95-117">-EndpointName</span></span>
<span data-ttu-id="07f95-118">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="07f95-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="07f95-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="07f95-119">-HostName</span></span>
<span data-ttu-id="07f95-120">Specifica il nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="07f95-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="07f95-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="07f95-121">-ProfileName</span></span>
<span data-ttu-id="07f95-122">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="07f95-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="07f95-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f95-123">-ResourceGroupName</span></span>
<span data-ttu-id="07f95-124">Specifica il nome del gruppo di risorse a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="07f95-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="07f95-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07f95-125">-Confirm</span></span>
<span data-ttu-id="07f95-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07f95-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f95-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f95-127">-WhatIf</span></span>
<span data-ttu-id="07f95-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07f95-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07f95-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07f95-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f95-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f95-130">CommonParameters</span></span>
<span data-ttu-id="07f95-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f95-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f95-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="07f95-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f95-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="07f95-133">INPUTS</span></span>

### <span data-ttu-id="07f95-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="07f95-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="07f95-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07f95-135">OUTPUTS</span></span>

### <span data-ttu-id="07f95-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07f95-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="07f95-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="07f95-137">NOTES</span></span>

## <span data-ttu-id="07f95-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07f95-138">RELATED LINKS</span></span>

[<span data-ttu-id="07f95-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07f95-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="07f95-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07f95-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="07f95-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="07f95-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


