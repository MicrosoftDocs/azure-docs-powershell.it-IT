---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207995"
---
# <span data-ttu-id="14eb0-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="14eb0-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="14eb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="14eb0-103">Configura le impostazioni upstream di un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="14eb0-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="14eb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14eb0-104">SYNTAX</span></span>

### <span data-ttu-id="14eb0-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14eb0-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14eb0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14eb0-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14eb0-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14eb0-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14eb0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14eb0-108">DESCRIPTION</span></span>
<span data-ttu-id="14eb0-109">Configura le impostazioni upstream di un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="14eb0-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="14eb0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14eb0-110">EXAMPLES</span></span>

### <span data-ttu-id="14eb0-111">Impostare due modelli upstream ordinati</span><span class="sxs-lookup"><span data-stu-id="14eb0-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="14eb0-112">Il JSON seguente rappresenta il set di modelli effettivo.</span><span class="sxs-lookup"><span data-stu-id="14eb0-112">The following JSON represents the actual templates set.</span></span> 

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

### <span data-ttu-id="14eb0-113">Cancellare tutte le impostazioni di upstream</span><span class="sxs-lookup"><span data-stu-id="14eb0-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="14eb0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14eb0-114">PARAMETERS</span></span>

### <span data-ttu-id="14eb0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14eb0-115">-AsJob</span></span>
<span data-ttu-id="14eb0-116">Eseguire il cmdlet in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="14eb0-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="14eb0-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="14eb0-117">-Clear</span></span>
<span data-ttu-id="14eb0-118">Cancellare tutte le impostazioni di upstream.</span><span class="sxs-lookup"><span data-stu-id="14eb0-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="14eb0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14eb0-119">-DefaultProfile</span></span>
<span data-ttu-id="14eb0-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14eb0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14eb0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14eb0-121">-InputObject</span></span>
<span data-ttu-id="14eb0-122">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="14eb0-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="14eb0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="14eb0-123">-Name</span></span>
<span data-ttu-id="14eb0-124">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="14eb0-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="14eb0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14eb0-125">-ResourceGroupName</span></span>
<span data-ttu-id="14eb0-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14eb0-126">The resource group name.</span></span>
<span data-ttu-id="14eb0-127">Se non è specificato, verrà usato quello predefinito.</span><span class="sxs-lookup"><span data-stu-id="14eb0-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="14eb0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14eb0-128">-ResourceId</span></span>
<span data-ttu-id="14eb0-129">ID risorsa servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="14eb0-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="14eb0-130">-Template</span><span class="sxs-lookup"><span data-stu-id="14eb0-130">-Template</span></span>
<span data-ttu-id="14eb0-131">Elementi del modello per le impostazioni upstream.</span><span class="sxs-lookup"><span data-stu-id="14eb0-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="14eb0-132">Chiave obbligatoria: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="14eb0-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="14eb0-133">Chiavi facoltative: HubOrdinamento, EventOrdinamento, CategoryOrdinamento.</span><span class="sxs-lookup"><span data-stu-id="14eb0-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="14eb0-134">Esempio di utilizzo della sintassi della splatting per passare il parametro templates: @{UrlTemplate=' http://host-connections1.com ', Hub Sistema= 'chat'; EventTemplate='broadcast' },@{UrlTemplate=' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="14eb0-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

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

### <span data-ttu-id="14eb0-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14eb0-135">-Confirm</span></span>
<span data-ttu-id="14eb0-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14eb0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14eb0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14eb0-137">-WhatIf</span></span>
<span data-ttu-id="14eb0-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14eb0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14eb0-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14eb0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14eb0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14eb0-140">CommonParameters</span></span>
<span data-ttu-id="14eb0-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14eb0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14eb0-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14eb0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14eb0-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="14eb0-143">INPUTS</span></span>

### <span data-ttu-id="14eb0-144">System.String</span><span class="sxs-lookup"><span data-stu-id="14eb0-144">System.String</span></span>

## <span data-ttu-id="14eb0-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14eb0-145">OUTPUTS</span></span>

### <span data-ttu-id="14eb0-146">Microsoft.Azure.Commands.Signalr.Models.PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="14eb0-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="14eb0-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="14eb0-147">NOTES</span></span>

## <span data-ttu-id="14eb0-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14eb0-148">RELATED LINKS</span></span>

[<span data-ttu-id="14eb0-149">Come usare la splatting per passare parametri ai comandi in PowerShell</span><span class="sxs-lookup"><span data-stu-id="14eb0-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
