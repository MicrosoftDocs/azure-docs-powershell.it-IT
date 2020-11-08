---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032261"
---
# <span data-ttu-id="0f5b5-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="0f5b5-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="0f5b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f5b5-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5b5-103">Ottiene l'oggetto PeerAsn da ARM.</span><span class="sxs-lookup"><span data-stu-id="0f5b5-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="0f5b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f5b5-104">SYNTAX</span></span>

### <span data-ttu-id="0f5b5-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f5b5-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f5b5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f5b5-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f5b5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f5b5-107">DESCRIPTION</span></span>
<span data-ttu-id="0f5b5-108">Ottiene il PeerAsn per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0f5b5-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="0f5b5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f5b5-109">EXAMPLES</span></span>

### <span data-ttu-id="0f5b5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f5b5-110">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -Name Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="0f5b5-111">Ottiene il PeerAsn</span><span class="sxs-lookup"><span data-stu-id="0f5b5-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="0f5b5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f5b5-112">PARAMETERS</span></span>

### <span data-ttu-id="0f5b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f5b5-113">-DefaultProfile</span></span>
<span data-ttu-id="0f5b5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f5b5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f5b5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f5b5-115">-Name</span></span>
<span data-ttu-id="0f5b5-116">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="0f5b5-116">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f5b5-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f5b5-117">-ResourceId</span></span>
<span data-ttu-id="0f5b5-118">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f5b5-118">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f5b5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5b5-119">CommonParameters</span></span>
<span data-ttu-id="0f5b5-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f5b5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5b5-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f5b5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5b5-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f5b5-122">INPUTS</span></span>

### <span data-ttu-id="0f5b5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0f5b5-123">System.String</span></span>

## <span data-ttu-id="0f5b5-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f5b5-124">OUTPUTS</span></span>

### <span data-ttu-id="0f5b5-125">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="0f5b5-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="0f5b5-126">Note</span><span class="sxs-lookup"><span data-stu-id="0f5b5-126">NOTES</span></span>

## <span data-ttu-id="0f5b5-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f5b5-127">RELATED LINKS</span></span>
