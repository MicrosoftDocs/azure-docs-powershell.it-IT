---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330400"
---
# <span data-ttu-id="32fe3-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="32fe3-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="32fe3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="32fe3-103">Rimuove un endpoint da Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="32fe3-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="32fe3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32fe3-104">SYNTAX</span></span>

### <span data-ttu-id="32fe3-105">Campi</span><span class="sxs-lookup"><span data-stu-id="32fe3-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32fe3-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="32fe3-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32fe3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32fe3-107">DESCRIPTION</span></span>
<span data-ttu-id="32fe3-108">Il cmdlet **Remove-AzTrafficManagerEndpoint** consente di rimuovere un endpoint da Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="32fe3-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="32fe3-109">Questo cmdlet consente di eseguire il commit di ogni modifica al servizio Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="32fe3-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="32fe3-110">Per rimuovere più endpoint da un oggetto profilo di gestione traffico locale e eseguire il commit delle modifiche in una singola operazione, usare il cmdlet Remove-AzTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="32fe3-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="32fe3-111">Puoi usare l'operatore pipeline per passare un oggetto **TrafficManagerEndpoint** a questo cmdlet oppure puoi specificare un oggetto **TrafficManagerEndpoint** usando il parametro *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="32fe3-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="32fe3-112">In alternativa, puoi specificare il nome e il tipo di endpoint usando i parametri *Name* e *Type* , insieme ai parametri *ProfileName* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="32fe3-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="32fe3-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32fe3-113">EXAMPLES</span></span>

### <span data-ttu-id="32fe3-114">Esempio 1: rimuovere un endpoint da un profilo</span><span class="sxs-lookup"><span data-stu-id="32fe3-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="32fe3-115">Questo comando rimuove l'endpoint Azure denominato Contoso dal profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="32fe3-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="32fe3-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32fe3-116">PARAMETERS</span></span>

### <span data-ttu-id="32fe3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32fe3-117">-DefaultProfile</span></span>
<span data-ttu-id="32fe3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32fe3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32fe3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="32fe3-119">-Force</span></span>
<span data-ttu-id="32fe3-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="32fe3-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="32fe3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="32fe3-121">-Name</span></span>
<span data-ttu-id="32fe3-122">Specifica il nome dell'endpoint di gestione traffico rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32fe3-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="32fe3-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="32fe3-123">-ProfileName</span></span>
<span data-ttu-id="32fe3-124">Specifica il nome di un profilo di Traffic Manager da cui questo cmdlet rimuove un endpoint.</span><span class="sxs-lookup"><span data-stu-id="32fe3-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="32fe3-125">Per ottenere un profilo, usare il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="32fe3-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="32fe3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32fe3-126">-ResourceGroupName</span></span>
<span data-ttu-id="32fe3-127">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32fe3-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="32fe3-128">Questo cmdlet consente di rimuovere un endpoint di gestione traffico da un profilo di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="32fe3-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="32fe3-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="32fe3-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="32fe3-130">Specifica l'endpoint del gestore di traffico rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32fe3-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="32fe3-131">Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="32fe3-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="32fe3-132">-Digitare</span><span class="sxs-lookup"><span data-stu-id="32fe3-132">-Type</span></span>
<span data-ttu-id="32fe3-133">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="32fe3-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="32fe3-134">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="32fe3-134">Valid values are:</span></span> 

- <span data-ttu-id="32fe3-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="32fe3-135">AzureEndpoints</span></span>
- <span data-ttu-id="32fe3-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="32fe3-136">ExternalEndpoints</span></span>
- <span data-ttu-id="32fe3-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="32fe3-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="32fe3-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32fe3-138">-Confirm</span></span>
<span data-ttu-id="32fe3-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32fe3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32fe3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32fe3-140">-WhatIf</span></span>
<span data-ttu-id="32fe3-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32fe3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32fe3-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32fe3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32fe3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32fe3-143">CommonParameters</span></span>
<span data-ttu-id="32fe3-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32fe3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32fe3-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32fe3-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32fe3-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32fe3-146">INPUTS</span></span>

### <span data-ttu-id="32fe3-147">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="32fe3-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="32fe3-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32fe3-148">OUTPUTS</span></span>

### <span data-ttu-id="32fe3-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32fe3-149">System.Boolean</span></span>

## <span data-ttu-id="32fe3-150">Note</span><span class="sxs-lookup"><span data-stu-id="32fe3-150">NOTES</span></span>

## <span data-ttu-id="32fe3-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32fe3-151">RELATED LINKS</span></span>

[<span data-ttu-id="32fe3-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="32fe3-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="32fe3-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="32fe3-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="32fe3-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="32fe3-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="32fe3-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="32fe3-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="32fe3-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="32fe3-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


