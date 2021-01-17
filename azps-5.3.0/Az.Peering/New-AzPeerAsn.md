---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384828"
---
# <span data-ttu-id="2733a-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="2733a-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="2733a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2733a-102">SYNOPSIS</span></span>
<span data-ttu-id="2733a-103">Crea un nuovo peer ASN</span><span class="sxs-lookup"><span data-stu-id="2733a-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="2733a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2733a-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2733a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2733a-105">DESCRIPTION</span></span>
<span data-ttu-id="2733a-106">Crea un nuovo oggetto PeerAsn per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2733a-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="2733a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2733a-107">EXAMPLES</span></span>

### <span data-ttu-id="2733a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2733a-108">Example 1</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="2733a-109">Crea un nuovo PeerAsn</span><span class="sxs-lookup"><span data-stu-id="2733a-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="2733a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2733a-110">PARAMETERS</span></span>

### <span data-ttu-id="2733a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2733a-111">-AsJob</span></span>
<span data-ttu-id="2733a-112">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="2733a-112">Run in the background.</span></span>

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

### <span data-ttu-id="2733a-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="2733a-113">-ContactDetail</span></span>
<span data-ttu-id="2733a-114">Indirizzi di posta elettronica usati per contattare i problemi di arrise in genere un centro operazioni di rete</span><span class="sxs-lookup"><span data-stu-id="2733a-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2733a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2733a-115">-DefaultProfile</span></span>
<span data-ttu-id="2733a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2733a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2733a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2733a-117">-Name</span></span>
<span data-ttu-id="2733a-118">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="2733a-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2733a-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="2733a-119">-PeerAsn</span></span>
<span data-ttu-id="2733a-120">ID risorsa ASN peer. usare Get-AzPeerAsn per recuperare l'ID.</span><span class="sxs-lookup"><span data-stu-id="2733a-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="2733a-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="2733a-121">-PeerName</span></span>
<span data-ttu-id="2733a-122">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="2733a-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2733a-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2733a-123">-Confirm</span></span>
<span data-ttu-id="2733a-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2733a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2733a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2733a-125">-WhatIf</span></span>
<span data-ttu-id="2733a-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2733a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2733a-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2733a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2733a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2733a-128">CommonParameters</span></span>
<span data-ttu-id="2733a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2733a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2733a-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2733a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2733a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2733a-131">INPUTS</span></span>

### <span data-ttu-id="2733a-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2733a-132">None</span></span>

## <span data-ttu-id="2733a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2733a-133">OUTPUTS</span></span>

### <span data-ttu-id="2733a-134">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="2733a-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="2733a-135">Note</span><span class="sxs-lookup"><span data-stu-id="2733a-135">NOTES</span></span>

## <span data-ttu-id="2733a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2733a-136">RELATED LINKS</span></span>
