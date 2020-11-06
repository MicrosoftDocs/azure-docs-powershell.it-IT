---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: df871dff0f59bc9c1e319e1470bbaa37750542e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517004"
---
# <span data-ttu-id="a58c3-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a58c3-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="a58c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a58c3-102">SYNOPSIS</span></span>
<span data-ttu-id="a58c3-103">Controlla se un dominio personalizzato può essere aggiunto a un endpoint.</span><span class="sxs-lookup"><span data-stu-id="a58c3-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a58c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a58c3-104">SYNTAX</span></span>

### <span data-ttu-id="a58c3-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a58c3-105">Parameter Set for fields parameters (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a58c3-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="a58c3-106">Parameter Set for object parameters</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a58c3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a58c3-107">DESCRIPTION</span></span>
<span data-ttu-id="a58c3-108">Il cmdlet **test-AzureRmCdnCustomDomain** controlla se un dominio personalizzato può essere aggiunto a un endpoint convalidando il mapping CNAME.</span><span class="sxs-lookup"><span data-stu-id="a58c3-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="a58c3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a58c3-109">EXAMPLES</span></span>

## <span data-ttu-id="a58c3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a58c3-110">PARAMETERS</span></span>

### <span data-ttu-id="a58c3-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a58c3-111">-CdnEndpoint</span></span>
<span data-ttu-id="a58c3-112">Specifica l'endpoint a cui si vuole aggiungere il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a58c3-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a58c3-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="a58c3-113">-CustomDomainHostName</span></span>
<span data-ttu-id="a58c3-114">Specifica il nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a58c3-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="a58c3-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a58c3-115">-EndpointName</span></span>
<span data-ttu-id="a58c3-116">Specifica il nome dell'endpoint a cui si vuole aggiungere il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a58c3-116">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58c3-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a58c3-117">-ProfileName</span></span>
<span data-ttu-id="a58c3-118">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="a58c3-118">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58c3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a58c3-119">-ResourceGroupName</span></span>
<span data-ttu-id="a58c3-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a58c3-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a58c3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58c3-121">-DefaultProfile</span></span>
<span data-ttu-id="a58c3-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a58c3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a58c3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58c3-123">CommonParameters</span></span>
<span data-ttu-id="a58c3-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a58c3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58c3-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a58c3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58c3-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a58c3-126">INPUTS</span></span>

### <span data-ttu-id="a58c3-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a58c3-127">PSEndpoint</span></span>
<span data-ttu-id="a58c3-128">Il parametro ' CdnEndpoint ' accetta il valore di tipo ' PSEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a58c3-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="a58c3-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a58c3-129">OUTPUTS</span></span>

### <span data-ttu-id="a58c3-130">Microsoft. Azure. Commands. CDN. Models. endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="a58c3-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="a58c3-131">Note</span><span class="sxs-lookup"><span data-stu-id="a58c3-131">NOTES</span></span>

## <span data-ttu-id="a58c3-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a58c3-132">RELATED LINKS</span></span>

[<span data-ttu-id="a58c3-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a58c3-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="a58c3-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a58c3-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="a58c3-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a58c3-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


