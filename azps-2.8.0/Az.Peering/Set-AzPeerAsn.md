---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: 81398d4ab62db1b8dca573dfd6beccde3be63700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855389"
---
# <span data-ttu-id="44ba6-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="44ba6-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="44ba6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="44ba6-103">Aggiornare le informazioni di contatto</span><span class="sxs-lookup"><span data-stu-id="44ba6-103">Update Contact Information</span></span>

## <span data-ttu-id="44ba6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44ba6-104">SYNTAX</span></span>

### <span data-ttu-id="44ba6-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="44ba6-105">ByName (Default)</span></span>
```
Set-AzPeerAsn [-Name] <String> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44ba6-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="44ba6-106">Default</span></span>
```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44ba6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44ba6-107">DESCRIPTION</span></span>
<span data-ttu-id="44ba6-108">Consente di aggiornare le informazioni di contatto per un PeerAsn nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="44ba6-108">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="44ba6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44ba6-109">EXAMPLES</span></span>

### <span data-ttu-id="44ba6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="44ba6-110">Example 1</span></span>
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

<span data-ttu-id="44ba6-111">Aggiunge un indirizzo di posta elettronica al peer ASN</span><span class="sxs-lookup"><span data-stu-id="44ba6-111">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="44ba6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44ba6-112">PARAMETERS</span></span>

### <span data-ttu-id="44ba6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44ba6-113">-AsJob</span></span>
<span data-ttu-id="44ba6-114">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="44ba6-114">Run in the background.</span></span>

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

### <span data-ttu-id="44ba6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ba6-115">-DefaultProfile</span></span>
<span data-ttu-id="44ba6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="44ba6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44ba6-117">-Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="44ba6-117">-Email</span></span>
<span data-ttu-id="44ba6-118">Posta elettronica</span><span class="sxs-lookup"><span data-stu-id="44ba6-118">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ba6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44ba6-119">-InputObject</span></span>
<span data-ttu-id="44ba6-120">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="44ba6-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44ba6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="44ba6-121">-Name</span></span>
<span data-ttu-id="44ba6-122">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="44ba6-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ba6-123">-Telefono</span><span class="sxs-lookup"><span data-stu-id="44ba6-123">-Phone</span></span>
<span data-ttu-id="44ba6-124">Telefono</span><span class="sxs-lookup"><span data-stu-id="44ba6-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ba6-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44ba6-125">-Confirm</span></span>
<span data-ttu-id="44ba6-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44ba6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44ba6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44ba6-127">-WhatIf</span></span>
<span data-ttu-id="44ba6-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44ba6-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44ba6-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44ba6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44ba6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ba6-130">CommonParameters</span></span>
<span data-ttu-id="44ba6-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44ba6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ba6-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44ba6-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ba6-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44ba6-133">INPUTS</span></span>

### <span data-ttu-id="44ba6-134">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="44ba6-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="44ba6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44ba6-135">OUTPUTS</span></span>

### <span data-ttu-id="44ba6-136">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="44ba6-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="44ba6-137">Note</span><span class="sxs-lookup"><span data-stu-id="44ba6-137">NOTES</span></span>

## <span data-ttu-id="44ba6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44ba6-138">RELATED LINKS</span></span>
