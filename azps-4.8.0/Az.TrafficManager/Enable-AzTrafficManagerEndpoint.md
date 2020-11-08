---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032782"
---
# <span data-ttu-id="2daea-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2daea-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="2daea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2daea-102">SYNOPSIS</span></span>
<span data-ttu-id="2daea-103">Abilita un endpoint in un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="2daea-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="2daea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2daea-104">SYNTAX</span></span>

### <span data-ttu-id="2daea-105">Campi</span><span class="sxs-lookup"><span data-stu-id="2daea-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2daea-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="2daea-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2daea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2daea-107">DESCRIPTION</span></span>
<span data-ttu-id="2daea-108">Il cmdlet **Enable-AzTrafficManagerEndpoint** Abilita un endpoint in un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="2daea-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="2daea-109">Puoi usare l'operatore pipeline per passare un oggetto **TrafficManagerEndpoint** a questo cmdlet oppure puoi specificare un oggetto **TrafficManagerEndpoint** usando il parametro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="2daea-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="2daea-110">In alternativa, puoi specificare il nome e il tipo di endpoint usando i parametri *Name* e *Type* , insieme ai parametri *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2daea-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="2daea-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2daea-111">EXAMPLES</span></span>

### <span data-ttu-id="2daea-112">Esempio 1: abilitare un endpoint da un profilo</span><span class="sxs-lookup"><span data-stu-id="2daea-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="2daea-113">Questo comando Abilita l'endpoint esterno denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2daea-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="2daea-114">Esempio 2: abilitare un endpoint usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="2daea-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="2daea-115">Questo comando ottiene l'endpoint esterno denominato Contoso dal profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2daea-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="2daea-116">Il comando passa quindi tale endpoint al cmdlet **Enable-AzTrafficManagerEndpoint** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="2daea-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2daea-117">Questo cmdlet abilita tale endpoint.</span><span class="sxs-lookup"><span data-stu-id="2daea-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="2daea-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2daea-118">PARAMETERS</span></span>

### <span data-ttu-id="2daea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2daea-119">-DefaultProfile</span></span>
<span data-ttu-id="2daea-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2daea-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2daea-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2daea-121">-Name</span></span>
<span data-ttu-id="2daea-122">Specifica il nome dell'endpoint di gestione traffico che questo cmdlet consente.</span><span class="sxs-lookup"><span data-stu-id="2daea-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="2daea-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2daea-123">-ProfileName</span></span>
<span data-ttu-id="2daea-124">Specifica il nome di un profilo di Traffic Manager in cui questo cmdlet Abilita un endpoint.</span><span class="sxs-lookup"><span data-stu-id="2daea-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="2daea-125">Per ottenere un profilo, usare il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2daea-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="2daea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2daea-126">-ResourceGroupName</span></span>
<span data-ttu-id="2daea-127">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2daea-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2daea-128">Questo cmdlet consente a un endpoint di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="2daea-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2daea-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2daea-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="2daea-130">Specifica l'endpoint di gestione traffico attivato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2daea-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="2daea-131">Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2daea-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="2daea-132">-Digitare</span><span class="sxs-lookup"><span data-stu-id="2daea-132">-Type</span></span>
<span data-ttu-id="2daea-133">Specifica il tipo di endpoint disabilitato dal cmdlet nel profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="2daea-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="2daea-134">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="2daea-134">Valid values are:</span></span> 

- <span data-ttu-id="2daea-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="2daea-135">AzureEndpoints</span></span>
- <span data-ttu-id="2daea-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="2daea-136">ExternalEndpoints</span></span>
- <span data-ttu-id="2daea-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="2daea-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="2daea-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2daea-138">CommonParameters</span></span>
<span data-ttu-id="2daea-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2daea-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2daea-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2daea-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2daea-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2daea-141">INPUTS</span></span>

### <span data-ttu-id="2daea-142">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2daea-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="2daea-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2daea-143">OUTPUTS</span></span>

### <span data-ttu-id="2daea-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2daea-144">System.Boolean</span></span>

## <span data-ttu-id="2daea-145">Note</span><span class="sxs-lookup"><span data-stu-id="2daea-145">NOTES</span></span>

## <span data-ttu-id="2daea-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2daea-146">RELATED LINKS</span></span>

[<span data-ttu-id="2daea-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2daea-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2daea-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2daea-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2daea-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2daea-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="2daea-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2daea-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2daea-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2daea-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="2daea-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2daea-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2daea-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2daea-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


