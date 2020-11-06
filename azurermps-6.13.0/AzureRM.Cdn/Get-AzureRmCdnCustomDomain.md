---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e0c1d2e49cce4798499506352811d1e341bf47e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521411"
---
# <span data-ttu-id="1c0fd-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1c0fd-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="1c0fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c0fd-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0fd-103">Ottiene un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="1c0fd-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c0fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c0fd-104">SYNTAX</span></span>

### <span data-ttu-id="1c0fd-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c0fd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c0fd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c0fd-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c0fd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c0fd-107">DESCRIPTION</span></span>
<span data-ttu-id="1c0fd-108">Il cmdlet **Get-AzureRmCdnCustomDomain** ottiene un dominio personalizzato della rete CDN (Azure Content Delivery Network) e le relative impostazioni.</span><span class="sxs-lookup"><span data-stu-id="1c0fd-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="1c0fd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c0fd-109">EXAMPLES</span></span>

## <span data-ttu-id="1c0fd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c0fd-110">PARAMETERS</span></span>

### <span data-ttu-id="1c0fd-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c0fd-111">-CdnEndpoint</span></span>
<span data-ttu-id="1c0fd-112">Specifica l'oggetto endpoint CDN di cui il dominio personalizzato è un membro.</span><span class="sxs-lookup"><span data-stu-id="1c0fd-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="1c0fd-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="1c0fd-113">-CustomDomainName</span></span>
<span data-ttu-id="1c0fd-114">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1c0fd-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="1c0fd-115">Il nome del dominio personalizzato è diverso dal nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1c0fd-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="1c0fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0fd-116">-DefaultProfile</span></span>
<span data-ttu-id="1c0fd-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1c0fd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c0fd-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1c0fd-118">-EndpointName</span></span>
<span data-ttu-id="1c0fd-119">Specifica il nome dell'endpoint a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1c0fd-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="1c0fd-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1c0fd-120">-ProfileName</span></span>
<span data-ttu-id="1c0fd-121">Specifica il nome del profilo a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1c0fd-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="1c0fd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c0fd-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c0fd-123">Specifica il nome del gruppo di risorse a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1c0fd-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="1c0fd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0fd-124">CommonParameters</span></span>
<span data-ttu-id="1c0fd-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c0fd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0fd-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c0fd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0fd-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c0fd-127">INPUTS</span></span>

### <span data-ttu-id="1c0fd-128">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c0fd-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="1c0fd-129">Parametri: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c0fd-129">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="1c0fd-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c0fd-130">OUTPUTS</span></span>

### <span data-ttu-id="1c0fd-131">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1c0fd-131">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="1c0fd-132">Note</span><span class="sxs-lookup"><span data-stu-id="1c0fd-132">NOTES</span></span>

## <span data-ttu-id="1c0fd-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c0fd-133">RELATED LINKS</span></span>

[<span data-ttu-id="1c0fd-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1c0fd-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="1c0fd-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1c0fd-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


