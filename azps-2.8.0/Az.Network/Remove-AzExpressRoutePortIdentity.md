---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c7ffb86fa56a09fb0c5bbdd41e62bf8d47bee140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852753"
---
# <span data-ttu-id="53b28-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="53b28-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="53b28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53b28-102">SYNOPSIS</span></span>
<span data-ttu-id="53b28-103">Rimuove un'identità da un ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="53b28-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="53b28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53b28-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53b28-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53b28-105">DESCRIPTION</span></span>
<span data-ttu-id="53b28-106">Il cmdlet **Remove-AzExpressRoutePortIdentity** rimuove l'identità da un oggetto ExpressRoutePort di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="53b28-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="53b28-107">Usare **Remove-AzExpressRoutePort** per rimuoverlo da ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="53b28-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="53b28-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53b28-108">EXAMPLES</span></span>

### <span data-ttu-id="53b28-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53b28-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="53b28-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53b28-110">PARAMETERS</span></span>

### <span data-ttu-id="53b28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53b28-111">-DefaultProfile</span></span>
<span data-ttu-id="53b28-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53b28-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53b28-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="53b28-113">-ExpressRoutePort</span></span>
<span data-ttu-id="53b28-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="53b28-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="53b28-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53b28-115">-Confirm</span></span>
<span data-ttu-id="53b28-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53b28-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53b28-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53b28-117">-WhatIf</span></span>
<span data-ttu-id="53b28-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53b28-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53b28-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53b28-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53b28-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53b28-120">CommonParameters</span></span>
<span data-ttu-id="53b28-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53b28-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53b28-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53b28-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="53b28-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53b28-123">INPUTS</span></span>

### <span data-ttu-id="53b28-124">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="53b28-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="53b28-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53b28-125">OUTPUTS</span></span>

### <span data-ttu-id="53b28-126">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="53b28-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="53b28-127">Note</span><span class="sxs-lookup"><span data-stu-id="53b28-127">NOTES</span></span>

## <span data-ttu-id="53b28-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53b28-128">RELATED LINKS</span></span>
[<span data-ttu-id="53b28-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="53b28-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="53b28-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="53b28-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="53b28-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="53b28-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)
