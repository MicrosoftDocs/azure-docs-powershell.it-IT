---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 64fdd0cb3c2fa31396d9e917dcd7c2e26730c755
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508511"
---
# <span data-ttu-id="1bc8c-101">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1bc8c-101">Enable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="1bc8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bc8c-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc8c-103">Abilita un endpoint in un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-103">Enables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bc8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bc8c-104">SYNTAX</span></span>

### <span data-ttu-id="1bc8c-105">Campi</span><span class="sxs-lookup"><span data-stu-id="1bc8c-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bc8c-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="1bc8c-106">Object</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bc8c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bc8c-107">DESCRIPTION</span></span>
<span data-ttu-id="1bc8c-108">Il cmdlet **Enable-AzureRmTrafficManagerEndpoint** Abilita un endpoint in un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-108">The **Enable-AzureRmTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="1bc8c-109">Puoi usare l'operatore pipeline per passare un oggetto **TrafficManagerEndpoint** a questo cmdlet oppure puoi specificare un oggetto **TrafficManagerEndpoint** usando il parametro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="1bc8c-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="1bc8c-110">In alternativa, puoi specificare il nome e il tipo di endpoint usando i parametri *Name* e *Type* , insieme ai parametri *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="1bc8c-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="1bc8c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bc8c-111">EXAMPLES</span></span>

### <span data-ttu-id="1bc8c-112">Esempio 1: abilitare un endpoint da un profilo</span><span class="sxs-lookup"><span data-stu-id="1bc8c-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="1bc8c-113">Questo comando Abilita l'endpoint esterno denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="1bc8c-114">Esempio 2: abilitare un endpoint usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="1bc8c-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

<span data-ttu-id="1bc8c-115">Questo comando ottiene l'endpoint esterno denominato Contoso dal profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="1bc8c-116">Il comando passa quindi tale endpoint al cmdlet **Enable-AzureRmTrafficManagerEndpoint** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-116">The command then passes that endpoint to the **Enable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1bc8c-117">Questo cmdlet abilita tale endpoint.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="1bc8c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bc8c-118">PARAMETERS</span></span>

### <span data-ttu-id="1bc8c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bc8c-119">-Name</span></span>
<span data-ttu-id="1bc8c-120">Specifica il nome dell'endpoint di gestione traffico che questo cmdlet consente.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-120">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="1bc8c-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1bc8c-121">-ProfileName</span></span>
<span data-ttu-id="1bc8c-122">Specifica il nome di un profilo di Traffic Manager in cui questo cmdlet Abilita un endpoint.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-122">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="1bc8c-123">Per ottenere un profilo, usare il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-123">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="1bc8c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bc8c-124">-ResourceGroupName</span></span>
<span data-ttu-id="1bc8c-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-125">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1bc8c-126">Questo cmdlet consente a un endpoint di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-126">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1bc8c-127">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1bc8c-127">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="1bc8c-128">Specifica l'endpoint di gestione traffico attivato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-128">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="1bc8c-129">Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="1bc8c-130">-Digitare</span><span class="sxs-lookup"><span data-stu-id="1bc8c-130">-Type</span></span>
<span data-ttu-id="1bc8c-131">Specifica il tipo di endpoint disabilitato dal cmdlet nel profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-131">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="1bc8c-132">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1bc8c-132">Valid values are:</span></span> 

- <span data-ttu-id="1bc8c-133">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="1bc8c-133">AzureEndpoints</span></span>
- <span data-ttu-id="1bc8c-134">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="1bc8c-134">ExternalEndpoints</span></span>
- <span data-ttu-id="1bc8c-135">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="1bc8c-135">NestedEndpoints</span></span>

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

### <span data-ttu-id="1bc8c-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bc8c-136">-DefaultProfile</span></span>
<span data-ttu-id="1bc8c-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bc8c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc8c-138">CommonParameters</span></span>
<span data-ttu-id="1bc8c-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bc8c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bc8c-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bc8c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc8c-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bc8c-141">INPUTS</span></span>

### <span data-ttu-id="1bc8c-142">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1bc8c-142">TrafficManagerEndpoint</span></span>
<span data-ttu-id="1bc8c-143">Il parametro ' TrafficManagerEndpoint ' accetta il valore di tipo ' TrafficManagerEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1bc8c-143">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="1bc8c-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bc8c-144">OUTPUTS</span></span>

### <span data-ttu-id="1bc8c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1bc8c-145">System.Boolean</span></span>

## <span data-ttu-id="1bc8c-146">Note</span><span class="sxs-lookup"><span data-stu-id="1bc8c-146">NOTES</span></span>

## <span data-ttu-id="1bc8c-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bc8c-147">RELATED LINKS</span></span>

[<span data-ttu-id="1bc8c-148">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1bc8c-148">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="1bc8c-149">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1bc8c-149">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="1bc8c-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bc8c-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1bc8c-151">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1bc8c-151">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="1bc8c-152">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bc8c-152">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1bc8c-153">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1bc8c-153">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="1bc8c-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1bc8c-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


