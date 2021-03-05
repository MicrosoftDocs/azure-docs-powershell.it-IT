---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 4270f7c9781ef960cdbb20a8a067a3dc22255723
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996867"
---
# <span data-ttu-id="09322-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09322-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="09322-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09322-102">SYNOPSIS</span></span>
<span data-ttu-id="09322-103">Aggiorna un endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="09322-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="09322-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09322-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09322-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="09322-105">DESCRIPTION</span></span>
<span data-ttu-id="09322-106">Il cmdlet **Set-AzCdnEndpoint** aggiorna un endpoint della rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="09322-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="09322-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09322-107">EXAMPLES</span></span>

## <span data-ttu-id="09322-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09322-108">PARAMETERS</span></span>

### <span data-ttu-id="09322-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09322-109">-CdnEndpoint</span></span>
<span data-ttu-id="09322-110">Specifica l'endpoint a cui viene aggiornato questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09322-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="09322-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09322-111">-DefaultProfile</span></span>
<span data-ttu-id="09322-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="09322-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09322-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09322-113">-Confirm</span></span>
<span data-ttu-id="09322-114">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09322-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09322-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09322-115">-WhatIf</span></span>
<span data-ttu-id="09322-116">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09322-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09322-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09322-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09322-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09322-118">CommonParameters</span></span>
<span data-ttu-id="09322-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09322-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09322-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="09322-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09322-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="09322-121">INPUTS</span></span>

### <span data-ttu-id="09322-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="09322-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="09322-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09322-123">OUTPUTS</span></span>

### <span data-ttu-id="09322-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="09322-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="09322-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="09322-125">NOTES</span></span>

## <span data-ttu-id="09322-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09322-126">RELATED LINKS</span></span>

[<span data-ttu-id="09322-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09322-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="09322-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09322-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="09322-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09322-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="09322-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09322-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="09322-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09322-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


