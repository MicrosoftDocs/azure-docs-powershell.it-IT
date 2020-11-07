---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: fe1182f165e347b312288d56604fddad6bad68da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677973"
---
# <span data-ttu-id="9b3df-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b3df-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="9b3df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b3df-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3df-103">Modifica un ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="9b3df-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="9b3df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b3df-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b3df-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b3df-105">DESCRIPTION</span></span>
<span data-ttu-id="9b3df-106">Il cmdlet **set-AzExpressRoutePort** Salva il ExpressRoutePort modificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="9b3df-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="9b3df-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b3df-107">EXAMPLES</span></span>

### <span data-ttu-id="9b3df-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b3df-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="9b3df-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9b3df-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="9b3df-110">Modifica lo stato di amministratore di un collegamento di un ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b3df-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="9b3df-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b3df-111">PARAMETERS</span></span>

### <span data-ttu-id="9b3df-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b3df-112">-AsJob</span></span>
<span data-ttu-id="9b3df-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9b3df-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b3df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3df-114">-DefaultProfile</span></span>
<span data-ttu-id="9b3df-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b3df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b3df-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b3df-116">-ExpressRoutePort</span></span>
<span data-ttu-id="9b3df-117">Oggetto ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="9b3df-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="9b3df-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b3df-118">-Confirm</span></span>
<span data-ttu-id="9b3df-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b3df-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b3df-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b3df-120">-WhatIf</span></span>
<span data-ttu-id="9b3df-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b3df-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b3df-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b3df-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b3df-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3df-123">CommonParameters</span></span>
<span data-ttu-id="9b3df-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b3df-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3df-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b3df-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3df-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b3df-126">INPUTS</span></span>

### <span data-ttu-id="9b3df-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b3df-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="9b3df-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b3df-128">OUTPUTS</span></span>

### <span data-ttu-id="9b3df-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b3df-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="9b3df-130">Note</span><span class="sxs-lookup"><span data-stu-id="9b3df-130">NOTES</span></span>

## <span data-ttu-id="9b3df-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b3df-131">RELATED LINKS</span></span>

[<span data-ttu-id="9b3df-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b3df-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="9b3df-133">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b3df-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="9b3df-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b3df-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)
