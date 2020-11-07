---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: ec15b97aa87c5e581069606a425f25b71dd495dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686865"
---
# <span data-ttu-id="a8b5e-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a8b5e-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="a8b5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b5e-103">Crea un dominio personalizzato per un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8b5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8b5e-104">SYNTAX</span></span>

### <span data-ttu-id="a8b5e-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8b5e-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8b5e-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="a8b5e-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8b5e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8b5e-107">DESCRIPTION</span></span>
<span data-ttu-id="a8b5e-108">Il cmdlet **New-AzureRmCdnCustomDomain** crea un dominio personalizzato per l'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="a8b5e-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a8b5e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8b5e-109">EXAMPLES</span></span>

## <span data-ttu-id="a8b5e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8b5e-110">PARAMETERS</span></span>

### <span data-ttu-id="a8b5e-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8b5e-111">-CdnEndpoint</span></span>
<span data-ttu-id="a8b5e-112">Specifica l'oggetto endpoint CDN a cui viene aggiunto il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="a8b5e-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="a8b5e-113">-CustomDomainName</span></span>
<span data-ttu-id="a8b5e-114">Specifica il nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="a8b5e-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a8b5e-115">-EndpointName</span></span>
<span data-ttu-id="a8b5e-116">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="a8b5e-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="a8b5e-117">-HostName</span></span>
<span data-ttu-id="a8b5e-118">Specifica il nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-118">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="a8b5e-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a8b5e-119">-ProfileName</span></span>
<span data-ttu-id="a8b5e-120">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="a8b5e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8b5e-121">-ResourceGroupName</span></span>
<span data-ttu-id="a8b5e-122">Specifica il nome del gruppo di risorse a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-122">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="a8b5e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8b5e-123">-Confirm</span></span>
<span data-ttu-id="a8b5e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8b5e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8b5e-125">-WhatIf</span></span>
<span data-ttu-id="a8b5e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8b5e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8b5e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b5e-128">-DefaultProfile</span></span>
<span data-ttu-id="a8b5e-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8b5e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b5e-130">CommonParameters</span></span>
<span data-ttu-id="a8b5e-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8b5e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b5e-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8b5e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b5e-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8b5e-133">INPUTS</span></span>

### <span data-ttu-id="a8b5e-134">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8b5e-134">PSEndpoint</span></span>
<span data-ttu-id="a8b5e-135">Il parametro ' CdnEndpoint ' accetta il valore di tipo ' PSEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a8b5e-135">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="a8b5e-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8b5e-136">OUTPUTS</span></span>

### <span data-ttu-id="a8b5e-137">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a8b5e-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="a8b5e-138">Note</span><span class="sxs-lookup"><span data-stu-id="a8b5e-138">NOTES</span></span>

## <span data-ttu-id="a8b5e-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8b5e-139">RELATED LINKS</span></span>

[<span data-ttu-id="a8b5e-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a8b5e-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="a8b5e-141">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a8b5e-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="a8b5e-142">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a8b5e-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


