---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: c431b03c4dd417638f84fe3a483bcaf9eefcb837
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963981"
---
# <span data-ttu-id="35a79-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a79-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="35a79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35a79-102">SYNOPSIS</span></span>
<span data-ttu-id="35a79-103">Modifica un valore ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="35a79-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="35a79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35a79-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35a79-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35a79-105">DESCRIPTION</span></span>
<span data-ttu-id="35a79-106">Il cmdlet **Set-AzExpressRoutePort** salva l'istanza di ExpressRoutePort modificata in Azure.</span><span class="sxs-lookup"><span data-stu-id="35a79-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="35a79-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35a79-107">EXAMPLES</span></span>

### <span data-ttu-id="35a79-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35a79-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="35a79-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="35a79-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="35a79-110">Modifica lo stato di amministratore di un collegamento di ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a79-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="35a79-111">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="35a79-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="35a79-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35a79-112">PARAMETERS</span></span>

### <span data-ttu-id="35a79-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35a79-113">-AsJob</span></span>
<span data-ttu-id="35a79-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="35a79-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35a79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a79-115">-DefaultProfile</span></span>
<span data-ttu-id="35a79-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35a79-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35a79-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a79-117">-ExpressRoutePort</span></span>
<span data-ttu-id="35a79-118">Oggetto ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="35a79-118">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35a79-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35a79-119">-Confirm</span></span>
<span data-ttu-id="35a79-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35a79-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35a79-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35a79-121">-WhatIf</span></span>
<span data-ttu-id="35a79-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35a79-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35a79-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35a79-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35a79-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a79-124">CommonParameters</span></span>
<span data-ttu-id="35a79-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a79-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a79-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a79-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a79-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="35a79-127">INPUTS</span></span>

### <span data-ttu-id="35a79-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a79-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="35a79-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35a79-129">OUTPUTS</span></span>

### <span data-ttu-id="35a79-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a79-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="35a79-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="35a79-131">NOTES</span></span>

## <span data-ttu-id="35a79-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35a79-132">RELATED LINKS</span></span>

[<span data-ttu-id="35a79-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a79-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="35a79-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a79-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="35a79-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="35a79-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
