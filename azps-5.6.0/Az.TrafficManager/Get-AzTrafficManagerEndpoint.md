---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 04764a27a6940c0bc2b5d0e6df0baad350606972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950781"
---
# <span data-ttu-id="0f883-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f883-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="0f883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f883-102">SYNOPSIS</span></span>
<span data-ttu-id="0f883-103">Ottiene un endpoint per un profilo di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="0f883-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="0f883-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f883-104">SYNTAX</span></span>

### <span data-ttu-id="0f883-105">Campi</span><span class="sxs-lookup"><span data-stu-id="0f883-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f883-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="0f883-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f883-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f883-107">DESCRIPTION</span></span>
<span data-ttu-id="0f883-108">Il cmdlet **Get-AzTrafficManagerEndpoint** ottiene un endpoint per un profilo di Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="0f883-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="0f883-109">È possibile modificare l'oggetto in locale e quindi applicarvi le modifiche usando il cmdlet Set-AzTrafficManagerEndpoint></span><span class="sxs-lookup"><span data-stu-id="0f883-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="0f883-110">Specificare l'endpoint usando i parametri *Name* *e Type.*</span><span class="sxs-lookup"><span data-stu-id="0f883-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="0f883-111">È possibile specificare il profilo di Gestione traffico usando il parametro *ProfileName* e *ResourceGroupName* oppure specificando un **oggetto TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="0f883-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="0f883-112">In alternativa, è possibile passare questo valore usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="0f883-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="0f883-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f883-113">EXAMPLES</span></span>

### <span data-ttu-id="0f883-114">Esempio 1: Ottenere un endpoint</span><span class="sxs-lookup"><span data-stu-id="0f883-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="0f883-115">Questo comando recupera l'endpoint di Azure denominato contoso dal profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $TrafficManagerEndpoint variabile.</span><span class="sxs-lookup"><span data-stu-id="0f883-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="0f883-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f883-116">PARAMETERS</span></span>

### <span data-ttu-id="0f883-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f883-117">-DefaultProfile</span></span>
<span data-ttu-id="0f883-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f883-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f883-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0f883-119">-Name</span></span>
<span data-ttu-id="0f883-120">Specifica il nome dell'endpoint di Gestione traffico che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f883-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0f883-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0f883-121">-ProfileName</span></span>
<span data-ttu-id="0f883-122">Specifica il nome dell'endpoint di Gestione traffico che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f883-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0f883-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f883-123">-ResourceGroupName</span></span>
<span data-ttu-id="0f883-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f883-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0f883-125">Questo cmdlet ottiene un endpoint di Gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0f883-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0f883-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f883-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="0f883-127">Specifica l'endpoint di Gestione traffico che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f883-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0f883-128">-Type</span><span class="sxs-lookup"><span data-stu-id="0f883-128">-Type</span></span>
<span data-ttu-id="0f883-129">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="0f883-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="0f883-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="0f883-130">Valid values are:</span></span> 

- <span data-ttu-id="0f883-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="0f883-131">AzureEndpoints</span></span>
- <span data-ttu-id="0f883-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="0f883-132">ExternalEndpoints</span></span>
- <span data-ttu-id="0f883-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="0f883-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="0f883-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f883-134">CommonParameters</span></span>
<span data-ttu-id="0f883-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f883-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f883-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f883-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f883-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f883-137">INPUTS</span></span>

### <span data-ttu-id="0f883-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f883-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0f883-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f883-139">OUTPUTS</span></span>

### <span data-ttu-id="0f883-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f883-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0f883-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f883-141">NOTES</span></span>

## <span data-ttu-id="0f883-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f883-142">RELATED LINKS</span></span>

[<span data-ttu-id="0f883-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f883-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0f883-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f883-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0f883-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f883-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0f883-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f883-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0f883-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f883-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


