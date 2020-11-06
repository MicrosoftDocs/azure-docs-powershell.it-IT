---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: 395ee4b20ae2c26d05ad66489b3c643d0f4245a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517515"
---
# <span data-ttu-id="ba439-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ba439-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="ba439-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba439-102">SYNOPSIS</span></span>
<span data-ttu-id="ba439-103">Aggiorna un server di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="ba439-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba439-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba439-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba439-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba439-105">DESCRIPTION</span></span>
<span data-ttu-id="ba439-106">Il cmdlet **set-AzureRmCdnOrigin** aggiorna un server di origine della rete CDN (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="ba439-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="ba439-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba439-107">EXAMPLES</span></span>

## <span data-ttu-id="ba439-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba439-108">PARAMETERS</span></span>

### <span data-ttu-id="ba439-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ba439-109">-CdnOrigin</span></span>
<span data-ttu-id="ba439-110">Specifica il server di origine che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="ba439-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="ba439-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba439-111">-DefaultProfile</span></span>
<span data-ttu-id="ba439-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ba439-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba439-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba439-113">CommonParameters</span></span>
<span data-ttu-id="ba439-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba439-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba439-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba439-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba439-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba439-116">INPUTS</span></span>

### <span data-ttu-id="ba439-117">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="ba439-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>
<span data-ttu-id="ba439-118">Parametri: CdnOrigin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ba439-118">Parameters: CdnOrigin (ByValue)</span></span>

## <span data-ttu-id="ba439-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba439-119">OUTPUTS</span></span>

### <span data-ttu-id="ba439-120">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="ba439-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="ba439-121">Note</span><span class="sxs-lookup"><span data-stu-id="ba439-121">NOTES</span></span>

## <span data-ttu-id="ba439-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba439-122">RELATED LINKS</span></span>

[<span data-ttu-id="ba439-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ba439-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


