---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476110"
---
# <span data-ttu-id="c81f2-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="c81f2-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="c81f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c81f2-102">SYNOPSIS</span></span>
<span data-ttu-id="c81f2-103">Ottenere un elenco di negozi privati</span><span class="sxs-lookup"><span data-stu-id="c81f2-103">Get private store list</span></span>

## <span data-ttu-id="c81f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c81f2-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c81f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c81f2-105">DESCRIPTION</span></span>
<span data-ttu-id="c81f2-106">Ottenere un elenco di archivio privato creato in ambito tenant</span><span class="sxs-lookup"><span data-stu-id="c81f2-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="c81f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c81f2-107">EXAMPLES</span></span>

### <span data-ttu-id="c81f2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c81f2-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="c81f2-109">Elenco archivio privato creato in ambito tenant</span><span class="sxs-lookup"><span data-stu-id="c81f2-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="c81f2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c81f2-110">PARAMETERS</span></span>

### <span data-ttu-id="c81f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81f2-111">-DefaultProfile</span></span>
<span data-ttu-id="c81f2-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c81f2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c81f2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81f2-113">CommonParameters</span></span>
<span data-ttu-id="c81f2-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c81f2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81f2-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c81f2-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81f2-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c81f2-116">INPUTS</span></span>

### <span data-ttu-id="c81f2-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c81f2-117">None</span></span>

## <span data-ttu-id="c81f2-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c81f2-118">OUTPUTS</span></span>

### <span data-ttu-id="c81f2-119">Microsoft. Azure. Commands. Marketplace. Models. PrivateStore. PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="c81f2-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="c81f2-120">Note</span><span class="sxs-lookup"><span data-stu-id="c81f2-120">NOTES</span></span>

## <span data-ttu-id="c81f2-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c81f2-121">RELATED LINKS</span></span>
