---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192047"
---
# <span data-ttu-id="c14f4-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="c14f4-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="c14f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c14f4-102">SYNOPSIS</span></span>
<span data-ttu-id="c14f4-103">Rimuove un'identità da un ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c14f4-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="c14f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c14f4-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c14f4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c14f4-105">DESCRIPTION</span></span>
<span data-ttu-id="c14f4-106">Il cmdlet **Remove-AzExpressRoutePortIdentity** rimuove l'identità da un oggetto ExpressRoutePort di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="c14f4-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="c14f4-107">Usare **Remove-AzExpressRoutePort** per rimuoverlo da ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c14f4-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="c14f4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c14f4-108">EXAMPLES</span></span>

### <span data-ttu-id="c14f4-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c14f4-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="c14f4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c14f4-110">PARAMETERS</span></span>

### <span data-ttu-id="c14f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c14f4-111">-DefaultProfile</span></span>
<span data-ttu-id="c14f4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c14f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c14f4-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c14f4-113">-ExpressRoutePort</span></span>
<span data-ttu-id="c14f4-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c14f4-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="c14f4-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c14f4-115">-Confirm</span></span>
<span data-ttu-id="c14f4-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c14f4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c14f4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c14f4-117">-WhatIf</span></span>
<span data-ttu-id="c14f4-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c14f4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c14f4-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c14f4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c14f4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c14f4-120">CommonParameters</span></span>
<span data-ttu-id="c14f4-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c14f4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c14f4-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c14f4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="c14f4-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c14f4-123">INPUTS</span></span>

### <span data-ttu-id="c14f4-124">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c14f4-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c14f4-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c14f4-125">OUTPUTS</span></span>

### <span data-ttu-id="c14f4-126">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c14f4-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c14f4-127">Note</span><span class="sxs-lookup"><span data-stu-id="c14f4-127">NOTES</span></span>

## <span data-ttu-id="c14f4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c14f4-128">RELATED LINKS</span></span>
[<span data-ttu-id="c14f4-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="c14f4-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="c14f4-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="c14f4-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="c14f4-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="c14f4-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)