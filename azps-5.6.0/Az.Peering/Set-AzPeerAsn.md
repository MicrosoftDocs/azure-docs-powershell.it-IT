---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: fd4058cd09ad0d0ca27f8324368cd6d0277cec7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989237"
---
# <span data-ttu-id="9893d-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="9893d-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="9893d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9893d-102">SYNOPSIS</span></span>
<span data-ttu-id="9893d-103">Aggiornare le informazioni di contatto</span><span class="sxs-lookup"><span data-stu-id="9893d-103">Update Contact Information</span></span>

## <span data-ttu-id="9893d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9893d-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9893d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9893d-105">DESCRIPTION</span></span>
<span data-ttu-id="9893d-106">Consente di aggiornare le informazioni di contatto per un peerAsn nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9893d-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="9893d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9893d-107">EXAMPLES</span></span>

### <span data-ttu-id="9893d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9893d-108">Example 1</span></span>
```powershell
#Get the Peer ASN object
PS C:> Get-AzPeerAsn -PeerName Contoso | Set-AzPeerAsn -Email noc1@contoso.com

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="9893d-109">Aggiunge un indirizzo di posta elettronica all'asn peer</span><span class="sxs-lookup"><span data-stu-id="9893d-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="9893d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9893d-110">PARAMETERS</span></span>

### <span data-ttu-id="9893d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9893d-111">-AsJob</span></span>
<span data-ttu-id="9893d-112">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="9893d-112">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9893d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9893d-113">-DefaultProfile</span></span>
<span data-ttu-id="9893d-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9893d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9893d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9893d-115">-InputObject</span></span>
<span data-ttu-id="9893d-116">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="9893d-116">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9893d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9893d-117">-Confirm</span></span>
<span data-ttu-id="9893d-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9893d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9893d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9893d-119">-WhatIf</span></span>
<span data-ttu-id="9893d-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9893d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9893d-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9893d-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9893d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9893d-122">CommonParameters</span></span>
<span data-ttu-id="9893d-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9893d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9893d-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9893d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9893d-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="9893d-125">INPUTS</span></span>

### <span data-ttu-id="9893d-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSZionaAsn</span><span class="sxs-lookup"><span data-stu-id="9893d-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="9893d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9893d-127">OUTPUTS</span></span>

### <span data-ttu-id="9893d-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSZionaAsn</span><span class="sxs-lookup"><span data-stu-id="9893d-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="9893d-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="9893d-129">NOTES</span></span>

## <span data-ttu-id="9893d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9893d-130">RELATED LINKS</span></span>
