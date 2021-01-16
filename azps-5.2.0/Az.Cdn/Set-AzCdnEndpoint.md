---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 7222b33470dc1fff22039c5e88bf3c6560b80c31
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336727"
---
# <span data-ttu-id="7dfb0-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7dfb0-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="7dfb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7dfb0-102">SYNOPSIS</span></span>
<span data-ttu-id="7dfb0-103">Aggiorna un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="7dfb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7dfb0-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7dfb0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dfb0-105">DESCRIPTION</span></span>
<span data-ttu-id="7dfb0-106">Il cmdlet **set-AzCdnEndpoint** aggiorna un endpoint della rete CDN (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="7dfb0-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7dfb0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7dfb0-107">EXAMPLES</span></span>

## <span data-ttu-id="7dfb0-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7dfb0-108">PARAMETERS</span></span>

### <span data-ttu-id="7dfb0-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7dfb0-109">-CdnEndpoint</span></span>
<span data-ttu-id="7dfb0-110">Specifica l'endpoint che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="7dfb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dfb0-111">-DefaultProfile</span></span>
<span data-ttu-id="7dfb0-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7dfb0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7dfb0-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7dfb0-113">-Confirm</span></span>
<span data-ttu-id="7dfb0-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dfb0-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dfb0-115">-WhatIf</span></span>
<span data-ttu-id="7dfb0-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dfb0-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dfb0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dfb0-118">CommonParameters</span></span>
<span data-ttu-id="7dfb0-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dfb0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dfb0-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7dfb0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dfb0-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7dfb0-121">INPUTS</span></span>

### <span data-ttu-id="7dfb0-122">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7dfb0-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7dfb0-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7dfb0-123">OUTPUTS</span></span>

### <span data-ttu-id="7dfb0-124">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7dfb0-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7dfb0-125">Note</span><span class="sxs-lookup"><span data-stu-id="7dfb0-125">NOTES</span></span>

## <span data-ttu-id="7dfb0-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7dfb0-126">RELATED LINKS</span></span>

[<span data-ttu-id="7dfb0-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7dfb0-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="7dfb0-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7dfb0-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="7dfb0-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7dfb0-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="7dfb0-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7dfb0-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="7dfb0-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7dfb0-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


