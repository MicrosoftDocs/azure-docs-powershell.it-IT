---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 50ad29e9c28b42b1459d66358b8c6c37e2e0f4ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518259"
---
# <span data-ttu-id="ded21-101">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ded21-101">Get-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="ded21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ded21-102">SYNOPSIS</span></span>
<span data-ttu-id="ded21-103">Ottiene un endpoint per un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="ded21-103">Gets an endpoint for a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ded21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ded21-104">SYNTAX</span></span>

### <span data-ttu-id="ded21-105">Campi</span><span class="sxs-lookup"><span data-stu-id="ded21-105">Fields</span></span>
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ded21-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="ded21-106">Object</span></span>
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ded21-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ded21-107">DESCRIPTION</span></span>
<span data-ttu-id="ded21-108">Il cmdlet **Get-AzureRmTrafficManagerEndpoint** ottiene un endpoint per un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="ded21-108">The **Get-AzureRmTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="ded21-109">Puoi modificare l'oggetto localmente e quindi applicare le modifiche al profilo usando il cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ded21-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="ded21-110">Specificare l'endpoint usando i parametri *Name* e *Type* .</span><span class="sxs-lookup"><span data-stu-id="ded21-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="ded21-111">Puoi specificare il profilo di Traffic Manager usando il parametro *ProfileName* e *ResourceGroupName* oppure specificando un oggetto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="ded21-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ded21-112">In alternativa, puoi passare tale valore usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="ded21-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="ded21-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ded21-113">EXAMPLES</span></span>

### <span data-ttu-id="ded21-114">Esempio 1: ottenere un endpoint</span><span class="sxs-lookup"><span data-stu-id="ded21-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="ded21-115">Questo comando ottiene l'endpoint Azure denominato Contoso dal profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ded21-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="ded21-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ded21-116">PARAMETERS</span></span>

### <span data-ttu-id="ded21-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ded21-117">-Name</span></span>
<span data-ttu-id="ded21-118">Specifica il nome dell'endpoint di gestione traffico che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ded21-118">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ded21-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ded21-119">-ProfileName</span></span>
<span data-ttu-id="ded21-120">Specifica il nome dell'endpoint di gestione traffico che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ded21-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ded21-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded21-121">-ResourceGroupName</span></span>
<span data-ttu-id="ded21-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ded21-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ded21-123">Questo cmdlet ottiene un endpoint di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ded21-123">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ded21-124">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ded21-124">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="ded21-125">Specifica l'endpoint di gestione traffico che ottiene questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ded21-125">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ded21-126">-Digitare</span><span class="sxs-lookup"><span data-stu-id="ded21-126">-Type</span></span>
<span data-ttu-id="ded21-127">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="ded21-127">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="ded21-128">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ded21-128">Valid values are:</span></span> 

- <span data-ttu-id="ded21-129">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="ded21-129">AzureEndpoints</span></span>
- <span data-ttu-id="ded21-130">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="ded21-130">ExternalEndpoints</span></span>
- <span data-ttu-id="ded21-131">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="ded21-131">NestedEndpoints</span></span>

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

### <span data-ttu-id="ded21-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded21-132">-DefaultProfile</span></span>
<span data-ttu-id="ded21-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ded21-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ded21-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded21-134">CommonParameters</span></span>
<span data-ttu-id="ded21-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded21-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded21-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ded21-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded21-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ded21-137">INPUTS</span></span>

### <span data-ttu-id="ded21-138">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ded21-138">TrafficManagerEndpoint</span></span>
<span data-ttu-id="ded21-139">Il parametro ' TrafficManagerEndpoint ' accetta il valore di tipo ' TrafficManagerEndpoint ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ded21-139">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="ded21-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ded21-140">OUTPUTS</span></span>

### <span data-ttu-id="ded21-141">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ded21-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ded21-142">Note</span><span class="sxs-lookup"><span data-stu-id="ded21-142">NOTES</span></span>

## <span data-ttu-id="ded21-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ded21-143">RELATED LINKS</span></span>

[<span data-ttu-id="ded21-144">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ded21-144">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ded21-145">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ded21-145">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ded21-146">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ded21-146">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ded21-147">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ded21-147">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ded21-148">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ded21-148">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)


