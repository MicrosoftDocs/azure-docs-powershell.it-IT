---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190214"
---
# <span data-ttu-id="47bf6-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="47bf6-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="47bf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47bf6-102">SYNOPSIS</span></span>
<span data-ttu-id="47bf6-103">Ottieni l'elenco dell'archivio privato</span><span class="sxs-lookup"><span data-stu-id="47bf6-103">Get private store list</span></span>

## <span data-ttu-id="47bf6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47bf6-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47bf6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="47bf6-105">DESCRIPTION</span></span>
<span data-ttu-id="47bf6-106">Ottenere l'elenco dell'archivio privato creato nell'ambito tenant</span><span class="sxs-lookup"><span data-stu-id="47bf6-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="47bf6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47bf6-107">EXAMPLES</span></span>

### <span data-ttu-id="47bf6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="47bf6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="47bf6-109">elenco dell'archivio privato creato nell'ambito tenant</span><span class="sxs-lookup"><span data-stu-id="47bf6-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="47bf6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47bf6-110">PARAMETERS</span></span>

### <span data-ttu-id="47bf6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47bf6-111">-DefaultProfile</span></span>
<span data-ttu-id="47bf6-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47bf6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47bf6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47bf6-113">CommonParameters</span></span>
<span data-ttu-id="47bf6-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47bf6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47bf6-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47bf6-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47bf6-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="47bf6-116">INPUTS</span></span>

### <span data-ttu-id="47bf6-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="47bf6-117">None</span></span>

## <span data-ttu-id="47bf6-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47bf6-118">OUTPUTS</span></span>

### <span data-ttu-id="47bf6-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="47bf6-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="47bf6-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="47bf6-120">NOTES</span></span>

## <span data-ttu-id="47bf6-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47bf6-121">RELATED LINKS</span></span>
