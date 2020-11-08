---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019245"
---
# <span data-ttu-id="3eff9-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="3eff9-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="3eff9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3eff9-102">SYNOPSIS</span></span>
<span data-ttu-id="3eff9-103">Rigenerare un tasto di accesso per un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="3eff9-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="3eff9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3eff9-104">SYNTAX</span></span>

### <span data-ttu-id="3eff9-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3eff9-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eff9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eff9-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eff9-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3eff9-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eff9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3eff9-108">DESCRIPTION</span></span>
<span data-ttu-id="3eff9-109">Rigenerare un tasto di accesso per un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="3eff9-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="3eff9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3eff9-110">EXAMPLES</span></span>

### <span data-ttu-id="3eff9-111">Rigenerare la chiave primaria</span><span class="sxs-lookup"><span data-stu-id="3eff9-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="3eff9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3eff9-112">PARAMETERS</span></span>

### <span data-ttu-id="3eff9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eff9-113">-DefaultProfile</span></span>
<span data-ttu-id="3eff9-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3eff9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eff9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eff9-115">-InputObject</span></span>
<span data-ttu-id="3eff9-116">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="3eff9-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="3eff9-117">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="3eff9-117">-KeyType</span></span>
<span data-ttu-id="3eff9-118">Il tipo di chiave, primario o secondario.</span><span class="sxs-lookup"><span data-stu-id="3eff9-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="3eff9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="3eff9-119">-Name</span></span>
<span data-ttu-id="3eff9-120">Nome del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="3eff9-120">SignalR service name.</span></span>

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

### <span data-ttu-id="3eff9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3eff9-121">-PassThru</span></span>
<span data-ttu-id="3eff9-122">Restituisce vero se la rigenerazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="3eff9-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="3eff9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eff9-123">-ResourceGroupName</span></span>
<span data-ttu-id="3eff9-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3eff9-124">Resource group name.</span></span>

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

### <span data-ttu-id="3eff9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3eff9-125">-ResourceId</span></span>
<span data-ttu-id="3eff9-126">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="3eff9-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="3eff9-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3eff9-127">-Confirm</span></span>
<span data-ttu-id="3eff9-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eff9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eff9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eff9-129">-WhatIf</span></span>
<span data-ttu-id="3eff9-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3eff9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eff9-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3eff9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eff9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eff9-132">CommonParameters</span></span>
<span data-ttu-id="3eff9-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eff9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eff9-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3eff9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eff9-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3eff9-135">INPUTS</span></span>

### <span data-ttu-id="3eff9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3eff9-136">System.String</span></span>
### <span data-ttu-id="3eff9-137">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="3eff9-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="3eff9-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3eff9-138">OUTPUTS</span></span>

### <span data-ttu-id="3eff9-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3eff9-139">System.Boolean</span></span>
## <span data-ttu-id="3eff9-140">Note</span><span class="sxs-lookup"><span data-stu-id="3eff9-140">NOTES</span></span>

## <span data-ttu-id="3eff9-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3eff9-141">RELATED LINKS</span></span>
