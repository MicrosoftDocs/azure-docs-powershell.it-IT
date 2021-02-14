---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195142"
---
# <span data-ttu-id="0d4fe-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d4fe-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="0d4fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="0d4fe-103">Controlla se è possibile aggiungere un dominio personalizzato a un endpoint.</span><span class="sxs-lookup"><span data-stu-id="0d4fe-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="0d4fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d4fe-104">SYNTAX</span></span>

### <span data-ttu-id="0d4fe-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0d4fe-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d4fe-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4fe-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d4fe-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0d4fe-107">DESCRIPTION</span></span>
<span data-ttu-id="0d4fe-108">Il **cmdlet Test-AzCdnCustomDomain** controlla se è possibile aggiungere un dominio personalizzato a un endpoint convalidando il mapping CName.</span><span class="sxs-lookup"><span data-stu-id="0d4fe-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="0d4fe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d4fe-109">EXAMPLES</span></span>

## <span data-ttu-id="0d4fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d4fe-110">PARAMETERS</span></span>

### <span data-ttu-id="0d4fe-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d4fe-111">-CdnEndpoint</span></span>
<span data-ttu-id="0d4fe-112">Specifica l'endpoint a cui si vuole aggiungere il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0d4fe-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="0d4fe-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="0d4fe-113">-CustomDomainHostName</span></span>
<span data-ttu-id="0d4fe-114">Specifica il nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0d4fe-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="0d4fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d4fe-115">-DefaultProfile</span></span>
<span data-ttu-id="0d4fe-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0d4fe-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d4fe-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0d4fe-117">-EndpointName</span></span>
<span data-ttu-id="0d4fe-118">Specifica il nome dell'endpoint a cui si vuole aggiungere il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0d4fe-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="0d4fe-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0d4fe-119">-ProfileName</span></span>
<span data-ttu-id="0d4fe-120">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="0d4fe-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="0d4fe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d4fe-121">-ResourceGroupName</span></span>
<span data-ttu-id="0d4fe-122">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d4fe-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0d4fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d4fe-123">CommonParameters</span></span>
<span data-ttu-id="0d4fe-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d4fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d4fe-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0d4fe-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d4fe-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="0d4fe-126">INPUTS</span></span>

### <span data-ttu-id="0d4fe-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d4fe-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="0d4fe-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d4fe-128">OUTPUTS</span></span>

### <span data-ttu-id="0d4fe-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="0d4fe-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="0d4fe-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="0d4fe-130">NOTES</span></span>

## <span data-ttu-id="0d4fe-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d4fe-131">RELATED LINKS</span></span>

[<span data-ttu-id="0d4fe-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d4fe-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="0d4fe-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d4fe-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="0d4fe-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="0d4fe-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


