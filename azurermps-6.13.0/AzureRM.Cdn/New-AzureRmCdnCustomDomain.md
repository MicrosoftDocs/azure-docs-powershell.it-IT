---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: a3d92c095173d9eeb0b5e84812d42656e414b9d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518864"
---
# <span data-ttu-id="c193e-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c193e-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="c193e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c193e-102">SYNOPSIS</span></span>
<span data-ttu-id="c193e-103">Crea un dominio personalizzato per un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="c193e-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c193e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c193e-104">SYNTAX</span></span>

### <span data-ttu-id="c193e-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c193e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c193e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c193e-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c193e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c193e-107">DESCRIPTION</span></span>
<span data-ttu-id="c193e-108">Il cmdlet **New-AzureRmCdnCustomDomain** crea un dominio personalizzato per l'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="c193e-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c193e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c193e-109">EXAMPLES</span></span>

## <span data-ttu-id="c193e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c193e-110">PARAMETERS</span></span>

### <span data-ttu-id="c193e-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c193e-111">-CdnEndpoint</span></span>
<span data-ttu-id="c193e-112">Specifica l'oggetto endpoint CDN a cui viene aggiunto il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c193e-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="c193e-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="c193e-113">-CustomDomainName</span></span>
<span data-ttu-id="c193e-114">Specifica il nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c193e-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="c193e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c193e-115">-DefaultProfile</span></span>
<span data-ttu-id="c193e-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c193e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c193e-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c193e-117">-EndpointName</span></span>
<span data-ttu-id="c193e-118">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="c193e-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="c193e-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="c193e-119">-HostName</span></span>
<span data-ttu-id="c193e-120">Specifica il nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c193e-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="c193e-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c193e-121">-ProfileName</span></span>
<span data-ttu-id="c193e-122">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="c193e-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="c193e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c193e-123">-ResourceGroupName</span></span>
<span data-ttu-id="c193e-124">Specifica il nome del gruppo di risorse a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c193e-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="c193e-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c193e-125">-Confirm</span></span>
<span data-ttu-id="c193e-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c193e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c193e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c193e-127">-WhatIf</span></span>
<span data-ttu-id="c193e-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c193e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c193e-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c193e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c193e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c193e-130">CommonParameters</span></span>
<span data-ttu-id="c193e-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c193e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c193e-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c193e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c193e-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c193e-133">INPUTS</span></span>

### <span data-ttu-id="c193e-134">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c193e-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="c193e-135">Parametri: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c193e-135">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="c193e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c193e-136">OUTPUTS</span></span>

### <span data-ttu-id="c193e-137">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c193e-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="c193e-138">Note</span><span class="sxs-lookup"><span data-stu-id="c193e-138">NOTES</span></span>

## <span data-ttu-id="c193e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c193e-139">RELATED LINKS</span></span>

[<span data-ttu-id="c193e-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c193e-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="c193e-141">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c193e-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="c193e-142">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c193e-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


