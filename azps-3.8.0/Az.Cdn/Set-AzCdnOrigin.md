---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 9635031d6eaea5a7920a6862fb8cf20ce536c1db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020790"
---
# <span data-ttu-id="08f81-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="08f81-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="08f81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08f81-102">SYNOPSIS</span></span>
<span data-ttu-id="08f81-103">Aggiorna un server di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="08f81-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="08f81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08f81-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08f81-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08f81-105">DESCRIPTION</span></span>
<span data-ttu-id="08f81-106">Il cmdlet **set-AzCdnOrigin** aggiorna un server di origine della rete CDN (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="08f81-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="08f81-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08f81-107">EXAMPLES</span></span>

## <span data-ttu-id="08f81-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08f81-108">PARAMETERS</span></span>

### <span data-ttu-id="08f81-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="08f81-109">-CdnOrigin</span></span>
<span data-ttu-id="08f81-110">Specifica il server di origine che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="08f81-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08f81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f81-111">-DefaultProfile</span></span>
<span data-ttu-id="08f81-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="08f81-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08f81-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f81-113">CommonParameters</span></span>
<span data-ttu-id="08f81-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08f81-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f81-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08f81-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f81-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08f81-116">INPUTS</span></span>

### <span data-ttu-id="08f81-117">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="08f81-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="08f81-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08f81-118">OUTPUTS</span></span>

### <span data-ttu-id="08f81-119">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="08f81-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="08f81-120">Note</span><span class="sxs-lookup"><span data-stu-id="08f81-120">NOTES</span></span>

## <span data-ttu-id="08f81-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08f81-121">RELATED LINKS</span></span>

[<span data-ttu-id="08f81-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="08f81-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


