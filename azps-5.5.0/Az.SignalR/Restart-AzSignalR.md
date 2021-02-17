---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: ea5de8ddd36d315381d4f60ee0fa1ce7dc49adc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208002"
---
# <span data-ttu-id="23e14-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="23e14-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="23e14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23e14-102">SYNOPSIS</span></span>
<span data-ttu-id="23e14-103">Riavvia un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="23e14-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="23e14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23e14-104">SYNTAX</span></span>

### <span data-ttu-id="23e14-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23e14-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23e14-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23e14-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23e14-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23e14-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23e14-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="23e14-108">DESCRIPTION</span></span>
<span data-ttu-id="23e14-109">Riavvia un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="23e14-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="23e14-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23e14-110">EXAMPLES</span></span>

### <span data-ttu-id="23e14-111">Riavvia un servizio SignalR specifico</span><span class="sxs-lookup"><span data-stu-id="23e14-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="23e14-112">Il gruppo di risorse predefinito può essere impostato \` da Set-AzDefault -ResourceGroupName \` myResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="23e14-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="23e14-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23e14-113">PARAMETERS</span></span>

### <span data-ttu-id="23e14-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23e14-114">-AsJob</span></span>
<span data-ttu-id="23e14-115">Eseguire il cmdlet in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="23e14-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="23e14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e14-116">-DefaultProfile</span></span>
<span data-ttu-id="23e14-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23e14-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23e14-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23e14-118">-InputObject</span></span>
<span data-ttu-id="23e14-119">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="23e14-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="23e14-120">-Name</span><span class="sxs-lookup"><span data-stu-id="23e14-120">-Name</span></span>
<span data-ttu-id="23e14-121">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="23e14-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="23e14-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23e14-122">-PassThru</span></span>
<span data-ttu-id="23e14-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="23e14-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="23e14-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e14-124">-ResourceGroupName</span></span>
<span data-ttu-id="23e14-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="23e14-125">The resource group name.</span></span>
<span data-ttu-id="23e14-126">Se non è specificato, verrà usato quello predefinito.</span><span class="sxs-lookup"><span data-stu-id="23e14-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="23e14-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23e14-127">-ResourceId</span></span>
<span data-ttu-id="23e14-128">ID risorsa servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="23e14-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="23e14-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23e14-129">-Confirm</span></span>
<span data-ttu-id="23e14-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23e14-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23e14-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e14-131">-WhatIf</span></span>
<span data-ttu-id="23e14-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23e14-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23e14-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23e14-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23e14-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e14-134">CommonParameters</span></span>
<span data-ttu-id="23e14-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e14-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e14-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="23e14-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e14-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="23e14-137">INPUTS</span></span>

### <span data-ttu-id="23e14-138">System.String</span><span class="sxs-lookup"><span data-stu-id="23e14-138">System.String</span></span>

### <span data-ttu-id="23e14-139">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="23e14-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="23e14-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23e14-140">OUTPUTS</span></span>

### <span data-ttu-id="23e14-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="23e14-141">System.Boolean</span></span>

## <span data-ttu-id="23e14-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="23e14-142">NOTES</span></span>

## <span data-ttu-id="23e14-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23e14-143">RELATED LINKS</span></span>
