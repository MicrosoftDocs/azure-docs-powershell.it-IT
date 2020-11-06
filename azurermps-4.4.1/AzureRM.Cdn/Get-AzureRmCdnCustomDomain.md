---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: dcfa0968ac70f7a0abc14ee61ee615bee3aee5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519628"
---
# <span data-ttu-id="036d7-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="036d7-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="036d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="036d7-102">SYNOPSIS</span></span>
<span data-ttu-id="036d7-103">Ottiene un dominio personalizzato CDN.</span><span class="sxs-lookup"><span data-stu-id="036d7-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="036d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="036d7-104">SYNTAX</span></span>

### <span data-ttu-id="036d7-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="036d7-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="036d7-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="036d7-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="036d7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="036d7-107">DESCRIPTION</span></span>
<span data-ttu-id="036d7-108">Il cmdlet **Get-AzureRmCdnCustomDomain** ottiene un dominio personalizzato della rete CDN (Azure Content Delivery Network) e le relative impostazioni.</span><span class="sxs-lookup"><span data-stu-id="036d7-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="036d7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="036d7-109">EXAMPLES</span></span>

## <span data-ttu-id="036d7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="036d7-110">PARAMETERS</span></span>

### <span data-ttu-id="036d7-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="036d7-111">-CdnEndpoint</span></span>
<span data-ttu-id="036d7-112">Specifica l'oggetto endpoint CDN di cui il dominio personalizzato è un membro.</span><span class="sxs-lookup"><span data-stu-id="036d7-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="036d7-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="036d7-113">-CustomDomainName</span></span>
<span data-ttu-id="036d7-114">Specifica il nome del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="036d7-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="036d7-115">Il nome del dominio personalizzato è diverso dal nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="036d7-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="036d7-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="036d7-116">-EndpointName</span></span>
<span data-ttu-id="036d7-117">Specifica il nome dell'endpoint a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="036d7-117">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="036d7-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="036d7-118">-ProfileName</span></span>
<span data-ttu-id="036d7-119">Specifica il nome del profilo a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="036d7-119">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="036d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="036d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="036d7-121">Specifica il nome del gruppo di risorse a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="036d7-121">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="036d7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="036d7-122">-DefaultProfile</span></span>
<span data-ttu-id="036d7-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="036d7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="036d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036d7-124">CommonParameters</span></span>
<span data-ttu-id="036d7-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="036d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036d7-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="036d7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036d7-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="036d7-127">INPUTS</span></span>

### <span data-ttu-id="036d7-128">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="036d7-128">PSEndpoint</span></span>
<span data-ttu-id="036d7-129">Il parametro ' CdnEndpoint ' accetta il valore di tipo ' PSEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="036d7-129">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="036d7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="036d7-130">OUTPUTS</span></span>

###  
<span data-ttu-id="036d7-131">Questo cmdlet restituisce un oggetto Domain personalizzato.</span><span class="sxs-lookup"><span data-stu-id="036d7-131">This cmdlet returns a custom domain object.</span></span>

## <span data-ttu-id="036d7-132">Note</span><span class="sxs-lookup"><span data-stu-id="036d7-132">NOTES</span></span>

## <span data-ttu-id="036d7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="036d7-133">RELATED LINKS</span></span>

[<span data-ttu-id="036d7-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="036d7-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="036d7-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="036d7-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


