---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRoutePort.md
ms.openlocfilehash: 46f73d2a58fe5f1109de6a15a5cb39e3b568a4b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519244"
---
# <span data-ttu-id="ce200-101">Set-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce200-101">Set-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="ce200-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce200-102">SYNOPSIS</span></span>
<span data-ttu-id="ce200-103">Modifica un ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ce200-103">Modifies an ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce200-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce200-104">SYNTAX</span></span>

```
Set-AzureRmExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce200-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce200-105">DESCRIPTION</span></span>
<span data-ttu-id="ce200-106">Il cmdlet **set-AzureRmExpressRoutePort** Salva il ExpressRoutePort modificato in Azure.</span><span class="sxs-lookup"><span data-stu-id="ce200-106">The **Set-AzureRmExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="ce200-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce200-107">EXAMPLES</span></span>

### <span data-ttu-id="ce200-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce200-108">Example 1</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="ce200-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ce200-109">Example 2</span></span>
```powershell
$erport = Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzureRmExpressRoutePort -InputObject $erport
```

<span data-ttu-id="ce200-110">Modifica lo stato di amministratore di un collegamento di un ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce200-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="ce200-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce200-111">PARAMETERS</span></span>

### <span data-ttu-id="ce200-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce200-112">-AsJob</span></span>
<span data-ttu-id="ce200-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ce200-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce200-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce200-114">-DefaultProfile</span></span>
<span data-ttu-id="ce200-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce200-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce200-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce200-116">-ExpressRoutePort</span></span>
<span data-ttu-id="ce200-117">Oggetto ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="ce200-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="ce200-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce200-118">-Confirm</span></span>
<span data-ttu-id="ce200-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce200-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce200-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce200-120">-WhatIf</span></span>
<span data-ttu-id="ce200-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce200-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce200-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce200-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce200-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce200-123">CommonParameters</span></span>
<span data-ttu-id="ce200-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce200-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce200-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce200-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce200-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce200-126">INPUTS</span></span>

### <span data-ttu-id="ce200-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce200-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ce200-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce200-128">OUTPUTS</span></span>

### <span data-ttu-id="ce200-129">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce200-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ce200-130">Note</span><span class="sxs-lookup"><span data-stu-id="ce200-130">NOTES</span></span>

## <span data-ttu-id="ce200-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce200-131">RELATED LINKS</span></span>
