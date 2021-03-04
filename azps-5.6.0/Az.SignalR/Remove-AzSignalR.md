---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 067dd93f28a5019de96f146a237fe131a9717bfc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955469"
---
# <span data-ttu-id="86461-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="86461-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="86461-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86461-102">SYNOPSIS</span></span>
<span data-ttu-id="86461-103">Rimuovi un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="86461-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="86461-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86461-104">SYNTAX</span></span>

### <span data-ttu-id="86461-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86461-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86461-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86461-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86461-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86461-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86461-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="86461-108">DESCRIPTION</span></span>
<span data-ttu-id="86461-109">Rimuovi un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="86461-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="86461-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86461-110">EXAMPLES</span></span>

### <span data-ttu-id="86461-111">Rimuovi un servizio SignalR</span><span class="sxs-lookup"><span data-stu-id="86461-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="86461-112">Rimuovi tutto il servizio SignalR dalla pipe</span><span class="sxs-lookup"><span data-stu-id="86461-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="86461-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86461-113">PARAMETERS</span></span>

### <span data-ttu-id="86461-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86461-114">-AsJob</span></span>
<span data-ttu-id="86461-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="86461-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86461-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86461-116">-DefaultProfile</span></span>
<span data-ttu-id="86461-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86461-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86461-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86461-118">-InputObject</span></span>
<span data-ttu-id="86461-119">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="86461-119">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86461-120">-Name</span><span class="sxs-lookup"><span data-stu-id="86461-120">-Name</span></span>
<span data-ttu-id="86461-121">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="86461-121">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86461-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86461-122">-PassThru</span></span>
<span data-ttu-id="86461-123">Restituisce true se la rimozione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="86461-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86461-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86461-124">-ResourceGroupName</span></span>
<span data-ttu-id="86461-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="86461-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86461-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86461-126">-ResourceId</span></span>
<span data-ttu-id="86461-127">ID risorsa servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="86461-127">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86461-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86461-128">-Confirm</span></span>
<span data-ttu-id="86461-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86461-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86461-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86461-130">-WhatIf</span></span>
<span data-ttu-id="86461-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86461-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86461-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86461-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86461-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86461-133">CommonParameters</span></span>
<span data-ttu-id="86461-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86461-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86461-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="86461-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86461-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="86461-136">INPUTS</span></span>

### <span data-ttu-id="86461-137">System.String</span><span class="sxs-lookup"><span data-stu-id="86461-137">System.String</span></span>
### <span data-ttu-id="86461-138">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="86461-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="86461-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86461-139">OUTPUTS</span></span>

### <span data-ttu-id="86461-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="86461-140">System.Boolean</span></span>
## <span data-ttu-id="86461-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="86461-141">NOTES</span></span>

## <span data-ttu-id="86461-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86461-142">RELATED LINKS</span></span>
