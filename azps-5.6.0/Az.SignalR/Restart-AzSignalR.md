---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: c98b716f37fcf9aafafacdefad4c51b0451cf12d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955454"
---
# <span data-ttu-id="48196-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="48196-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="48196-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48196-102">SYNOPSIS</span></span>
<span data-ttu-id="48196-103">Riavvia un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="48196-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="48196-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48196-104">SYNTAX</span></span>

### <span data-ttu-id="48196-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48196-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48196-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48196-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48196-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48196-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48196-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="48196-108">DESCRIPTION</span></span>
<span data-ttu-id="48196-109">Riavvia un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="48196-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="48196-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48196-110">EXAMPLES</span></span>

### <span data-ttu-id="48196-111">Riavvia un servizio SignalR specifico</span><span class="sxs-lookup"><span data-stu-id="48196-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="48196-112">Il gruppo di risorse predefinito può essere \` impostato da Set-AzDefault -ResourceGroupName \` myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="48196-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="48196-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48196-113">PARAMETERS</span></span>

### <span data-ttu-id="48196-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48196-114">-AsJob</span></span>
<span data-ttu-id="48196-115">Eseguire il cmdlet nel processo in background.</span><span class="sxs-lookup"><span data-stu-id="48196-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="48196-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48196-116">-DefaultProfile</span></span>
<span data-ttu-id="48196-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48196-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48196-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48196-118">-InputObject</span></span>
<span data-ttu-id="48196-119">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="48196-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="48196-120">-Name</span><span class="sxs-lookup"><span data-stu-id="48196-120">-Name</span></span>
<span data-ttu-id="48196-121">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="48196-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="48196-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48196-122">-PassThru</span></span>
<span data-ttu-id="48196-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="48196-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="48196-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48196-124">-ResourceGroupName</span></span>
<span data-ttu-id="48196-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="48196-125">The resource group name.</span></span>
<span data-ttu-id="48196-126">Se non viene specificato, verrà usato quello predefinito.</span><span class="sxs-lookup"><span data-stu-id="48196-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="48196-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48196-127">-ResourceId</span></span>
<span data-ttu-id="48196-128">ID risorsa servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="48196-128">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48196-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48196-129">-Confirm</span></span>
<span data-ttu-id="48196-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48196-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48196-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48196-131">-WhatIf</span></span>
<span data-ttu-id="48196-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48196-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48196-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48196-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48196-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48196-134">CommonParameters</span></span>
<span data-ttu-id="48196-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48196-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48196-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48196-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48196-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="48196-137">INPUTS</span></span>

### <span data-ttu-id="48196-138">System.String</span><span class="sxs-lookup"><span data-stu-id="48196-138">System.String</span></span>

### <span data-ttu-id="48196-139">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="48196-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="48196-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48196-140">OUTPUTS</span></span>

### <span data-ttu-id="48196-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48196-141">System.Boolean</span></span>

## <span data-ttu-id="48196-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="48196-142">NOTES</span></span>

## <span data-ttu-id="48196-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48196-143">RELATED LINKS</span></span>
