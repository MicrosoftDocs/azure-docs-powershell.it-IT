---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: e14f74af1c8e50ddc5bc3281fca71b1e2d740e3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950798"
---
# <span data-ttu-id="8954e-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8954e-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="8954e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8954e-102">SYNOPSIS</span></span>
<span data-ttu-id="8954e-103">Disabilita un endpoint in un profilo di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="8954e-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="8954e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8954e-104">SYNTAX</span></span>

### <span data-ttu-id="8954e-105">Campi</span><span class="sxs-lookup"><span data-stu-id="8954e-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8954e-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="8954e-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8954e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8954e-107">DESCRIPTION</span></span>
<span data-ttu-id="8954e-108">Il cmdlet **Disable-AzTrafficManagerEndpoint** disabilita un endpoint in un profilo di Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="8954e-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="8954e-109">È possibile usare l'operatore della pipeline per passare un oggetto **TrafficManagerEndpoint** a questo cmdlet oppure passare un **oggetto TrafficManagerEndpoint** usando il *parametro TrafficManagerEndpoint.*</span><span class="sxs-lookup"><span data-stu-id="8954e-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="8954e-110">In alternativa, è possibile specificare il nome e il tipo dell'endpoint usando i parametri *Name* e *Type,* insieme ai parametri *ProfileName* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="8954e-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="8954e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8954e-111">EXAMPLES</span></span>

### <span data-ttu-id="8954e-112">Esempio 1: Disabilitare un endpoint in base al nome</span><span class="sxs-lookup"><span data-stu-id="8954e-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="8954e-113">Questo comando disabilita l'endpoint esterno denominato contoso nel profilo denominato ContosoProfile nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8954e-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="8954e-114">Il comando chiede di confermare.</span><span class="sxs-lookup"><span data-stu-id="8954e-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="8954e-115">Esempio 2: Disabilitare un endpoint usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="8954e-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="8954e-116">Questo comando recupera l'endpoint esterno denominato Contoso dal profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8954e-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="8954e-117">Il comando passa quindi l'endpoint al cmdlet **Disable-AzTrafficManagerEndpoint** usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8954e-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8954e-118">Questo cmdlet disabilita l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="8954e-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="8954e-119">Il comando specifica il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="8954e-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8954e-120">Di conseguenza, non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8954e-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8954e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8954e-121">PARAMETERS</span></span>

### <span data-ttu-id="8954e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8954e-122">-DefaultProfile</span></span>
<span data-ttu-id="8954e-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8954e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8954e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8954e-124">-Force</span></span>
<span data-ttu-id="8954e-125">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="8954e-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8954e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8954e-126">-Name</span></span>
<span data-ttu-id="8954e-127">Specifica il nome dell'endpoint di Gestione traffico che questo cmdlet disabilita.</span><span class="sxs-lookup"><span data-stu-id="8954e-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="8954e-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8954e-128">-ProfileName</span></span>
<span data-ttu-id="8954e-129">Specifica il nome di un profilo di Gestione traffico in cui questo cmdlet disabilita un endpoint.</span><span class="sxs-lookup"><span data-stu-id="8954e-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="8954e-130">Per ottenere un profilo, usare il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="8954e-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="8954e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8954e-131">-ResourceGroupName</span></span>
<span data-ttu-id="8954e-132">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8954e-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8954e-133">Questo cmdlet disabilita un endpoint di Gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8954e-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8954e-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8954e-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="8954e-135">Specifica l'endpoint di Gestione traffico disabilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8954e-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="8954e-136">Per ottenere un **oggetto TrafficManagerEndpoint,** usare il cmdlet Get-AzTrafficManagerEndpoint TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8954e-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="8954e-137">-Type</span><span class="sxs-lookup"><span data-stu-id="8954e-137">-Type</span></span>
<span data-ttu-id="8954e-138">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="8954e-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="8954e-139">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="8954e-139">Valid values are:</span></span> 

- <span data-ttu-id="8954e-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="8954e-140">AzureEndpoints</span></span>
- <span data-ttu-id="8954e-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="8954e-141">ExternalEndpoints</span></span>
- <span data-ttu-id="8954e-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="8954e-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="8954e-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8954e-143">-Confirm</span></span>
<span data-ttu-id="8954e-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8954e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8954e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8954e-145">-WhatIf</span></span>
<span data-ttu-id="8954e-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8954e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8954e-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8954e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8954e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8954e-148">CommonParameters</span></span>
<span data-ttu-id="8954e-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8954e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8954e-150">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8954e-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8954e-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="8954e-151">INPUTS</span></span>

### <span data-ttu-id="8954e-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8954e-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="8954e-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8954e-153">OUTPUTS</span></span>

### <span data-ttu-id="8954e-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8954e-154">System.Boolean</span></span>

## <span data-ttu-id="8954e-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="8954e-155">NOTES</span></span>

## <span data-ttu-id="8954e-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8954e-156">RELATED LINKS</span></span>

[<span data-ttu-id="8954e-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8954e-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8954e-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8954e-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8954e-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8954e-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="8954e-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8954e-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8954e-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8954e-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="8954e-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8954e-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8954e-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8954e-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


