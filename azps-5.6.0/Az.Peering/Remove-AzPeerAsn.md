---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: a5b50fd4d57fc7036196decdb7b967e2867b21f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989322"
---
# <span data-ttu-id="b9d7a-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="b9d7a-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="b9d7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9d7a-103">Rimuovi Peer Asn</span><span class="sxs-lookup"><span data-stu-id="b9d7a-103">Remove Peer Asn</span></span>

## <span data-ttu-id="b9d7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9d7a-104">SYNTAX</span></span>

### <span data-ttu-id="b9d7a-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9d7a-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9d7a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b9d7a-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9d7a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9d7a-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9d7a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b9d7a-108">DESCRIPTION</span></span>
<span data-ttu-id="b9d7a-109">Rimuovere un peerAsn dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b9d7a-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="b9d7a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9d7a-110">EXAMPLES</span></span>

### <span data-ttu-id="b9d7a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b9d7a-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="b9d7a-112">Rimuove l'asn peer</span><span class="sxs-lookup"><span data-stu-id="b9d7a-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="b9d7a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9d7a-113">PARAMETERS</span></span>

### <span data-ttu-id="b9d7a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9d7a-114">-AsJob</span></span>
<span data-ttu-id="b9d7a-115">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="b9d7a-115">Run in the background.</span></span>

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

### <span data-ttu-id="b9d7a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9d7a-116">-DefaultProfile</span></span>
<span data-ttu-id="b9d7a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9d7a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9d7a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b9d7a-118">-Force</span></span>
<span data-ttu-id="b9d7a-119">{{ Fill Force Description }}</span><span class="sxs-lookup"><span data-stu-id="b9d7a-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="b9d7a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9d7a-120">-InputObject</span></span>
<span data-ttu-id="b9d7a-121">Oggetto PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="b9d7a-121">The PeerAsn object.</span></span>

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

### <span data-ttu-id="b9d7a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b9d7a-122">-Name</span></span>
<span data-ttu-id="b9d7a-123">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="b9d7a-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b9d7a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9d7a-124">-PassThru</span></span>
<span data-ttu-id="b9d7a-125">Return true if complete</span><span class="sxs-lookup"><span data-stu-id="b9d7a-125">Return true if complete</span></span>

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

### <span data-ttu-id="b9d7a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9d7a-126">-ResourceId</span></span>
<span data-ttu-id="b9d7a-127">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b9d7a-127">The resource id string name.</span></span>

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

### <span data-ttu-id="b9d7a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9d7a-128">-Confirm</span></span>
<span data-ttu-id="b9d7a-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9d7a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9d7a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9d7a-130">-WhatIf</span></span>
<span data-ttu-id="b9d7a-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9d7a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9d7a-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9d7a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9d7a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9d7a-133">CommonParameters</span></span>
<span data-ttu-id="b9d7a-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9d7a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9d7a-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b9d7a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9d7a-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="b9d7a-136">INPUTS</span></span>

### <span data-ttu-id="b9d7a-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSZionaAsn</span><span class="sxs-lookup"><span data-stu-id="b9d7a-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="b9d7a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b9d7a-138">System.String</span></span>

## <span data-ttu-id="b9d7a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9d7a-139">OUTPUTS</span></span>

### <span data-ttu-id="b9d7a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9d7a-140">System.Boolean</span></span>

## <span data-ttu-id="b9d7a-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="b9d7a-141">NOTES</span></span>

## <span data-ttu-id="b9d7a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9d7a-142">RELATED LINKS</span></span>
