---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9ac1bb863053fc322265613a24d90b700d1846cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855249"
---
# <span data-ttu-id="afc70-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afc70-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="afc70-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="afc70-102">SYNOPSIS</span></span>
<span data-ttu-id="afc70-103">Ottiene un endpoint per un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="afc70-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="afc70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afc70-104">SYNTAX</span></span>

### <span data-ttu-id="afc70-105">Campi</span><span class="sxs-lookup"><span data-stu-id="afc70-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afc70-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="afc70-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afc70-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afc70-107">DESCRIPTION</span></span>
<span data-ttu-id="afc70-108">Il cmdlet **Get-AzTrafficManagerEndpoint** ottiene un endpoint per un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="afc70-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="afc70-109">Puoi modificare l'oggetto localmente e quindi applicare le modifiche al profilo usando il cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="afc70-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="afc70-110">Specificare l'endpoint usando i parametri *Name* e *Type* .</span><span class="sxs-lookup"><span data-stu-id="afc70-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="afc70-111">Puoi specificare il profilo di Traffic Manager usando il parametro *ProfileName* e *ResourceGroupName* oppure specificando un oggetto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="afc70-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="afc70-112">In alternativa, puoi passare tale valore usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="afc70-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="afc70-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afc70-113">EXAMPLES</span></span>

### <span data-ttu-id="afc70-114">Esempio 1: ottenere un endpoint</span><span class="sxs-lookup"><span data-stu-id="afc70-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="afc70-115">Questo comando ottiene l'endpoint Azure denominato Contoso dal profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="afc70-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="afc70-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="afc70-116">PARAMETERS</span></span>

### <span data-ttu-id="afc70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc70-117">-DefaultProfile</span></span>
<span data-ttu-id="afc70-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afc70-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afc70-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="afc70-119">-Name</span></span>
<span data-ttu-id="afc70-120">Specifica il nome dell'endpoint di gestione traffico che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afc70-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="afc70-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="afc70-121">-ProfileName</span></span>
<span data-ttu-id="afc70-122">Specifica il nome dell'endpoint di gestione traffico che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afc70-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="afc70-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afc70-123">-ResourceGroupName</span></span>
<span data-ttu-id="afc70-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="afc70-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="afc70-125">Questo cmdlet ottiene un endpoint di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="afc70-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="afc70-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afc70-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="afc70-127">Specifica l'endpoint di gestione traffico che ottiene questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afc70-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="afc70-128">-Digitare</span><span class="sxs-lookup"><span data-stu-id="afc70-128">-Type</span></span>
<span data-ttu-id="afc70-129">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="afc70-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="afc70-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="afc70-130">Valid values are:</span></span> 

- <span data-ttu-id="afc70-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="afc70-131">AzureEndpoints</span></span>
- <span data-ttu-id="afc70-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="afc70-132">ExternalEndpoints</span></span>
- <span data-ttu-id="afc70-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="afc70-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="afc70-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc70-134">CommonParameters</span></span>
<span data-ttu-id="afc70-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afc70-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc70-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afc70-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc70-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="afc70-137">INPUTS</span></span>

### <span data-ttu-id="afc70-138">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afc70-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="afc70-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afc70-139">OUTPUTS</span></span>

### <span data-ttu-id="afc70-140">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afc70-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="afc70-141">Note</span><span class="sxs-lookup"><span data-stu-id="afc70-141">NOTES</span></span>

## <span data-ttu-id="afc70-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afc70-142">RELATED LINKS</span></span>

[<span data-ttu-id="afc70-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afc70-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="afc70-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afc70-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="afc70-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afc70-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="afc70-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afc70-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="afc70-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afc70-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


