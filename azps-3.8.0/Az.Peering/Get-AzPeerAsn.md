---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: 559d2d8c069d7e36630600d0fcdc16ea475da9f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022449"
---
# <span data-ttu-id="a3dff-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a3dff-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="a3dff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3dff-102">SYNOPSIS</span></span>
<span data-ttu-id="a3dff-103">Ottiene l'oggetto PeerAsn da ARM.</span><span class="sxs-lookup"><span data-stu-id="a3dff-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="a3dff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3dff-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3dff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3dff-105">DESCRIPTION</span></span>
<span data-ttu-id="a3dff-106">Ottiene il PeerAsn per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a3dff-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="a3dff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3dff-107">EXAMPLES</span></span>

### <span data-ttu-id="a3dff-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3dff-108">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -PeerName Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="a3dff-109">Ottiene il PeerAsn</span><span class="sxs-lookup"><span data-stu-id="a3dff-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="a3dff-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3dff-110">PARAMETERS</span></span>

### <span data-ttu-id="a3dff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3dff-111">-DefaultProfile</span></span>
<span data-ttu-id="a3dff-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3dff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3dff-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3dff-113">-Name</span></span>
<span data-ttu-id="a3dff-114">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="a3dff-114">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3dff-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3dff-115">CommonParameters</span></span>
<span data-ttu-id="a3dff-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3dff-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3dff-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3dff-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3dff-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3dff-118">INPUTS</span></span>

### <span data-ttu-id="a3dff-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a3dff-119">None</span></span>

## <span data-ttu-id="a3dff-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3dff-120">OUTPUTS</span></span>

### <span data-ttu-id="a3dff-121">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a3dff-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="a3dff-122">Note</span><span class="sxs-lookup"><span data-stu-id="a3dff-122">NOTES</span></span>

## <span data-ttu-id="a3dff-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3dff-123">RELATED LINKS</span></span>
