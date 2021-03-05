---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 22644dca713ef234aec8be17c324faaf90eebf20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996363"
---
# <span data-ttu-id="496e9-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="496e9-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="496e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="496e9-102">SYNOPSIS</span></span>
<span data-ttu-id="496e9-103">Rimuove un'identità da ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="496e9-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="496e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="496e9-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="496e9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="496e9-105">DESCRIPTION</span></span>
<span data-ttu-id="496e9-106">Il cmdlet **Remove-AzExpressRoutePortIdentity** rimuove l'identità da un oggetto Azure ExpressRoutePort locale.</span><span class="sxs-lookup"><span data-stu-id="496e9-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="496e9-107">Usare **Remove-AzExpressRoutePort** per rimuoverlo da ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="496e9-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="496e9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="496e9-108">EXAMPLES</span></span>

### <span data-ttu-id="496e9-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="496e9-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="496e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="496e9-110">PARAMETERS</span></span>

### <span data-ttu-id="496e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496e9-111">-DefaultProfile</span></span>
<span data-ttu-id="496e9-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="496e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="496e9-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="496e9-113">-ExpressRoutePort</span></span>
<span data-ttu-id="496e9-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="496e9-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="496e9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="496e9-115">-Confirm</span></span>
<span data-ttu-id="496e9-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="496e9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="496e9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="496e9-117">-WhatIf</span></span>
<span data-ttu-id="496e9-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="496e9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="496e9-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="496e9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="496e9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496e9-120">CommonParameters</span></span>
<span data-ttu-id="496e9-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="496e9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496e9-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="496e9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="496e9-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="496e9-123">INPUTS</span></span>

### <span data-ttu-id="496e9-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="496e9-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="496e9-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="496e9-125">OUTPUTS</span></span>

### <span data-ttu-id="496e9-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="496e9-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="496e9-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="496e9-127">NOTES</span></span>

## <span data-ttu-id="496e9-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="496e9-128">RELATED LINKS</span></span>
[<span data-ttu-id="496e9-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="496e9-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="496e9-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="496e9-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="496e9-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="496e9-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
