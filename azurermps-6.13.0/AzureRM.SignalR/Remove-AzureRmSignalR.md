---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
ms.openlocfilehash: 5fcf62e592ed1e842c3dc6f4be21462170c4f83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516431"
---
# <span data-ttu-id="3db87-101">Remove-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="3db87-101">Remove-AzureRmSignalR</span></span>

## <span data-ttu-id="3db87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3db87-102">SYNOPSIS</span></span>
<span data-ttu-id="3db87-103">Rimuovere un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="3db87-103">Remove a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3db87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3db87-104">SYNTAX</span></span>

### <span data-ttu-id="3db87-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3db87-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db87-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3db87-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3db87-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3db87-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3db87-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3db87-108">DESCRIPTION</span></span>
<span data-ttu-id="3db87-109">Rimuovere un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="3db87-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="3db87-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3db87-110">EXAMPLES</span></span>

### <span data-ttu-id="3db87-111">Rimuovere un servizio di segnalazione</span><span class="sxs-lookup"><span data-stu-id="3db87-111">Remove a SignalR service</span></span>
```powershell
PS C:\> Remove-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="3db87-112">Rimuovere tutti i servizi di segnalazione da pipe</span><span class="sxs-lookup"><span data-stu-id="3db87-112">Remove all SignalR service from pipe</span></span>
```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup | Remove-AzureRmSignalR
```

## <span data-ttu-id="3db87-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3db87-113">PARAMETERS</span></span>

### <span data-ttu-id="3db87-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3db87-114">-AsJob</span></span>
<span data-ttu-id="3db87-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3db87-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3db87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db87-116">-DefaultProfile</span></span>
<span data-ttu-id="3db87-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3db87-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3db87-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3db87-118">-InputObject</span></span>
<span data-ttu-id="3db87-119">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="3db87-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="3db87-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3db87-120">-Name</span></span>
<span data-ttu-id="3db87-121">Nome del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="3db87-121">SignalR service name.</span></span>

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

### <span data-ttu-id="3db87-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3db87-122">-PassThru</span></span>
<span data-ttu-id="3db87-123">Restituisce vero se la rimozione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="3db87-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="3db87-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3db87-124">-ResourceGroupName</span></span>
<span data-ttu-id="3db87-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3db87-125">Resource group name.</span></span>

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

### <span data-ttu-id="3db87-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3db87-126">-ResourceId</span></span>
<span data-ttu-id="3db87-127">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="3db87-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="3db87-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3db87-128">-Confirm</span></span>
<span data-ttu-id="3db87-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db87-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3db87-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db87-130">-WhatIf</span></span>
<span data-ttu-id="3db87-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3db87-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3db87-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3db87-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3db87-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db87-133">CommonParameters</span></span>
<span data-ttu-id="3db87-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db87-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db87-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3db87-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db87-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3db87-136">INPUTS</span></span>

### <span data-ttu-id="3db87-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3db87-137">System.String</span></span>
<span data-ttu-id="3db87-138">Parametri: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3db87-138">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="3db87-139">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="3db87-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="3db87-140">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3db87-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3db87-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3db87-141">OUTPUTS</span></span>

### <span data-ttu-id="3db87-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3db87-142">System.Boolean</span></span>

## <span data-ttu-id="3db87-143">Note</span><span class="sxs-lookup"><span data-stu-id="3db87-143">NOTES</span></span>

## <span data-ttu-id="3db87-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3db87-144">RELATED LINKS</span></span>
