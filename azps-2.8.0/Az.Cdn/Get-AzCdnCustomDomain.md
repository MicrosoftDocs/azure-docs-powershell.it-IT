---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: 3462e256889dffd086d9fa1d0fb96dba42ed109a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675572"
---
# <span data-ttu-id="f9209-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f9209-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="f9209-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9209-102">SYNOPSIS</span></span>
<span data-ttu-id="f9209-103">Ottiene un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="f9209-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="f9209-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9209-104">SYNTAX</span></span>

### <span data-ttu-id="f9209-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9209-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9209-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9209-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9209-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9209-107">DESCRIPTION</span></span>
<span data-ttu-id="f9209-108">Il cmdlet **Get-AzCdnCustomDomain** ottiene un dominio personalizzato della rete CDN (Azure Content Delivery Network) e le relative impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f9209-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="f9209-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9209-109">EXAMPLES</span></span>

## <span data-ttu-id="f9209-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9209-110">PARAMETERS</span></span>

### <span data-ttu-id="f9209-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9209-111">-CdnEndpoint</span></span>
<span data-ttu-id="f9209-112">Specifica l'oggetto endpoint CDN di cui il dominio personalizzato è un membro.</span><span class="sxs-lookup"><span data-stu-id="f9209-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="f9209-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="f9209-113">-CustomDomainName</span></span>
<span data-ttu-id="f9209-114">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f9209-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="f9209-115">Il nome del dominio personalizzato è diverso dal nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f9209-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="f9209-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9209-116">-DefaultProfile</span></span>
<span data-ttu-id="f9209-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f9209-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9209-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f9209-118">-EndpointName</span></span>
<span data-ttu-id="f9209-119">Specifica il nome dell'endpoint a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f9209-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="f9209-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f9209-120">-ProfileName</span></span>
<span data-ttu-id="f9209-121">Specifica il nome del profilo a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f9209-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="f9209-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9209-122">-ResourceGroupName</span></span>
<span data-ttu-id="f9209-123">Specifica il nome del gruppo di risorse a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f9209-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="f9209-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9209-124">CommonParameters</span></span>
<span data-ttu-id="f9209-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9209-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9209-126">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9209-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9209-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9209-127">INPUTS</span></span>

### <span data-ttu-id="f9209-128">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9209-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="f9209-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9209-129">OUTPUTS</span></span>

### <span data-ttu-id="f9209-130">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f9209-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="f9209-131">Note</span><span class="sxs-lookup"><span data-stu-id="f9209-131">NOTES</span></span>

## <span data-ttu-id="f9209-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9209-132">RELATED LINKS</span></span>

[<span data-ttu-id="f9209-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f9209-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="f9209-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f9209-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

