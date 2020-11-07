---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 196cdd5f41a33fe0e4185c4f30a35ce9444139de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676367"
---
# <span data-ttu-id="74880-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="74880-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="74880-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74880-102">SYNOPSIS</span></span>
<span data-ttu-id="74880-103">Disabilita un endpoint in un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="74880-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="74880-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74880-104">SYNTAX</span></span>

### <span data-ttu-id="74880-105">Campi</span><span class="sxs-lookup"><span data-stu-id="74880-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74880-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="74880-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74880-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74880-107">DESCRIPTION</span></span>
<span data-ttu-id="74880-108">Il cmdlet **Disable-AzTrafficManagerEndpoint Disabilita** un endpoint in un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="74880-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="74880-109">Puoi usare l'operatore pipeline per passare un oggetto **TrafficManagerEndpoint** a questo cmdlet oppure puoi passare un oggetto **TrafficManagerEndpoint** usando il parametro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="74880-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="74880-110">In alternativa, puoi specificare il nome e il tipo di endpoint usando i parametri *Name* e *Type* , insieme ai parametri *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="74880-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="74880-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74880-111">EXAMPLES</span></span>

### <span data-ttu-id="74880-112">Esempio 1: disabilitare un endpoint per nome</span><span class="sxs-lookup"><span data-stu-id="74880-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="74880-113">Questo comando Disabilita l'endpoint esterno denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="74880-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="74880-114">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="74880-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="74880-115">Esempio 2: disabilitare un endpoint usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="74880-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="74880-116">Questo comando ottiene l'endpoint esterno denominato Contoso dal profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="74880-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="74880-117">Il comando passa quindi tale endpoint al cmdlet **Disable-AzTrafficManagerEndpoint** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="74880-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="74880-118">Questo cmdlet disabilita tale endpoint.</span><span class="sxs-lookup"><span data-stu-id="74880-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="74880-119">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="74880-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="74880-120">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="74880-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="74880-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74880-121">PARAMETERS</span></span>

### <span data-ttu-id="74880-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74880-122">-DefaultProfile</span></span>
<span data-ttu-id="74880-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74880-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74880-124">-Force</span><span class="sxs-lookup"><span data-stu-id="74880-124">-Force</span></span>
<span data-ttu-id="74880-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="74880-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="74880-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="74880-126">-Name</span></span>
<span data-ttu-id="74880-127">Specifica il nome dell'endpoint di gestione traffico che questo cmdlet disabilita.</span><span class="sxs-lookup"><span data-stu-id="74880-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="74880-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="74880-128">-ProfileName</span></span>
<span data-ttu-id="74880-129">Specifica il nome di un profilo di Traffic Manager in cui questo cmdlet disabilita un endpoint.</span><span class="sxs-lookup"><span data-stu-id="74880-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="74880-130">Per ottenere un profilo, usare il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="74880-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="74880-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74880-131">-ResourceGroupName</span></span>
<span data-ttu-id="74880-132">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="74880-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="74880-133">Questo cmdlet disabilita un endpoint di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="74880-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="74880-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="74880-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="74880-135">Specifica l'endpoint di gestione traffico che questo cmdlet disabilita.</span><span class="sxs-lookup"><span data-stu-id="74880-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="74880-136">Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="74880-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="74880-137">-Digitare</span><span class="sxs-lookup"><span data-stu-id="74880-137">-Type</span></span>
<span data-ttu-id="74880-138">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="74880-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="74880-139">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="74880-139">Valid values are:</span></span> 

- <span data-ttu-id="74880-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="74880-140">AzureEndpoints</span></span>
- <span data-ttu-id="74880-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="74880-141">ExternalEndpoints</span></span>
- <span data-ttu-id="74880-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="74880-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="74880-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="74880-143">-Confirm</span></span>
<span data-ttu-id="74880-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74880-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74880-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74880-145">-WhatIf</span></span>
<span data-ttu-id="74880-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74880-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74880-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74880-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74880-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74880-148">CommonParameters</span></span>
<span data-ttu-id="74880-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74880-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74880-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74880-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74880-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74880-151">INPUTS</span></span>

### <span data-ttu-id="74880-152">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="74880-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="74880-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74880-153">OUTPUTS</span></span>

### <span data-ttu-id="74880-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="74880-154">System.Boolean</span></span>

## <span data-ttu-id="74880-155">Note</span><span class="sxs-lookup"><span data-stu-id="74880-155">NOTES</span></span>

## <span data-ttu-id="74880-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74880-156">RELATED LINKS</span></span>

[<span data-ttu-id="74880-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="74880-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="74880-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="74880-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="74880-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="74880-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="74880-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="74880-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="74880-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="74880-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="74880-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="74880-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="74880-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="74880-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

