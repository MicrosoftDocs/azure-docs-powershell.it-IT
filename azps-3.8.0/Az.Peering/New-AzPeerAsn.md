---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: f811f73b50f88a256de62069a287d113607e7ee1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022433"
---
# <span data-ttu-id="64a58-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="64a58-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="64a58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64a58-102">SYNOPSIS</span></span>
<span data-ttu-id="64a58-103">Crea un nuovo peer ASN</span><span class="sxs-lookup"><span data-stu-id="64a58-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="64a58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64a58-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -Email <String[]> -Phone <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64a58-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64a58-105">DESCRIPTION</span></span>
<span data-ttu-id="64a58-106">Crea un nuovo oggetto PeerAsn per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="64a58-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="64a58-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64a58-107">EXAMPLES</span></span>

### <span data-ttu-id="64a58-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="64a58-108">Example 1</span></span>
```powershell
PS C:> New-AzPeerAsn -Name Contoso65050 -PeerName Contoso -PeerAsn 65050 -Emails noc@contoso.com -Phone "888-888-8889"

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="64a58-109">Crea un nuovo PeerAsn</span><span class="sxs-lookup"><span data-stu-id="64a58-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="64a58-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64a58-110">PARAMETERS</span></span>

### <span data-ttu-id="64a58-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64a58-111">-AsJob</span></span>
<span data-ttu-id="64a58-112">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="64a58-112">Run in the background.</span></span>

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

### <span data-ttu-id="64a58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a58-113">-DefaultProfile</span></span>
<span data-ttu-id="64a58-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64a58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a58-115">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="64a58-115">-Email</span></span>
<span data-ttu-id="64a58-116">Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="64a58-116">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a58-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="64a58-117">-Name</span></span>
<span data-ttu-id="64a58-118">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="64a58-118">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a58-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="64a58-119">-PeerAsn</span></span>
<span data-ttu-id="64a58-120">ID risorsa ASN peer. usare Get-AzPeerAsn per recuperare l'ID.</span><span class="sxs-lookup"><span data-stu-id="64a58-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a58-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="64a58-121">-PeerName</span></span>
<span data-ttu-id="64a58-122">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="64a58-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a58-123">-Telefono</span><span class="sxs-lookup"><span data-stu-id="64a58-123">-Phone</span></span>
<span data-ttu-id="64a58-124">Telefono</span><span class="sxs-lookup"><span data-stu-id="64a58-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64a58-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64a58-125">-Confirm</span></span>
<span data-ttu-id="64a58-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64a58-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a58-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a58-127">-WhatIf</span></span>
<span data-ttu-id="64a58-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64a58-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64a58-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64a58-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a58-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a58-130">CommonParameters</span></span>
<span data-ttu-id="64a58-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a58-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a58-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64a58-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a58-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64a58-133">INPUTS</span></span>

### <span data-ttu-id="64a58-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="64a58-134">None</span></span>

## <span data-ttu-id="64a58-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64a58-135">OUTPUTS</span></span>

### <span data-ttu-id="64a58-136">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="64a58-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="64a58-137">Note</span><span class="sxs-lookup"><span data-stu-id="64a58-137">NOTES</span></span>

## <span data-ttu-id="64a58-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64a58-138">RELATED LINKS</span></span>
