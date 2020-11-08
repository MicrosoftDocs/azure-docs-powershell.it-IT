---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: 7fde60c0bd1f400dd332782b6fbb9a92fefae4a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019281"
---
# <span data-ttu-id="6371a-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="6371a-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="6371a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6371a-102">SYNOPSIS</span></span>
<span data-ttu-id="6371a-103">Riavviare un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="6371a-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="6371a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6371a-104">SYNTAX</span></span>

### <span data-ttu-id="6371a-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6371a-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6371a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6371a-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6371a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6371a-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6371a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6371a-108">DESCRIPTION</span></span>
<span data-ttu-id="6371a-109">Riavviare un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="6371a-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="6371a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6371a-110">EXAMPLES</span></span>

### <span data-ttu-id="6371a-111">Riavviare un servizio segnalatore specifico</span><span class="sxs-lookup"><span data-stu-id="6371a-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="6371a-112">Il gruppo di risorse predefinito può essere impostato da \` set-AzDefault-ResourceGroupName myResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="6371a-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="6371a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6371a-113">PARAMETERS</span></span>

### <span data-ttu-id="6371a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6371a-114">-AsJob</span></span>
<span data-ttu-id="6371a-115">Eseguire il cmdlet in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="6371a-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="6371a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6371a-116">-DefaultProfile</span></span>
<span data-ttu-id="6371a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6371a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6371a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6371a-118">-InputObject</span></span>
<span data-ttu-id="6371a-119">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="6371a-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="6371a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6371a-120">-Name</span></span>
<span data-ttu-id="6371a-121">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="6371a-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="6371a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6371a-122">-PassThru</span></span>
<span data-ttu-id="6371a-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6371a-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="6371a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6371a-124">-ResourceGroupName</span></span>
<span data-ttu-id="6371a-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6371a-125">The resource group name.</span></span>
<span data-ttu-id="6371a-126">Verrà usato quello predefinito se non specificato.</span><span class="sxs-lookup"><span data-stu-id="6371a-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="6371a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6371a-127">-ResourceId</span></span>
<span data-ttu-id="6371a-128">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="6371a-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="6371a-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6371a-129">-Confirm</span></span>
<span data-ttu-id="6371a-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6371a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6371a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6371a-131">-WhatIf</span></span>
<span data-ttu-id="6371a-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6371a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6371a-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6371a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6371a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6371a-134">CommonParameters</span></span>
<span data-ttu-id="6371a-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6371a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6371a-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6371a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6371a-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6371a-137">INPUTS</span></span>

### <span data-ttu-id="6371a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6371a-138">System.String</span></span>

### <span data-ttu-id="6371a-139">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="6371a-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="6371a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6371a-140">OUTPUTS</span></span>

### <span data-ttu-id="6371a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6371a-141">System.Boolean</span></span>

## <span data-ttu-id="6371a-142">Note</span><span class="sxs-lookup"><span data-stu-id="6371a-142">NOTES</span></span>

## <span data-ttu-id="6371a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6371a-143">RELATED LINKS</span></span>
