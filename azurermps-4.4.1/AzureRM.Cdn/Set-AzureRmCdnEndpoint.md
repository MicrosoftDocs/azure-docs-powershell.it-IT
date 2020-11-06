---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 70a6e57b45e1703b06343cb66d5b83b526b55063
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517023"
---
# <span data-ttu-id="dd79c-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd79c-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="dd79c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd79c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd79c-103">Aggiorna un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="dd79c-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd79c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd79c-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd79c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd79c-105">DESCRIPTION</span></span>
<span data-ttu-id="dd79c-106">Il cmdlet **set-AzureRmCdnEndpoint** aggiorna un endpoint della rete CDN (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="dd79c-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="dd79c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd79c-107">EXAMPLES</span></span>

## <span data-ttu-id="dd79c-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd79c-108">PARAMETERS</span></span>

### <span data-ttu-id="dd79c-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd79c-109">-CdnEndpoint</span></span>
<span data-ttu-id="dd79c-110">Specifica l'endpoint che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="dd79c-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd79c-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd79c-111">-Confirm</span></span>
<span data-ttu-id="dd79c-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd79c-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd79c-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd79c-113">-WhatIf</span></span>
<span data-ttu-id="dd79c-114">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd79c-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd79c-115">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd79c-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd79c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd79c-116">-DefaultProfile</span></span>
<span data-ttu-id="dd79c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd79c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd79c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd79c-118">CommonParameters</span></span>
<span data-ttu-id="dd79c-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd79c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd79c-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd79c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd79c-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd79c-121">INPUTS</span></span>

### <span data-ttu-id="dd79c-122">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd79c-122">PSEndpoint</span></span>
<span data-ttu-id="dd79c-123">Il parametro ' CdnEndpoint ' accetta il valore di tipo ' PSEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="dd79c-123">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="dd79c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd79c-124">OUTPUTS</span></span>

### <span data-ttu-id="dd79c-125">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd79c-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="dd79c-126">Note</span><span class="sxs-lookup"><span data-stu-id="dd79c-126">NOTES</span></span>

## <span data-ttu-id="dd79c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd79c-127">RELATED LINKS</span></span>

[<span data-ttu-id="dd79c-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd79c-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="dd79c-129">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd79c-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="dd79c-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd79c-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="dd79c-131">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd79c-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="dd79c-132">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd79c-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


