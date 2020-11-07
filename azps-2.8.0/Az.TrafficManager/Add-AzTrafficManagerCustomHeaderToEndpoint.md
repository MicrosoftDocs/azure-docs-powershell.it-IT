---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 7e3661a827bb6864fbd43abde43c7ab2bb440ecb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856001"
---
# <span data-ttu-id="53377-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="53377-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="53377-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53377-102">SYNOPSIS</span></span>
<span data-ttu-id="53377-103">Aggiunge informazioni di intestazione personalizzate a un oggetto endpoint di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="53377-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="53377-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53377-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53377-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53377-105">DESCRIPTION</span></span>
<span data-ttu-id="53377-106">Il cmdlet **Add-AzTrafficManagerCustomHeaderToEndpoint** aggiunge informazioni di intestazione personalizzate a un oggetto endpoint di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="53377-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="53377-107">Puoi ottenere un endpoint usando i cmdlet New-AzTrafficManagerEndpoint o Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="53377-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="53377-108">Questo cmdlet funziona sull'oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="53377-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="53377-109">Eseguire il commit delle modifiche apportate all'endpoint per Traffic Manager usando il cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="53377-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="53377-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53377-110">EXAMPLES</span></span>

### <span data-ttu-id="53377-111">Esempio 1: aggiungere informazioni di intestazione personalizzate a un endpoint</span><span class="sxs-lookup"><span data-stu-id="53377-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="53377-112">Con il primo comando viene creato un endpoint di Azure Traffic Manager usando il cmdlet **New-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="53377-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="53377-113">Il comando Archivia l'endpoint locale nella variabile $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="53377-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="53377-114">Il secondo comando aggiunge informazioni di intestazione personalizzate all'endpoint archiviato in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="53377-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="53377-115">Il comando finale aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="53377-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="53377-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53377-116">PARAMETERS</span></span>

### <span data-ttu-id="53377-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53377-117">-DefaultProfile</span></span>
<span data-ttu-id="53377-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53377-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53377-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="53377-119">-Name</span></span>
<span data-ttu-id="53377-120">Specifica il nome delle informazioni di intestazione personalizzate da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="53377-120">Specifies the name of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53377-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="53377-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="53377-122">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="53377-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="53377-123">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="53377-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="53377-124">Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzTrafficManagerEndpoint o New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="53377-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53377-125">-Valore</span><span class="sxs-lookup"><span data-stu-id="53377-125">-Value</span></span>
<span data-ttu-id="53377-126">Specifica il valore delle informazioni di intestazione personalizzate da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="53377-126">Specifies the value of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53377-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53377-127">-Confirm</span></span>
<span data-ttu-id="53377-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53377-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53377-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53377-129">-WhatIf</span></span>
<span data-ttu-id="53377-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53377-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53377-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53377-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53377-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53377-132">CommonParameters</span></span>
<span data-ttu-id="53377-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53377-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53377-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53377-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53377-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53377-135">INPUTS</span></span>

### <span data-ttu-id="53377-136">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="53377-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="53377-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53377-137">OUTPUTS</span></span>

### <span data-ttu-id="53377-138">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="53377-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="53377-139">Note</span><span class="sxs-lookup"><span data-stu-id="53377-139">NOTES</span></span>

## <span data-ttu-id="53377-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53377-140">RELATED LINKS</span></span>

[<span data-ttu-id="53377-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="53377-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="53377-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="53377-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="53377-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53377-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="53377-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="53377-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
