---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: c554caf7230b54db3e1161a20e001f9873f6dfff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517016"
---
# <span data-ttu-id="78248-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="78248-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="78248-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78248-102">SYNOPSIS</span></span>
<span data-ttu-id="78248-103">Aggiorna un server di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="78248-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78248-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78248-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78248-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78248-105">DESCRIPTION</span></span>
<span data-ttu-id="78248-106">Il cmdlet **set-AzureRmCdnOrigin** aggiorna un server di origine della rete CDN (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="78248-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="78248-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78248-107">EXAMPLES</span></span>

## <span data-ttu-id="78248-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78248-108">PARAMETERS</span></span>

### <span data-ttu-id="78248-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="78248-109">-CdnOrigin</span></span>
<span data-ttu-id="78248-110">Specifica il server di origine che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="78248-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="78248-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78248-111">-DefaultProfile</span></span>
<span data-ttu-id="78248-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78248-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78248-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78248-113">CommonParameters</span></span>
<span data-ttu-id="78248-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78248-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78248-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78248-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78248-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78248-116">INPUTS</span></span>

### <span data-ttu-id="78248-117">PSOrigin</span><span class="sxs-lookup"><span data-stu-id="78248-117">PSOrigin</span></span>
<span data-ttu-id="78248-118">Il parametro ' CdnOrigin'accetta il valore di tipo ' PSOrigin'dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="78248-118">Parameter 'CdnOrigin' accepts value of type 'PSOrigin' from the pipeline</span></span>

## <span data-ttu-id="78248-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78248-119">OUTPUTS</span></span>

### <span data-ttu-id="78248-120">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="78248-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="78248-121">Note</span><span class="sxs-lookup"><span data-stu-id="78248-121">NOTES</span></span>

## <span data-ttu-id="78248-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78248-122">RELATED LINKS</span></span>

[<span data-ttu-id="78248-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="78248-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


