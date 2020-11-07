---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 4fe845225d2d396849e398f6974b1addf854d393
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684871"
---
# <span data-ttu-id="7b7e9-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7b7e9-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="7b7e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b7e9-102">SYNOPSIS</span></span>
<span data-ttu-id="7b7e9-103">Crea un dominio personalizzato per un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="7b7e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b7e9-104">SYNTAX</span></span>

### <span data-ttu-id="7b7e9-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7b7e9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b7e9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b7e9-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b7e9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b7e9-107">DESCRIPTION</span></span>
<span data-ttu-id="7b7e9-108">Il cmdlet **New-AzCdnCustomDomain** crea un dominio personalizzato per l'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="7b7e9-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7b7e9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b7e9-109">EXAMPLES</span></span>

## <span data-ttu-id="7b7e9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b7e9-110">PARAMETERS</span></span>

### <span data-ttu-id="7b7e9-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b7e9-111">-CdnEndpoint</span></span>
<span data-ttu-id="7b7e9-112">Specifica l'oggetto endpoint CDN a cui viene aggiunto il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="7b7e9-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7b7e9-113">-CustomDomainName</span></span>
<span data-ttu-id="7b7e9-114">Specifica il nome della risorsa del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="7b7e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b7e9-115">-DefaultProfile</span></span>
<span data-ttu-id="7b7e9-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7b7e9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b7e9-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7b7e9-117">-EndpointName</span></span>
<span data-ttu-id="7b7e9-118">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="7b7e9-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="7b7e9-119">-HostName</span></span>
<span data-ttu-id="7b7e9-120">Specifica il nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="7b7e9-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7b7e9-121">-ProfileName</span></span>
<span data-ttu-id="7b7e9-122">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7b7e9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b7e9-123">-ResourceGroupName</span></span>
<span data-ttu-id="7b7e9-124">Specifica il nome del gruppo di risorse a cui appartiene il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="7b7e9-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b7e9-125">-Confirm</span></span>
<span data-ttu-id="7b7e9-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b7e9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b7e9-127">-WhatIf</span></span>
<span data-ttu-id="7b7e9-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b7e9-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b7e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b7e9-130">CommonParameters</span></span>
<span data-ttu-id="7b7e9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b7e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b7e9-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b7e9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b7e9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b7e9-133">INPUTS</span></span>

### <span data-ttu-id="7b7e9-134">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b7e9-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7b7e9-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b7e9-135">OUTPUTS</span></span>

### <span data-ttu-id="7b7e9-136">Microsoft. Azure. Commands. CDN. Models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7b7e9-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="7b7e9-137">Note</span><span class="sxs-lookup"><span data-stu-id="7b7e9-137">NOTES</span></span>

## <span data-ttu-id="7b7e9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b7e9-138">RELATED LINKS</span></span>

[<span data-ttu-id="7b7e9-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7b7e9-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="7b7e9-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7b7e9-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="7b7e9-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7b7e9-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


