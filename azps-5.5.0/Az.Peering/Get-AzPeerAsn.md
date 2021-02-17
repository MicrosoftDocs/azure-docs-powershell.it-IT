---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191462"
---
# <span data-ttu-id="1e7aa-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="1e7aa-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="1e7aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e7aa-102">SYNOPSIS</span></span>
<span data-ttu-id="1e7aa-103">Recupera l'oggetto PeerAsn da ARM.</span><span class="sxs-lookup"><span data-stu-id="1e7aa-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="1e7aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e7aa-104">SYNTAX</span></span>

### <span data-ttu-id="1e7aa-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e7aa-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e7aa-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e7aa-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e7aa-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1e7aa-107">DESCRIPTION</span></span>
<span data-ttu-id="1e7aa-108">Ottiene il PeerAsn per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1e7aa-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="1e7aa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e7aa-109">EXAMPLES</span></span>

### <span data-ttu-id="1e7aa-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e7aa-110">Example 1</span></span>
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

<span data-ttu-id="1e7aa-111">Ottiene il peerAsn</span><span class="sxs-lookup"><span data-stu-id="1e7aa-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="1e7aa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e7aa-112">PARAMETERS</span></span>

### <span data-ttu-id="1e7aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e7aa-113">-DefaultProfile</span></span>
<span data-ttu-id="1e7aa-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e7aa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e7aa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1e7aa-115">-Name</span></span>
<span data-ttu-id="1e7aa-116">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="1e7aa-116">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="1e7aa-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e7aa-117">-ResourceId</span></span>
<span data-ttu-id="1e7aa-118">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1e7aa-118">The resource id string name.</span></span>

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

### <span data-ttu-id="1e7aa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e7aa-119">CommonParameters</span></span>
<span data-ttu-id="1e7aa-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e7aa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e7aa-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1e7aa-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e7aa-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="1e7aa-122">INPUTS</span></span>

### <span data-ttu-id="1e7aa-123">System.String</span><span class="sxs-lookup"><span data-stu-id="1e7aa-123">System.String</span></span>

## <span data-ttu-id="1e7aa-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e7aa-124">OUTPUTS</span></span>

### <span data-ttu-id="1e7aa-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSZionaAsn</span><span class="sxs-lookup"><span data-stu-id="1e7aa-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="1e7aa-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="1e7aa-126">NOTES</span></span>

## <span data-ttu-id="1e7aa-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e7aa-127">RELATED LINKS</span></span>
