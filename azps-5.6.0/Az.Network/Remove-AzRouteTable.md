---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: df0c4f25491493254801006b443178ad1efdc537
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006158"
---
# <span data-ttu-id="8c4c8-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c4c8-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="8c4c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c4c8-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4c8-103">Rimuove una tabella di route.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-103">Removes a route table.</span></span>

## <span data-ttu-id="8c4c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c4c8-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c4c8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8c4c8-105">DESCRIPTION</span></span>
<span data-ttu-id="8c4c8-106">Il cmdlet **Remove-AzRouteTable** rimuove una tabella di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="8c4c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c4c8-107">EXAMPLES</span></span>

### <span data-ttu-id="8c4c8-108">Esempio 1: Rimuovere una tabella di route</span><span class="sxs-lookup"><span data-stu-id="8c4c8-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="8c4c8-109">Questo comando rimuove la tabella di route denominata RouteTable01 nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="8c4c8-110">Il cmdlet chiede conferma prima di rimuovere la tabella.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="8c4c8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c4c8-111">PARAMETERS</span></span>

### <span data-ttu-id="8c4c8-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c4c8-112">-AsJob</span></span>
<span data-ttu-id="8c4c8-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8c4c8-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c4c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c4c8-114">-DefaultProfile</span></span>
<span data-ttu-id="8c4c8-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c4c8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8c4c8-116">-Force</span></span>
<span data-ttu-id="8c4c8-117">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c4c8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8c4c8-118">-Name</span></span>
<span data-ttu-id="8c4c8-119">Specifica il nome della tabella di route rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-119">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c4c8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c4c8-120">-PassThru</span></span>
<span data-ttu-id="8c4c8-121">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c4c8-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c4c8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c4c8-123">-ResourceGroupName</span></span>
<span data-ttu-id="8c4c8-124">Specifica il nome del gruppo di risorse che contiene la tabella di route rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8c4c8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c4c8-125">-Confirm</span></span>
<span data-ttu-id="8c4c8-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4c8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c4c8-127">-WhatIf</span></span>
<span data-ttu-id="8c4c8-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c4c8-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c4c8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4c8-130">CommonParameters</span></span>
<span data-ttu-id="8c4c8-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4c8-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c4c8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4c8-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="8c4c8-133">INPUTS</span></span>

### <span data-ttu-id="8c4c8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8c4c8-134">System.String</span></span>

## <span data-ttu-id="8c4c8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c4c8-135">OUTPUTS</span></span>

### <span data-ttu-id="8c4c8-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8c4c8-136">System.Boolean</span></span>

## <span data-ttu-id="8c4c8-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="8c4c8-137">NOTES</span></span>

## <span data-ttu-id="8c4c8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c4c8-138">RELATED LINKS</span></span>

[<span data-ttu-id="8c4c8-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c4c8-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="8c4c8-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c4c8-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="8c4c8-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8c4c8-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


