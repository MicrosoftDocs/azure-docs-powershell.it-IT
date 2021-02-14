---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195174"
---
# <span data-ttu-id="31b72-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="31b72-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="31b72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b72-102">SYNOPSIS</span></span>
<span data-ttu-id="31b72-103">Ottiene un dominio personalizzato della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="31b72-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="31b72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31b72-104">SYNTAX</span></span>

### <span data-ttu-id="31b72-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31b72-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31b72-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31b72-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b72-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="31b72-107">DESCRIPTION</span></span>
<span data-ttu-id="31b72-108">Il cmdlet **Get-AzCdnCustomDomain** ottiene un dominio personalizzato della rete per la distribuzione di contenuti (CDN) di Azure e le relative impostazioni.</span><span class="sxs-lookup"><span data-stu-id="31b72-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="31b72-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31b72-109">EXAMPLES</span></span>

## <span data-ttu-id="31b72-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31b72-110">PARAMETERS</span></span>

### <span data-ttu-id="31b72-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="31b72-111">-CdnEndpoint</span></span>
<span data-ttu-id="31b72-112">Specifica l'oggetto endpoint della rete CDN di cui il dominio personalizzato è membro.</span><span class="sxs-lookup"><span data-stu-id="31b72-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="31b72-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="31b72-113">-CustomDomainName</span></span>
<span data-ttu-id="31b72-114">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="31b72-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="31b72-115">Il nome del dominio personalizzato è diverso dal nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="31b72-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="31b72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b72-116">-DefaultProfile</span></span>
<span data-ttu-id="31b72-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="31b72-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31b72-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="31b72-118">-EndpointName</span></span>
<span data-ttu-id="31b72-119">Specifica il nome dell'endpoint a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="31b72-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="31b72-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="31b72-120">-ProfileName</span></span>
<span data-ttu-id="31b72-121">Specifica il nome del profilo a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="31b72-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="31b72-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b72-122">-ResourceGroupName</span></span>
<span data-ttu-id="31b72-123">Specifica il nome del gruppo di risorse a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="31b72-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="31b72-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b72-124">CommonParameters</span></span>
<span data-ttu-id="31b72-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b72-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b72-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31b72-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b72-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="31b72-127">INPUTS</span></span>

### <span data-ttu-id="31b72-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="31b72-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="31b72-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31b72-129">OUTPUTS</span></span>

### <span data-ttu-id="31b72-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="31b72-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="31b72-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="31b72-131">NOTES</span></span>

## <span data-ttu-id="31b72-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31b72-132">RELATED LINKS</span></span>

[<span data-ttu-id="31b72-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="31b72-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="31b72-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="31b72-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


