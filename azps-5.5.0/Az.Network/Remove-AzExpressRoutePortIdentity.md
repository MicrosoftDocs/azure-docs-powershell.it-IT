---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184302"
---
# <span data-ttu-id="460f0-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="460f0-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="460f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="460f0-102">SYNOPSIS</span></span>
<span data-ttu-id="460f0-103">Rimuove un'identità da ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="460f0-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="460f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="460f0-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="460f0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="460f0-105">DESCRIPTION</span></span>
<span data-ttu-id="460f0-106">Il cmdlet **Remove-AzExpressRoutePortIdentity** rimuove l'identità da un oggetto Azure ExpressRoutePort locale.</span><span class="sxs-lookup"><span data-stu-id="460f0-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="460f0-107">Usare **Remove-AzExpressRoutePort** per rimuoverlo da ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="460f0-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="460f0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="460f0-108">EXAMPLES</span></span>

### <span data-ttu-id="460f0-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="460f0-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="460f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="460f0-110">PARAMETERS</span></span>

### <span data-ttu-id="460f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="460f0-111">-DefaultProfile</span></span>
<span data-ttu-id="460f0-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="460f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="460f0-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="460f0-113">-ExpressRoutePort</span></span>
<span data-ttu-id="460f0-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="460f0-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="460f0-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="460f0-115">-Confirm</span></span>
<span data-ttu-id="460f0-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="460f0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="460f0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="460f0-117">-WhatIf</span></span>
<span data-ttu-id="460f0-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="460f0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="460f0-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="460f0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="460f0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460f0-120">CommonParameters</span></span>
<span data-ttu-id="460f0-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="460f0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460f0-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="460f0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="460f0-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="460f0-123">INPUTS</span></span>

### <span data-ttu-id="460f0-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="460f0-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="460f0-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="460f0-125">OUTPUTS</span></span>

### <span data-ttu-id="460f0-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="460f0-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="460f0-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="460f0-127">NOTES</span></span>

## <span data-ttu-id="460f0-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="460f0-128">RELATED LINKS</span></span>
[<span data-ttu-id="460f0-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="460f0-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="460f0-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="460f0-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="460f0-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="460f0-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
