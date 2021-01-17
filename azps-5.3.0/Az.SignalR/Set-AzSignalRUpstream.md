---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474928"
---
# <span data-ttu-id="ed524-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="ed524-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="ed524-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed524-102">SYNOPSIS</span></span>
<span data-ttu-id="ed524-103">Impostare le impostazioni upstream di un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="ed524-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="ed524-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed524-104">SYNTAX</span></span>

### <span data-ttu-id="ed524-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed524-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed524-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed524-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed524-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed524-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed524-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed524-108">DESCRIPTION</span></span>
<span data-ttu-id="ed524-109">Impostare le impostazioni upstream di un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="ed524-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="ed524-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed524-110">EXAMPLES</span></span>

### <span data-ttu-id="ed524-111">Impostare due modelli a Monte ordinati</span><span class="sxs-lookup"><span data-stu-id="ed524-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="ed524-112">Il JSON seguente rappresenta il set di modelli effettivi.</span><span class="sxs-lookup"><span data-stu-id="ed524-112">The following JSON represents the actual templates set.</span></span> 

 `
{
    "hubPattern": "chat",
    "eventPattern": "broadcast",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections1.com"
},
{
    "hubPattern": "*",
    "eventPattern": "*",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections2.com"
}
`

### <span data-ttu-id="ed524-113">Deselezionare tutte le impostazioni upstream</span><span class="sxs-lookup"><span data-stu-id="ed524-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="ed524-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed524-114">PARAMETERS</span></span>

### <span data-ttu-id="ed524-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed524-115">-AsJob</span></span>
<span data-ttu-id="ed524-116">Eseguire il cmdlet in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="ed524-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="ed524-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="ed524-117">-Clear</span></span>
<span data-ttu-id="ed524-118">Deselezionare tutte le impostazioni upstream.</span><span class="sxs-lookup"><span data-stu-id="ed524-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="ed524-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed524-119">-DefaultProfile</span></span>
<span data-ttu-id="ed524-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed524-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed524-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed524-121">-InputObject</span></span>
<span data-ttu-id="ed524-122">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="ed524-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="ed524-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed524-123">-Name</span></span>
<span data-ttu-id="ed524-124">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="ed524-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="ed524-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed524-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed524-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ed524-126">The resource group name.</span></span>
<span data-ttu-id="ed524-127">Verrà usato quello predefinito se non specificato.</span><span class="sxs-lookup"><span data-stu-id="ed524-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="ed524-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed524-128">-ResourceId</span></span>
<span data-ttu-id="ed524-129">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="ed524-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="ed524-130">-Modello</span><span class="sxs-lookup"><span data-stu-id="ed524-130">-Template</span></span>
<span data-ttu-id="ed524-131">Elementi del modello per le impostazioni upstream.</span><span class="sxs-lookup"><span data-stu-id="ed524-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="ed524-132">Tasto obbligatorio: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="ed524-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="ed524-133">Tasti facoltativi: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="ed524-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="ed524-134">Esempio di utilizzo della sintassi splatting per passare il parametro Templates: @ {UrlTemplate =' http://host-connections1.com ', HubPattern =' chat '; EventPattern =' Broadcast '}, @ {UrlTemplate =' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="ed524-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed524-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed524-135">-Confirm</span></span>
<span data-ttu-id="ed524-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed524-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed524-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed524-137">-WhatIf</span></span>
<span data-ttu-id="ed524-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed524-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed524-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed524-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed524-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed524-140">CommonParameters</span></span>
<span data-ttu-id="ed524-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed524-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed524-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed524-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed524-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed524-143">INPUTS</span></span>

### <span data-ttu-id="ed524-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ed524-144">System.String</span></span>

## <span data-ttu-id="ed524-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed524-145">OUTPUTS</span></span>

### <span data-ttu-id="ed524-146">Microsoft. Azure. Commands. SignalR. Models. PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="ed524-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="ed524-147">Note</span><span class="sxs-lookup"><span data-stu-id="ed524-147">NOTES</span></span>

## <span data-ttu-id="ed524-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed524-148">RELATED LINKS</span></span>

[<span data-ttu-id="ed524-149">Come usare splatting per passare parametri ai comandi in PowerShell</span><span class="sxs-lookup"><span data-stu-id="ed524-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
