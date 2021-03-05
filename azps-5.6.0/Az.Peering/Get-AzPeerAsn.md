---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: 9498183e66a0991f7a724065bb5a88e954cd6594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989602"
---
# <span data-ttu-id="30b70-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="30b70-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="30b70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30b70-102">SYNOPSIS</span></span>
<span data-ttu-id="30b70-103">Recupera l'oggetto PeerAsn da ARM.</span><span class="sxs-lookup"><span data-stu-id="30b70-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="30b70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30b70-104">SYNTAX</span></span>

### <span data-ttu-id="30b70-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="30b70-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30b70-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="30b70-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30b70-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="30b70-107">DESCRIPTION</span></span>
<span data-ttu-id="30b70-108">Recupera il PeerAsn per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="30b70-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="30b70-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30b70-109">EXAMPLES</span></span>

### <span data-ttu-id="30b70-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30b70-110">Example 1</span></span>
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

<span data-ttu-id="30b70-111">Ottiene il peerAsn</span><span class="sxs-lookup"><span data-stu-id="30b70-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="30b70-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30b70-112">PARAMETERS</span></span>

### <span data-ttu-id="30b70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b70-113">-DefaultProfile</span></span>
<span data-ttu-id="30b70-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30b70-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30b70-115">-Name</span><span class="sxs-lookup"><span data-stu-id="30b70-115">-Name</span></span>
<span data-ttu-id="30b70-116">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="30b70-116">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="30b70-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30b70-117">-ResourceId</span></span>
<span data-ttu-id="30b70-118">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="30b70-118">The resource id string name.</span></span>

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

### <span data-ttu-id="30b70-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b70-119">CommonParameters</span></span>
<span data-ttu-id="30b70-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30b70-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30b70-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30b70-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b70-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="30b70-122">INPUTS</span></span>

### <span data-ttu-id="30b70-123">System.String</span><span class="sxs-lookup"><span data-stu-id="30b70-123">System.String</span></span>

## <span data-ttu-id="30b70-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30b70-124">OUTPUTS</span></span>

### <span data-ttu-id="30b70-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSZionaAsn</span><span class="sxs-lookup"><span data-stu-id="30b70-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="30b70-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="30b70-126">NOTES</span></span>

## <span data-ttu-id="30b70-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30b70-127">RELATED LINKS</span></span>
