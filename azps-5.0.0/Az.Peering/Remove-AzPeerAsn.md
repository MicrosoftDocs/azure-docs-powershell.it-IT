---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199829"
---
# <span data-ttu-id="d1987-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="d1987-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="d1987-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1987-102">SYNOPSIS</span></span>
<span data-ttu-id="d1987-103">Rimuovere peer ASN</span><span class="sxs-lookup"><span data-stu-id="d1987-103">Remove Peer Asn</span></span>

## <span data-ttu-id="d1987-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1987-104">SYNTAX</span></span>

### <span data-ttu-id="d1987-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1987-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1987-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d1987-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1987-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1987-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1987-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1987-108">DESCRIPTION</span></span>
<span data-ttu-id="d1987-109">Rimuovere un PeerAsn dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d1987-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="d1987-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1987-110">EXAMPLES</span></span>

### <span data-ttu-id="d1987-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1987-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="d1987-112">Rimuove il peer ASN</span><span class="sxs-lookup"><span data-stu-id="d1987-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="d1987-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1987-113">PARAMETERS</span></span>

### <span data-ttu-id="d1987-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1987-114">-AsJob</span></span>
<span data-ttu-id="d1987-115">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="d1987-115">Run in the background.</span></span>

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

### <span data-ttu-id="d1987-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1987-116">-DefaultProfile</span></span>
<span data-ttu-id="d1987-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1987-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1987-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d1987-118">-Force</span></span>
<span data-ttu-id="d1987-119">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="d1987-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="d1987-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1987-120">-InputObject</span></span>
<span data-ttu-id="d1987-121">Oggetto PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="d1987-121">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1987-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1987-122">-Name</span></span>
<span data-ttu-id="d1987-123">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d1987-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1987-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1987-124">-PassThru</span></span>
<span data-ttu-id="d1987-125">Restituisce vero se completo</span><span class="sxs-lookup"><span data-stu-id="d1987-125">Return true if complete</span></span>

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

### <span data-ttu-id="d1987-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1987-126">-ResourceId</span></span>
<span data-ttu-id="d1987-127">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d1987-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1987-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d1987-128">-Confirm</span></span>
<span data-ttu-id="d1987-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1987-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1987-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1987-130">-WhatIf</span></span>
<span data-ttu-id="d1987-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1987-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1987-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1987-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1987-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1987-133">CommonParameters</span></span>
<span data-ttu-id="d1987-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1987-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1987-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1987-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1987-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1987-136">INPUTS</span></span>

### <span data-ttu-id="d1987-137">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="d1987-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="d1987-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d1987-138">System.String</span></span>

## <span data-ttu-id="d1987-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1987-139">OUTPUTS</span></span>

### <span data-ttu-id="d1987-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1987-140">System.Boolean</span></span>

## <span data-ttu-id="d1987-141">Note</span><span class="sxs-lookup"><span data-stu-id="d1987-141">NOTES</span></span>

## <span data-ttu-id="d1987-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1987-142">RELATED LINKS</span></span>
