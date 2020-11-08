---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018761"
---
# <span data-ttu-id="2ac84-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2ac84-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="2ac84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ac84-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac84-103">Ottiene un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="2ac84-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="2ac84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ac84-104">SYNTAX</span></span>

### <span data-ttu-id="2ac84-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ac84-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac84-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ac84-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ac84-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ac84-107">DESCRIPTION</span></span>
<span data-ttu-id="2ac84-108">Il cmdlet **Get-AzCdnCustomDomain** ottiene un dominio personalizzato della rete CDN (Azure Content Delivery Network) e le relative impostazioni.</span><span class="sxs-lookup"><span data-stu-id="2ac84-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="2ac84-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ac84-109">EXAMPLES</span></span>

## <span data-ttu-id="2ac84-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ac84-110">PARAMETERS</span></span>

### <span data-ttu-id="2ac84-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ac84-111">-CdnEndpoint</span></span>
<span data-ttu-id="2ac84-112">Specifica l'oggetto endpoint CDN di cui il dominio personalizzato è un membro.</span><span class="sxs-lookup"><span data-stu-id="2ac84-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="2ac84-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="2ac84-113">-CustomDomainName</span></span>
<span data-ttu-id="2ac84-114">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2ac84-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="2ac84-115">Il nome del dominio personalizzato è diverso dal nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2ac84-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="2ac84-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac84-116">-DefaultProfile</span></span>
<span data-ttu-id="2ac84-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2ac84-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ac84-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2ac84-118">-EndpointName</span></span>
<span data-ttu-id="2ac84-119">Specifica il nome dell'endpoint a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2ac84-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="2ac84-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2ac84-120">-ProfileName</span></span>
<span data-ttu-id="2ac84-121">Specifica il nome del profilo a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2ac84-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="2ac84-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac84-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ac84-123">Specifica il nome del gruppo di risorse a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2ac84-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="2ac84-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac84-124">CommonParameters</span></span>
<span data-ttu-id="2ac84-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac84-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac84-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ac84-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac84-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ac84-127">INPUTS</span></span>

### <span data-ttu-id="2ac84-128">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ac84-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="2ac84-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ac84-129">OUTPUTS</span></span>

### <span data-ttu-id="2ac84-130">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2ac84-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="2ac84-131">Note</span><span class="sxs-lookup"><span data-stu-id="2ac84-131">NOTES</span></span>

## <span data-ttu-id="2ac84-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ac84-132">RELATED LINKS</span></span>

[<span data-ttu-id="2ac84-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2ac84-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="2ac84-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="2ac84-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


