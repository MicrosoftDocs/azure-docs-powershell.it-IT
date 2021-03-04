---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 2f46b13570ef1f538658dae6d02000848822c150
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953886"
---
# <span data-ttu-id="6a1dc-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="6a1dc-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="6a1dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6a1dc-103">Crea un tag IP.</span><span class="sxs-lookup"><span data-stu-id="6a1dc-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="6a1dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a1dc-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a1dc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6a1dc-105">DESCRIPTION</span></span>
<span data-ttu-id="6a1dc-106">Il cmdlet **New-AzPublicIpTag crea** un tag IP.</span><span class="sxs-lookup"><span data-stu-id="6a1dc-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="6a1dc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a1dc-107">EXAMPLES</span></span>

### <span data-ttu-id="6a1dc-108">Esempio 1: Creare un nuovo tag IP</span><span class="sxs-lookup"><span data-stu-id="6a1dc-108">Example 1: Create a new IP Tag</span></span>
```powershell
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="6a1dc-109">Questo comando crea un nuovo tag IP con tagtype come "FirstPartyUsage" e tag like "/Sql".</span><span class="sxs-lookup"><span data-stu-id="6a1dc-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="6a1dc-110">Viene usato nella creazione di publicIpAddress con questi tag specifici per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="6a1dc-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="6a1dc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a1dc-111">PARAMETERS</span></span>

### <span data-ttu-id="6a1dc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a1dc-112">-DefaultProfile</span></span>
<span data-ttu-id="6a1dc-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a1dc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a1dc-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="6a1dc-114">-IpTagType</span></span>
<span data-ttu-id="6a1dc-115">Esempio di tipo IpTag:FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="6a1dc-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1dc-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a1dc-116">-Tag</span></span>
<span data-ttu-id="6a1dc-117">Esempio di valore IpTag:/Sql</span><span class="sxs-lookup"><span data-stu-id="6a1dc-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a1dc-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a1dc-118">-Confirm</span></span>
<span data-ttu-id="6a1dc-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a1dc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a1dc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a1dc-120">-WhatIf</span></span>
<span data-ttu-id="6a1dc-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a1dc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a1dc-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a1dc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a1dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a1dc-123">CommonParameters</span></span>
<span data-ttu-id="6a1dc-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a1dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a1dc-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6a1dc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a1dc-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="6a1dc-126">INPUTS</span></span>

### <span data-ttu-id="6a1dc-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6a1dc-127">System.String</span></span>

## <span data-ttu-id="6a1dc-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a1dc-128">OUTPUTS</span></span>

### <span data-ttu-id="6a1dc-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="6a1dc-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="6a1dc-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="6a1dc-130">NOTES</span></span>

## <span data-ttu-id="6a1dc-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a1dc-131">RELATED LINKS</span></span>
