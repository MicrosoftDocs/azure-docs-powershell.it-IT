---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182582"
---
# <span data-ttu-id="2ca0c-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ca0c-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="2ca0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ca0c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca0c-103">Rimuove un endpoint da Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="2ca0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ca0c-104">SYNTAX</span></span>

### <span data-ttu-id="2ca0c-105">Campi</span><span class="sxs-lookup"><span data-stu-id="2ca0c-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca0c-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="2ca0c-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca0c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2ca0c-107">DESCRIPTION</span></span>
<span data-ttu-id="2ca0c-108">Il cmdlet **Remove-AzTrafficManagerEndpoint** rimuove un endpoint da Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="2ca0c-109">Questo cmdlet esegue il commit di ogni modifica nel servizio Di gestione del traffico.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="2ca0c-110">Per rimuovere più endpoint da un oggetto profilo di Gestione traffico locale ed eseguire il commit delle modifiche in una singola operazione, usare il cmdlet Remove-AzTrafficManagerEndpointConfig locale.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="2ca0c-111">È possibile usare l'operatore della pipeline per passare un oggetto **TrafficManagerEndpoint** a questo cmdlet oppure è possibile specificare un **oggetto TrafficManagerEndpoint** usando il *parametro TrafficManagerEndpoint.*</span><span class="sxs-lookup"><span data-stu-id="2ca0c-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="2ca0c-112">In alternativa, è possibile specificare il nome e il tipo dell'endpoint usando i parametri *Name* e *Type,* insieme ai parametri *ProfileName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="2ca0c-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="2ca0c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ca0c-113">EXAMPLES</span></span>

### <span data-ttu-id="2ca0c-114">Esempio 1: Rimuovere un endpoint da un profilo</span><span class="sxs-lookup"><span data-stu-id="2ca0c-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="2ca0c-115">Questo comando rimuove l'endpoint di Azure denominato contoso dal profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2ca0c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ca0c-116">PARAMETERS</span></span>

### <span data-ttu-id="2ca0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca0c-117">-DefaultProfile</span></span>
<span data-ttu-id="2ca0c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ca0c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2ca0c-119">-Force</span></span>
<span data-ttu-id="2ca0c-120">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2ca0c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2ca0c-121">-Name</span></span>
<span data-ttu-id="2ca0c-122">Specifica il nome dell'endpoint di Gestione traffico rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca0c-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2ca0c-123">-ProfileName</span></span>
<span data-ttu-id="2ca0c-124">Specifica il nome di un profilo di Gestione traffico da cui questo cmdlet rimuove un endpoint.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="2ca0c-125">Per ottenere un profilo, usare il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca0c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca0c-126">-ResourceGroupName</span></span>
<span data-ttu-id="2ca0c-127">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2ca0c-128">Questo cmdlet rimuove un endpoint di Gestione traffico da un profilo di Gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca0c-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ca0c-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="2ca0c-130">Specifica l'endpoint di Gestione traffico rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="2ca0c-131">Per ottenere un **oggetto TrafficManagerEndpoint,** usare il cmdlet Get-AzTrafficManagerEndpoint TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca0c-132">-Type</span><span class="sxs-lookup"><span data-stu-id="2ca0c-132">-Type</span></span>
<span data-ttu-id="2ca0c-133">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="2ca0c-134">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="2ca0c-134">Valid values are:</span></span> 

- <span data-ttu-id="2ca0c-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="2ca0c-135">AzureEndpoints</span></span>
- <span data-ttu-id="2ca0c-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="2ca0c-136">ExternalEndpoints</span></span>
- <span data-ttu-id="2ca0c-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="2ca0c-137">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca0c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ca0c-138">-Confirm</span></span>
<span data-ttu-id="2ca0c-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca0c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca0c-140">-WhatIf</span></span>
<span data-ttu-id="2ca0c-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ca0c-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca0c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca0c-143">CommonParameters</span></span>
<span data-ttu-id="2ca0c-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ca0c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca0c-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca0c-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca0c-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="2ca0c-146">INPUTS</span></span>

### <span data-ttu-id="2ca0c-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ca0c-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="2ca0c-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ca0c-148">OUTPUTS</span></span>

### <span data-ttu-id="2ca0c-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ca0c-149">System.Boolean</span></span>

## <span data-ttu-id="2ca0c-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="2ca0c-150">NOTES</span></span>

## <span data-ttu-id="2ca0c-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ca0c-151">RELATED LINKS</span></span>

[<span data-ttu-id="2ca0c-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ca0c-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2ca0c-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ca0c-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="2ca0c-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ca0c-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2ca0c-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2ca0c-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="2ca0c-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2ca0c-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


