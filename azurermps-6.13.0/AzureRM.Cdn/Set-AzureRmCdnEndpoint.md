---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 3705cd0b20927c4b10360b7e02d507227ef2ec53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517519"
---
# <span data-ttu-id="71af9-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="71af9-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="71af9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71af9-102">SYNOPSIS</span></span>
<span data-ttu-id="71af9-103">Aggiorna un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="71af9-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71af9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71af9-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71af9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71af9-105">DESCRIPTION</span></span>
<span data-ttu-id="71af9-106">Il cmdlet **set-AzureRmCdnEndpoint** aggiorna un endpoint della rete CDN (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="71af9-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="71af9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71af9-107">EXAMPLES</span></span>

## <span data-ttu-id="71af9-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71af9-108">PARAMETERS</span></span>

### <span data-ttu-id="71af9-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="71af9-109">-CdnEndpoint</span></span>
<span data-ttu-id="71af9-110">Specifica l'endpoint che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="71af9-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="71af9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71af9-111">-DefaultProfile</span></span>
<span data-ttu-id="71af9-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="71af9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71af9-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71af9-113">-Confirm</span></span>
<span data-ttu-id="71af9-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71af9-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71af9-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71af9-115">-WhatIf</span></span>
<span data-ttu-id="71af9-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71af9-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71af9-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71af9-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71af9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71af9-118">CommonParameters</span></span>
<span data-ttu-id="71af9-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71af9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71af9-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71af9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71af9-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71af9-121">INPUTS</span></span>

### <span data-ttu-id="71af9-122">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="71af9-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="71af9-123">Parametri: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="71af9-123">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="71af9-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71af9-124">OUTPUTS</span></span>

### <span data-ttu-id="71af9-125">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="71af9-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="71af9-126">Note</span><span class="sxs-lookup"><span data-stu-id="71af9-126">NOTES</span></span>

## <span data-ttu-id="71af9-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71af9-127">RELATED LINKS</span></span>

[<span data-ttu-id="71af9-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="71af9-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="71af9-129">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="71af9-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="71af9-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="71af9-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="71af9-131">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="71af9-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="71af9-132">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="71af9-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


