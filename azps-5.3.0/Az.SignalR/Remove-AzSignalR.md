---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474930"
---
# <span data-ttu-id="294bf-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="294bf-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="294bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="294bf-102">SYNOPSIS</span></span>
<span data-ttu-id="294bf-103">Rimuovere un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="294bf-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="294bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="294bf-104">SYNTAX</span></span>

### <span data-ttu-id="294bf-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="294bf-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="294bf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="294bf-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="294bf-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="294bf-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="294bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="294bf-108">DESCRIPTION</span></span>
<span data-ttu-id="294bf-109">Rimuovere un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="294bf-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="294bf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="294bf-110">EXAMPLES</span></span>

### <span data-ttu-id="294bf-111">Rimuovere un servizio di segnalazione</span><span class="sxs-lookup"><span data-stu-id="294bf-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="294bf-112">Rimuovere tutti i servizi di segnalazione da pipe</span><span class="sxs-lookup"><span data-stu-id="294bf-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="294bf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="294bf-113">PARAMETERS</span></span>

### <span data-ttu-id="294bf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="294bf-114">-AsJob</span></span>
<span data-ttu-id="294bf-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="294bf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="294bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294bf-116">-DefaultProfile</span></span>
<span data-ttu-id="294bf-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="294bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="294bf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="294bf-118">-InputObject</span></span>
<span data-ttu-id="294bf-119">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="294bf-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="294bf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="294bf-120">-Name</span></span>
<span data-ttu-id="294bf-121">Nome del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="294bf-121">SignalR service name.</span></span>

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

### <span data-ttu-id="294bf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="294bf-122">-PassThru</span></span>
<span data-ttu-id="294bf-123">Restituisce vero se la rimozione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="294bf-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="294bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="294bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="294bf-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="294bf-125">Resource group name.</span></span>

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

### <span data-ttu-id="294bf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="294bf-126">-ResourceId</span></span>
<span data-ttu-id="294bf-127">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="294bf-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="294bf-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="294bf-128">-Confirm</span></span>
<span data-ttu-id="294bf-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="294bf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="294bf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="294bf-130">-WhatIf</span></span>
<span data-ttu-id="294bf-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="294bf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="294bf-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="294bf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="294bf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294bf-133">CommonParameters</span></span>
<span data-ttu-id="294bf-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="294bf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294bf-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="294bf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294bf-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="294bf-136">INPUTS</span></span>

### <span data-ttu-id="294bf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="294bf-137">System.String</span></span>
### <span data-ttu-id="294bf-138">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="294bf-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="294bf-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="294bf-139">OUTPUTS</span></span>

### <span data-ttu-id="294bf-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="294bf-140">System.Boolean</span></span>
## <span data-ttu-id="294bf-141">Note</span><span class="sxs-lookup"><span data-stu-id="294bf-141">NOTES</span></span>

## <span data-ttu-id="294bf-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="294bf-142">RELATED LINKS</span></span>
