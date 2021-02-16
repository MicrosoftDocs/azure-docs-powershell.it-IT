---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 6a0a90657ee76401117971a29dc03a78a7330afc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199462"
---
# <span data-ttu-id="4c181-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4c181-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="4c181-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c181-102">SYNOPSIS</span></span>
<span data-ttu-id="4c181-103">Crea un dominio personalizzato per un endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="4c181-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="4c181-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c181-104">SYNTAX</span></span>

### <span data-ttu-id="4c181-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c181-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c181-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c181-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c181-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c181-107">DESCRIPTION</span></span>
<span data-ttu-id="4c181-108">Il cmdlet **New-AzCdnCustomDomain** crea un dominio personalizzato per l'endpoint rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c181-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="4c181-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c181-109">EXAMPLES</span></span>

## <span data-ttu-id="4c181-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c181-110">PARAMETERS</span></span>

### <span data-ttu-id="4c181-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c181-111">-CdnEndpoint</span></span>
<span data-ttu-id="4c181-112">Specifica l'oggetto endpoint della rete CDN a cui viene aggiunto il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4c181-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="4c181-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="4c181-113">-CustomDomainName</span></span>
<span data-ttu-id="4c181-114">Specifica il nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4c181-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="4c181-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c181-115">-DefaultProfile</span></span>
<span data-ttu-id="4c181-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4c181-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c181-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4c181-117">-EndpointName</span></span>
<span data-ttu-id="4c181-118">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="4c181-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="4c181-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="4c181-119">-HostName</span></span>
<span data-ttu-id="4c181-120">Specifica il nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4c181-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="4c181-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4c181-121">-ProfileName</span></span>
<span data-ttu-id="4c181-122">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="4c181-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="4c181-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c181-123">-ResourceGroupName</span></span>
<span data-ttu-id="4c181-124">Specifica il nome del gruppo di risorse a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4c181-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="4c181-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c181-125">-Confirm</span></span>
<span data-ttu-id="4c181-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c181-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c181-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c181-127">-WhatIf</span></span>
<span data-ttu-id="4c181-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c181-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c181-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c181-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c181-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c181-130">CommonParameters</span></span>
<span data-ttu-id="4c181-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c181-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c181-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c181-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c181-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c181-133">INPUTS</span></span>

### <span data-ttu-id="4c181-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c181-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="4c181-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c181-135">OUTPUTS</span></span>

### <span data-ttu-id="4c181-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4c181-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="4c181-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c181-137">NOTES</span></span>

## <span data-ttu-id="4c181-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c181-138">RELATED LINKS</span></span>

[<span data-ttu-id="4c181-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4c181-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="4c181-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4c181-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="4c181-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4c181-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


