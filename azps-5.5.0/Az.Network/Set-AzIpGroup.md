---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189502"
---
# <span data-ttu-id="bffcd-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="bffcd-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="bffcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bffcd-102">SYNOPSIS</span></span>
<span data-ttu-id="bffcd-103">Salva un firewall modificato.</span><span class="sxs-lookup"><span data-stu-id="bffcd-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="bffcd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bffcd-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bffcd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bffcd-105">DESCRIPTION</span></span>
<span data-ttu-id="bffcd-106">Il cmdlet **Set-AzIpGroup** aggiorna un gruppo IpGroup di Azure</span><span class="sxs-lookup"><span data-stu-id="bffcd-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="bffcd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bffcd-107">EXAMPLES</span></span>

### <span data-ttu-id="bffcd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bffcd-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="bffcd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bffcd-109">PARAMETERS</span></span>

### <span data-ttu-id="bffcd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bffcd-110">-AsJob</span></span>
<span data-ttu-id="bffcd-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bffcd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bffcd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bffcd-112">-DefaultProfile</span></span>
<span data-ttu-id="bffcd-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bffcd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bffcd-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="bffcd-114">-IpGroup</span></span>
<span data-ttu-id="bffcd-115">Il gruppo IpGroup</span><span class="sxs-lookup"><span data-stu-id="bffcd-115">The IpGroup</span></span>

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

### <span data-ttu-id="bffcd-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bffcd-116">-Confirm</span></span>
<span data-ttu-id="bffcd-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bffcd-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bffcd-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bffcd-118">-WhatIf</span></span>
<span data-ttu-id="bffcd-119">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bffcd-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bffcd-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bffcd-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bffcd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bffcd-121">CommonParameters</span></span>
<span data-ttu-id="bffcd-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bffcd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bffcd-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bffcd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bffcd-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="bffcd-124">INPUTS</span></span>

### <span data-ttu-id="bffcd-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="bffcd-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="bffcd-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bffcd-126">OUTPUTS</span></span>

### <span data-ttu-id="bffcd-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="bffcd-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="bffcd-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="bffcd-128">NOTES</span></span>

## <span data-ttu-id="bffcd-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bffcd-129">RELATED LINKS</span></span>
