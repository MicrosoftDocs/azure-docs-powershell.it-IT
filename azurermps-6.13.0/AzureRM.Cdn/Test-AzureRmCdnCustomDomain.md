---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/test-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e249331f70e0ef0b7e1397f514363787e9dcf0dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519753"
---
# <span data-ttu-id="87649-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="87649-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="87649-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87649-102">SYNOPSIS</span></span>
<span data-ttu-id="87649-103">Controlla se un dominio personalizzato può essere aggiunto a un endpoint.</span><span class="sxs-lookup"><span data-stu-id="87649-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87649-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87649-104">SYNTAX</span></span>

### <span data-ttu-id="87649-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87649-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87649-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87649-106">ByObjectParameterSet</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87649-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87649-107">DESCRIPTION</span></span>
<span data-ttu-id="87649-108">Il cmdlet **test-AzureRmCdnCustomDomain** controlla se un dominio personalizzato può essere aggiunto a un endpoint convalidando il mapping CNAME.</span><span class="sxs-lookup"><span data-stu-id="87649-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="87649-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87649-109">EXAMPLES</span></span>

## <span data-ttu-id="87649-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87649-110">PARAMETERS</span></span>

### <span data-ttu-id="87649-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="87649-111">-CdnEndpoint</span></span>
<span data-ttu-id="87649-112">Specifica l'endpoint a cui si vuole aggiungere il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="87649-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="87649-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="87649-113">-CustomDomainHostName</span></span>
<span data-ttu-id="87649-114">Specifica il nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="87649-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="87649-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87649-115">-DefaultProfile</span></span>
<span data-ttu-id="87649-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="87649-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87649-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="87649-117">-EndpointName</span></span>
<span data-ttu-id="87649-118">Specifica il nome dell'endpoint a cui si vuole aggiungere il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="87649-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="87649-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="87649-119">-ProfileName</span></span>
<span data-ttu-id="87649-120">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="87649-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="87649-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87649-121">-ResourceGroupName</span></span>
<span data-ttu-id="87649-122">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="87649-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="87649-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87649-123">CommonParameters</span></span>
<span data-ttu-id="87649-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87649-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87649-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87649-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87649-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87649-126">INPUTS</span></span>

### <span data-ttu-id="87649-127">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="87649-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="87649-128">Parametri: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="87649-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="87649-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87649-129">OUTPUTS</span></span>

### <span data-ttu-id="87649-130">Microsoft. Azure. Commands. CDN. Models. endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="87649-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="87649-131">Note</span><span class="sxs-lookup"><span data-stu-id="87649-131">NOTES</span></span>

## <span data-ttu-id="87649-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87649-132">RELATED LINKS</span></span>

[<span data-ttu-id="87649-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="87649-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="87649-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="87649-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="87649-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="87649-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


