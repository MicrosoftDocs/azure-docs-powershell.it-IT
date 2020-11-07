---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: 82a112363a561e7566b0d748d00acc75dc026ebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855397"
---
# <span data-ttu-id="b47cb-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="b47cb-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="b47cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b47cb-102">SYNOPSIS</span></span>
<span data-ttu-id="b47cb-103">Rimuovere peer ASN</span><span class="sxs-lookup"><span data-stu-id="b47cb-103">Remove Peer Asn</span></span>

## <span data-ttu-id="b47cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b47cb-104">SYNTAX</span></span>

### <span data-ttu-id="b47cb-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b47cb-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b47cb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b47cb-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b47cb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b47cb-107">DESCRIPTION</span></span>
<span data-ttu-id="b47cb-108">Rimuovere un PeerAsn dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b47cb-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="b47cb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b47cb-109">EXAMPLES</span></span>

### <span data-ttu-id="b47cb-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b47cb-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="b47cb-111">Rimuove il peer ASN</span><span class="sxs-lookup"><span data-stu-id="b47cb-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="b47cb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b47cb-112">PARAMETERS</span></span>

### <span data-ttu-id="b47cb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b47cb-113">-AsJob</span></span>
<span data-ttu-id="b47cb-114">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="b47cb-114">Run in the background.</span></span>

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

### <span data-ttu-id="b47cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b47cb-115">-DefaultProfile</span></span>
<span data-ttu-id="b47cb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b47cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b47cb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b47cb-117">-Force</span></span>
<span data-ttu-id="b47cb-118">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="b47cb-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="b47cb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b47cb-119">-InputObject</span></span>
<span data-ttu-id="b47cb-120">Oggetto PeerAsn.</span><span class="sxs-lookup"><span data-stu-id="b47cb-120">The PeerAsn object.</span></span>

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

### <span data-ttu-id="b47cb-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b47cb-121">-Name</span></span>
<span data-ttu-id="b47cb-122">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b47cb-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b47cb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b47cb-123">-PassThru</span></span>
<span data-ttu-id="b47cb-124">Restituisce vero se completo</span><span class="sxs-lookup"><span data-stu-id="b47cb-124">Return true if complete</span></span>

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

### <span data-ttu-id="b47cb-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b47cb-125">-Confirm</span></span>
<span data-ttu-id="b47cb-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b47cb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b47cb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b47cb-127">-WhatIf</span></span>
<span data-ttu-id="b47cb-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b47cb-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b47cb-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b47cb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b47cb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b47cb-130">CommonParameters</span></span>
<span data-ttu-id="b47cb-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b47cb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b47cb-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b47cb-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b47cb-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b47cb-133">INPUTS</span></span>

### <span data-ttu-id="b47cb-134">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="b47cb-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="b47cb-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b47cb-135">OUTPUTS</span></span>

### <span data-ttu-id="b47cb-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b47cb-136">System.Boolean</span></span>

## <span data-ttu-id="b47cb-137">Note</span><span class="sxs-lookup"><span data-stu-id="b47cb-137">NOTES</span></span>

## <span data-ttu-id="b47cb-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b47cb-138">RELATED LINKS</span></span>
