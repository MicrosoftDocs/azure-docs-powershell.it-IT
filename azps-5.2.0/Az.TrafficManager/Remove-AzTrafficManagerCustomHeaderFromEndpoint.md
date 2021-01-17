---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 35ab92add873e603101400f77e813fb115386fd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330451"
---
# <span data-ttu-id="12ed3-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="12ed3-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="12ed3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="12ed3-103">Rimuove le informazioni di intestazione personalizzate da un oggetto endpoint di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="12ed3-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="12ed3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12ed3-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12ed3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12ed3-105">DESCRIPTION</span></span>
<span data-ttu-id="12ed3-106">Il cmdlet **Remove-AzTrafficManagerCustomHeaderFromEndpoint** rimuove le informazioni di intestazione personalizzate da un oggetto endpoint di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="12ed3-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="12ed3-107">Puoi ottenere un endpoint usando i cmdlet New-AzTrafficManagerEndpoint o Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="12ed3-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="12ed3-108">Questo cmdlet funziona sull'oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="12ed3-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="12ed3-109">Eseguire il commit delle modifiche apportate all'endpoint per Traffic Manager usando il cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="12ed3-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="12ed3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12ed3-110">EXAMPLES</span></span>

### <span data-ttu-id="12ed3-111">Esempio 1: rimuovere le informazioni di subnet personalizzate da un endpoint</span><span class="sxs-lookup"><span data-stu-id="12ed3-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="12ed3-112">Il primo comando ottiene l'endpoint Azure denominato Contoso dal profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="12ed3-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="12ed3-113">Il secondo comando rimuove le informazioni di intestazione personalizzate dall'endpoint archiviato in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="12ed3-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="12ed3-114">Il comando finale aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="12ed3-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="12ed3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12ed3-115">PARAMETERS</span></span>

### <span data-ttu-id="12ed3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ed3-116">-DefaultProfile</span></span>
<span data-ttu-id="12ed3-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12ed3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12ed3-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="12ed3-118">-Name</span></span>
<span data-ttu-id="12ed3-119">Specifica il nome delle informazioni di intestazione personalizzate da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="12ed3-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="12ed3-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="12ed3-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="12ed3-121">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="12ed3-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="12ed3-122">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="12ed3-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="12ed3-123">Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzTrafficManagerEndpoint o New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="12ed3-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="12ed3-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12ed3-124">-Confirm</span></span>
<span data-ttu-id="12ed3-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12ed3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12ed3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ed3-126">-WhatIf</span></span>
<span data-ttu-id="12ed3-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12ed3-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12ed3-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12ed3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12ed3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ed3-129">CommonParameters</span></span>
<span data-ttu-id="12ed3-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ed3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ed3-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12ed3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ed3-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12ed3-132">INPUTS</span></span>

### <span data-ttu-id="12ed3-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="12ed3-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="12ed3-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12ed3-134">OUTPUTS</span></span>

### <span data-ttu-id="12ed3-135">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="12ed3-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="12ed3-136">Note</span><span class="sxs-lookup"><span data-stu-id="12ed3-136">NOTES</span></span>

## <span data-ttu-id="12ed3-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12ed3-137">RELATED LINKS</span></span>

[<span data-ttu-id="12ed3-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="12ed3-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="12ed3-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="12ed3-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="12ed3-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="12ed3-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="12ed3-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="12ed3-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
