---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e2588e1516b8b0ee41e260b27ea40ed72a199613
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855437"
---
# <span data-ttu-id="2480c-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="2480c-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="2480c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2480c-102">SYNOPSIS</span></span>
<span data-ttu-id="2480c-103">Ottiene l'oggetto PeerAsn da ARM.</span><span class="sxs-lookup"><span data-stu-id="2480c-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="2480c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2480c-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2480c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2480c-105">DESCRIPTION</span></span>
<span data-ttu-id="2480c-106">Ottiene il PeerAsn per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2480c-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="2480c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2480c-107">EXAMPLES</span></span>

### <span data-ttu-id="2480c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2480c-108">Example 1</span></span>
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

<span data-ttu-id="2480c-109">Ottiene il PeerAsn</span><span class="sxs-lookup"><span data-stu-id="2480c-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="2480c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2480c-110">PARAMETERS</span></span>

### <span data-ttu-id="2480c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2480c-111">-DefaultProfile</span></span>
<span data-ttu-id="2480c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2480c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2480c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2480c-113">-Name</span></span>
<span data-ttu-id="2480c-114">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="2480c-114">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2480c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2480c-115">CommonParameters</span></span>
<span data-ttu-id="2480c-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2480c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2480c-117">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2480c-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2480c-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2480c-118">INPUTS</span></span>

### <span data-ttu-id="2480c-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2480c-119">None</span></span>

## <span data-ttu-id="2480c-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2480c-120">OUTPUTS</span></span>

### <span data-ttu-id="2480c-121">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="2480c-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="2480c-122">Note</span><span class="sxs-lookup"><span data-stu-id="2480c-122">NOTES</span></span>

## <span data-ttu-id="2480c-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2480c-123">RELATED LINKS</span></span>
