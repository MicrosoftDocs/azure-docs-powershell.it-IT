---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f0d179c82292ffb9300791337f40436c4d4c5f36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987291"
---
# <span data-ttu-id="458c6-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="458c6-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="458c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="458c6-102">SYNOPSIS</span></span>
<span data-ttu-id="458c6-103">Rimuove informazioni di intestazione personalizzate da un oggetto endpoint di Gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="458c6-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="458c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="458c6-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="458c6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="458c6-105">DESCRIPTION</span></span>
<span data-ttu-id="458c6-106">Il cmdlet **Remove-AzTrafficManagerCustomHeaderFromEndpoint** rimuove le informazioni di intestazione personalizzate da un oggetto endpoint locale di Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="458c6-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="458c6-107">È possibile ottenere un endpoint usando i cmdlet New-AzTrafficManagerEndpoint o Get-AzTrafficManagerEndpoint endpoint.</span><span class="sxs-lookup"><span data-stu-id="458c6-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="458c6-108">Questo cmdlet opera sull'oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="458c6-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="458c6-109">Eseguire il commit delle modifiche nell'endpoint per Gestione traffico usando il cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="458c6-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="458c6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="458c6-110">EXAMPLES</span></span>

### <span data-ttu-id="458c6-111">Esempio 1: Rimuovere informazioni sulla subnet personalizzata da un endpoint</span><span class="sxs-lookup"><span data-stu-id="458c6-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="458c6-112">Il primo comando recupera l'endpoint di Azure denominato contoso dal profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11 e quindi archivia l'oggetto nella $TrafficManagerEndpoint variabile.</span><span class="sxs-lookup"><span data-stu-id="458c6-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="458c6-113">Il secondo comando rimuove le informazioni di intestazione personalizzate dall'endpoint archiviato in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="458c6-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="458c6-114">Il comando finale aggiorna l'endpoint in Gestione traffico in modo che corrisponda al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="458c6-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="458c6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="458c6-115">PARAMETERS</span></span>

### <span data-ttu-id="458c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="458c6-116">-DefaultProfile</span></span>
<span data-ttu-id="458c6-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="458c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="458c6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="458c6-118">-Name</span></span>
<span data-ttu-id="458c6-119">Specifica il nome delle informazioni di intestazione personalizzate da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="458c6-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="458c6-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="458c6-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="458c6-121">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="458c6-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="458c6-122">Questo cmdlet modifica l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="458c6-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="458c6-123">Per ottenere un **oggetto TrafficManagerEndpoint,** usare il cmdlet Get-AzTrafficManagerEndpoint o New-AzTrafficManagerEndpoint TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="458c6-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="458c6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="458c6-124">-Confirm</span></span>
<span data-ttu-id="458c6-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="458c6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="458c6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="458c6-126">-WhatIf</span></span>
<span data-ttu-id="458c6-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="458c6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="458c6-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="458c6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="458c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="458c6-129">CommonParameters</span></span>
<span data-ttu-id="458c6-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="458c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="458c6-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="458c6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="458c6-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="458c6-132">INPUTS</span></span>

### <span data-ttu-id="458c6-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="458c6-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="458c6-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="458c6-134">OUTPUTS</span></span>

### <span data-ttu-id="458c6-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="458c6-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="458c6-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="458c6-136">NOTES</span></span>

## <span data-ttu-id="458c6-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="458c6-137">RELATED LINKS</span></span>

[<span data-ttu-id="458c6-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="458c6-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="458c6-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="458c6-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="458c6-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="458c6-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="458c6-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="458c6-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
