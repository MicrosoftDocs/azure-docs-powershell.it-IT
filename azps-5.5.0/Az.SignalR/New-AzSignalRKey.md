---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197799"
---
# <span data-ttu-id="7c5bb-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="7c5bb-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="7c5bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c5bb-102">SYNOPSIS</span></span>
<span data-ttu-id="7c5bb-103">Rigenerare una chiave di accesso per un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="7c5bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c5bb-104">SYNTAX</span></span>

### <span data-ttu-id="7c5bb-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c5bb-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c5bb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c5bb-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c5bb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c5bb-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c5bb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7c5bb-108">DESCRIPTION</span></span>
<span data-ttu-id="7c5bb-109">Rigenerare una chiave di accesso per un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="7c5bb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c5bb-110">EXAMPLES</span></span>

### <span data-ttu-id="7c5bb-111">Rigenerare la chiave primaria</span><span class="sxs-lookup"><span data-stu-id="7c5bb-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="7c5bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c5bb-112">PARAMETERS</span></span>

### <span data-ttu-id="7c5bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c5bb-113">-DefaultProfile</span></span>
<span data-ttu-id="7c5bb-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c5bb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c5bb-115">-InputObject</span></span>
<span data-ttu-id="7c5bb-116">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="7c5bb-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="7c5bb-117">-KeyType</span></span>
<span data-ttu-id="7c5bb-118">Tipo di chiave, Principale o Secondario.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c5bb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7c5bb-119">-Name</span></span>
<span data-ttu-id="7c5bb-120">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-120">SignalR service name.</span></span>

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

### <span data-ttu-id="7c5bb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c5bb-121">-PassThru</span></span>
<span data-ttu-id="7c5bb-122">Restituisce true se la rigenerazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="7c5bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c5bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c5bb-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-124">Resource group name.</span></span>

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

### <span data-ttu-id="7c5bb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c5bb-125">-ResourceId</span></span>
<span data-ttu-id="7c5bb-126">ID risorsa servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="7c5bb-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c5bb-127">-Confirm</span></span>
<span data-ttu-id="7c5bb-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c5bb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c5bb-129">-WhatIf</span></span>
<span data-ttu-id="7c5bb-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c5bb-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c5bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c5bb-132">CommonParameters</span></span>
<span data-ttu-id="7c5bb-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c5bb-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7c5bb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c5bb-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="7c5bb-135">INPUTS</span></span>

### <span data-ttu-id="7c5bb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7c5bb-136">System.String</span></span>
### <span data-ttu-id="7c5bb-137">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="7c5bb-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="7c5bb-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c5bb-138">OUTPUTS</span></span>

### <span data-ttu-id="7c5bb-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c5bb-139">System.Boolean</span></span>
## <span data-ttu-id="7c5bb-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="7c5bb-140">NOTES</span></span>

## <span data-ttu-id="7c5bb-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c5bb-141">RELATED LINKS</span></span>
