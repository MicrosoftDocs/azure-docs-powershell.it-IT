---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 1481b577e248354eb2fdccbb9d6ecd450ab0cf62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522100"
---
# <span data-ttu-id="52814-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52814-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="52814-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52814-102">SYNOPSIS</span></span>
<span data-ttu-id="52814-103">Disabilita un endpoint in un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="52814-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52814-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52814-104">SYNTAX</span></span>

### <span data-ttu-id="52814-105">Campi</span><span class="sxs-lookup"><span data-stu-id="52814-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52814-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="52814-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52814-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52814-107">DESCRIPTION</span></span>
<span data-ttu-id="52814-108">Il cmdlet **Disable-AzureRmTrafficManagerEndpoint Disabilita** un endpoint in un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="52814-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="52814-109">Puoi usare l'operatore pipeline per passare un oggetto **TrafficManagerEndpoint** a questo cmdlet oppure puoi passare un oggetto **TrafficManagerEndpoint** usando il parametro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="52814-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="52814-110">In alternativa, puoi specificare il nome e il tipo di endpoint usando i parametri *Name* e *Type* , insieme ai parametri *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="52814-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="52814-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52814-111">EXAMPLES</span></span>

### <span data-ttu-id="52814-112">Esempio 1: disabilitare un endpoint per nome</span><span class="sxs-lookup"><span data-stu-id="52814-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="52814-113">Questo comando Disabilita l'endpoint esterno denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="52814-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="52814-114">Il comando richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="52814-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="52814-115">Esempio 2: disabilitare un endpoint usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="52814-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="52814-116">Questo comando ottiene l'endpoint esterno denominato Contoso dal profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="52814-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="52814-117">Il comando passa quindi tale endpoint al cmdlet **Disable-AzureRmTrafficManagerEndpoint** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="52814-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="52814-118">Questo cmdlet disabilita tale endpoint.</span><span class="sxs-lookup"><span data-stu-id="52814-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="52814-119">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="52814-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="52814-120">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="52814-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="52814-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52814-121">PARAMETERS</span></span>

### <span data-ttu-id="52814-122">-Force</span><span class="sxs-lookup"><span data-stu-id="52814-122">-Force</span></span>
<span data-ttu-id="52814-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="52814-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="52814-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="52814-124">-Name</span></span>
<span data-ttu-id="52814-125">Specifica il nome dell'endpoint di gestione traffico che questo cmdlet disabilita.</span><span class="sxs-lookup"><span data-stu-id="52814-125">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="52814-126">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="52814-126">-ProfileName</span></span>
<span data-ttu-id="52814-127">Specifica il nome di un profilo di Traffic Manager in cui questo cmdlet disabilita un endpoint.</span><span class="sxs-lookup"><span data-stu-id="52814-127">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="52814-128">Per ottenere un profilo, usare il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="52814-128">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="52814-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52814-129">-ResourceGroupName</span></span>
<span data-ttu-id="52814-130">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52814-130">Specifies the name of a resource group.</span></span>
<span data-ttu-id="52814-131">Questo cmdlet disabilita un endpoint di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="52814-131">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="52814-132">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52814-132">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="52814-133">Specifica l'endpoint di gestione traffico che questo cmdlet disabilita.</span><span class="sxs-lookup"><span data-stu-id="52814-133">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="52814-134">Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="52814-134">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="52814-135">-Digitare</span><span class="sxs-lookup"><span data-stu-id="52814-135">-Type</span></span>
<span data-ttu-id="52814-136">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="52814-136">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="52814-137">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="52814-137">Valid values are:</span></span> 

- <span data-ttu-id="52814-138">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="52814-138">AzureEndpoints</span></span>
- <span data-ttu-id="52814-139">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="52814-139">ExternalEndpoints</span></span>
- <span data-ttu-id="52814-140">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="52814-140">NestedEndpoints</span></span>

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

### <span data-ttu-id="52814-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52814-141">-Confirm</span></span>
<span data-ttu-id="52814-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52814-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52814-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52814-143">-WhatIf</span></span>
<span data-ttu-id="52814-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52814-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52814-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52814-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52814-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52814-146">-DefaultProfile</span></span>
<span data-ttu-id="52814-147">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52814-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52814-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52814-148">CommonParameters</span></span>
<span data-ttu-id="52814-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52814-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52814-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52814-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52814-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52814-151">INPUTS</span></span>

### <span data-ttu-id="52814-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52814-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="52814-153">Il parametro ' TrafficManagerEndpoint ' accetta il valore di tipo ' TrafficManagerEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="52814-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="52814-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52814-154">OUTPUTS</span></span>

### <span data-ttu-id="52814-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52814-155">System.Boolean</span></span>

## <span data-ttu-id="52814-156">Note</span><span class="sxs-lookup"><span data-stu-id="52814-156">NOTES</span></span>

## <span data-ttu-id="52814-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52814-157">RELATED LINKS</span></span>

[<span data-ttu-id="52814-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52814-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="52814-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52814-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="52814-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="52814-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="52814-161">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52814-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="52814-162">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="52814-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="52814-163">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="52814-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="52814-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="52814-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


