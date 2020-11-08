---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032301"
---
# <span data-ttu-id="a2db7-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="a2db7-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="a2db7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2db7-102">SYNOPSIS</span></span>
<span data-ttu-id="a2db7-103">Salva un firewall modificato.</span><span class="sxs-lookup"><span data-stu-id="a2db7-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="a2db7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2db7-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2db7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2db7-105">DESCRIPTION</span></span>
<span data-ttu-id="a2db7-106">Il cmdlet **set-AzIpGroup** aggiorna un IpGroup di Azure</span><span class="sxs-lookup"><span data-stu-id="a2db7-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="a2db7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2db7-107">EXAMPLES</span></span>

### <span data-ttu-id="a2db7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2db7-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="a2db7-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2db7-109">PARAMETERS</span></span>

### <span data-ttu-id="a2db7-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2db7-110">-AsJob</span></span>
<span data-ttu-id="a2db7-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a2db7-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2db7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2db7-112">-DefaultProfile</span></span>
<span data-ttu-id="a2db7-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2db7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2db7-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="a2db7-114">-IpGroup</span></span>
<span data-ttu-id="a2db7-115">IpGroup</span><span class="sxs-lookup"><span data-stu-id="a2db7-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2db7-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a2db7-116">-Confirm</span></span>
<span data-ttu-id="a2db7-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2db7-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2db7-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2db7-118">-WhatIf</span></span>
<span data-ttu-id="a2db7-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2db7-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2db7-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2db7-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2db7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2db7-121">CommonParameters</span></span>
<span data-ttu-id="a2db7-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2db7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2db7-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2db7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2db7-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2db7-124">INPUTS</span></span>

### <span data-ttu-id="a2db7-125">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="a2db7-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="a2db7-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2db7-126">OUTPUTS</span></span>

### <span data-ttu-id="a2db7-127">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="a2db7-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="a2db7-128">Note</span><span class="sxs-lookup"><span data-stu-id="a2db7-128">NOTES</span></span>

## <span data-ttu-id="a2db7-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2db7-129">RELATED LINKS</span></span>
