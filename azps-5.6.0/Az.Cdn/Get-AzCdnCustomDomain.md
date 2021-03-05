---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: e1c436a76a3fc98714798bc938f0de987906e7d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010814"
---
# <span data-ttu-id="ce60a-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ce60a-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="ce60a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce60a-102">SYNOPSIS</span></span>
<span data-ttu-id="ce60a-103">Ottiene un dominio personalizzato della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="ce60a-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="ce60a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce60a-104">SYNTAX</span></span>

### <span data-ttu-id="ce60a-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce60a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce60a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce60a-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce60a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ce60a-107">DESCRIPTION</span></span>
<span data-ttu-id="ce60a-108">Il cmdlet **Get-AzCdnCustomDomain** ottiene un dominio personalizzato della rete per la distribuzione di contenuti (CDN) di Azure e le relative impostazioni.</span><span class="sxs-lookup"><span data-stu-id="ce60a-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="ce60a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce60a-109">EXAMPLES</span></span>

## <span data-ttu-id="ce60a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce60a-110">PARAMETERS</span></span>

### <span data-ttu-id="ce60a-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce60a-111">-CdnEndpoint</span></span>
<span data-ttu-id="ce60a-112">Specifica l'oggetto endpoint della rete CDN di cui il dominio personalizzato è membro.</span><span class="sxs-lookup"><span data-stu-id="ce60a-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="ce60a-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ce60a-113">-CustomDomainName</span></span>
<span data-ttu-id="ce60a-114">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ce60a-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="ce60a-115">Il nome del dominio personalizzato è diverso dal nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ce60a-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="ce60a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce60a-116">-DefaultProfile</span></span>
<span data-ttu-id="ce60a-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ce60a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce60a-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ce60a-118">-EndpointName</span></span>
<span data-ttu-id="ce60a-119">Specifica il nome dell'endpoint a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ce60a-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ce60a-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ce60a-120">-ProfileName</span></span>
<span data-ttu-id="ce60a-121">Specifica il nome del profilo a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ce60a-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ce60a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce60a-122">-ResourceGroupName</span></span>
<span data-ttu-id="ce60a-123">Specifica il nome del gruppo di risorse a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ce60a-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ce60a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce60a-124">CommonParameters</span></span>
<span data-ttu-id="ce60a-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce60a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce60a-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ce60a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce60a-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="ce60a-127">INPUTS</span></span>

### <span data-ttu-id="ce60a-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce60a-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="ce60a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce60a-129">OUTPUTS</span></span>

### <span data-ttu-id="ce60a-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ce60a-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="ce60a-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="ce60a-131">NOTES</span></span>

## <span data-ttu-id="ce60a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce60a-132">RELATED LINKS</span></span>

[<span data-ttu-id="ce60a-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ce60a-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="ce60a-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ce60a-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


