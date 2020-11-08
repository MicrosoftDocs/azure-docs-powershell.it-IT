---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200339"
---
# <span data-ttu-id="1abfb-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="1abfb-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="1abfb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1abfb-102">SYNOPSIS</span></span>
<span data-ttu-id="1abfb-103">Aggiornare le informazioni di contatto</span><span class="sxs-lookup"><span data-stu-id="1abfb-103">Update Contact Information</span></span>

## <span data-ttu-id="1abfb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1abfb-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1abfb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1abfb-105">DESCRIPTION</span></span>
<span data-ttu-id="1abfb-106">Consente di aggiornare le informazioni di contatto per un PeerAsn nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1abfb-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="1abfb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1abfb-107">EXAMPLES</span></span>

### <span data-ttu-id="1abfb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1abfb-108">Example 1</span></span>
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

<span data-ttu-id="1abfb-109">Aggiunge un indirizzo di posta elettronica al peer ASN</span><span class="sxs-lookup"><span data-stu-id="1abfb-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="1abfb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1abfb-110">PARAMETERS</span></span>

### <span data-ttu-id="1abfb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1abfb-111">-AsJob</span></span>
<span data-ttu-id="1abfb-112">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="1abfb-112">Run in the background.</span></span>

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

### <span data-ttu-id="1abfb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1abfb-113">-DefaultProfile</span></span>
<span data-ttu-id="1abfb-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1abfb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1abfb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1abfb-115">-InputObject</span></span>
<span data-ttu-id="1abfb-116">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="1abfb-116">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="1abfb-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1abfb-117">-Confirm</span></span>
<span data-ttu-id="1abfb-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1abfb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1abfb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1abfb-119">-WhatIf</span></span>
<span data-ttu-id="1abfb-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1abfb-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1abfb-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1abfb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1abfb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1abfb-122">CommonParameters</span></span>
<span data-ttu-id="1abfb-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1abfb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1abfb-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1abfb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1abfb-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1abfb-125">INPUTS</span></span>

### <span data-ttu-id="1abfb-126">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="1abfb-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="1abfb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1abfb-127">OUTPUTS</span></span>

### <span data-ttu-id="1abfb-128">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="1abfb-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="1abfb-129">Note</span><span class="sxs-lookup"><span data-stu-id="1abfb-129">NOTES</span></span>

## <span data-ttu-id="1abfb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1abfb-130">RELATED LINKS</span></span>
