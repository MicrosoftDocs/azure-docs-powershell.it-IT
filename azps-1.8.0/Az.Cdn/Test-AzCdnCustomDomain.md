---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 3ab4e9c673ebea17bbf15d4f978f7c500660060a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852237"
---
# <span data-ttu-id="a1adb-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a1adb-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="a1adb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1adb-102">SYNOPSIS</span></span>
<span data-ttu-id="a1adb-103">Controlla se un dominio personalizzato può essere aggiunto a un endpoint.</span><span class="sxs-lookup"><span data-stu-id="a1adb-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="a1adb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1adb-104">SYNTAX</span></span>

### <span data-ttu-id="a1adb-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1adb-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1adb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1adb-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1adb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1adb-107">DESCRIPTION</span></span>
<span data-ttu-id="a1adb-108">Il cmdlet **test-AzCdnCustomDomain** controlla se un dominio personalizzato può essere aggiunto a un endpoint convalidando il mapping CNAME.</span><span class="sxs-lookup"><span data-stu-id="a1adb-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="a1adb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1adb-109">EXAMPLES</span></span>

## <span data-ttu-id="a1adb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1adb-110">PARAMETERS</span></span>

### <span data-ttu-id="a1adb-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1adb-111">-CdnEndpoint</span></span>
<span data-ttu-id="a1adb-112">Specifica l'endpoint a cui si vuole aggiungere il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a1adb-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="a1adb-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="a1adb-113">-CustomDomainHostName</span></span>
<span data-ttu-id="a1adb-114">Specifica il nome host del dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a1adb-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="a1adb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1adb-115">-DefaultProfile</span></span>
<span data-ttu-id="a1adb-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a1adb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1adb-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a1adb-117">-EndpointName</span></span>
<span data-ttu-id="a1adb-118">Specifica il nome dell'endpoint a cui si vuole aggiungere il dominio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="a1adb-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="a1adb-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a1adb-119">-ProfileName</span></span>
<span data-ttu-id="a1adb-120">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="a1adb-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="a1adb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1adb-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1adb-122">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1adb-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a1adb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1adb-123">CommonParameters</span></span>
<span data-ttu-id="a1adb-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1adb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1adb-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1adb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1adb-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1adb-126">INPUTS</span></span>

### <span data-ttu-id="a1adb-127">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a1adb-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="a1adb-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1adb-128">OUTPUTS</span></span>

### <span data-ttu-id="a1adb-129">Microsoft. Azure. Commands. CDN. Models. endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="a1adb-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="a1adb-130">Note</span><span class="sxs-lookup"><span data-stu-id="a1adb-130">NOTES</span></span>

## <span data-ttu-id="a1adb-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1adb-131">RELATED LINKS</span></span>

[<span data-ttu-id="a1adb-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a1adb-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="a1adb-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a1adb-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="a1adb-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a1adb-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


