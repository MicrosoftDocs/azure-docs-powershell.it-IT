---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: ea69e8d07278be2c9f122d179090e63b9153128d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676343"
---
# <span data-ttu-id="86e1e-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="86e1e-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="86e1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="86e1e-103">Rimuove un intervallo di indirizzi o una subnet da un oggetto endpoint di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="86e1e-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="86e1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86e1e-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86e1e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86e1e-105">DESCRIPTION</span></span>
<span data-ttu-id="86e1e-106">Il cmdlet **Remove-AzTrafficManagerIpAddressRange** rimuove un intervallo di indirizzi IP da un oggetto endpoint di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="86e1e-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="86e1e-107">Puoi ottenere un endpoint usando i cmdlet New-AzTrafficManagerEndpoint o Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="86e1e-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="86e1e-108">Questo cmdlet funziona sull'oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="86e1e-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="86e1e-109">Eseguire il commit delle modifiche apportate all'endpoint per Traffic Manager usando il cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="86e1e-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="86e1e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86e1e-110">EXAMPLES</span></span>

### <span data-ttu-id="86e1e-111">Esempio 1: rimuovere gli intervalli di indirizzi IP da un endpoint</span><span class="sxs-lookup"><span data-stu-id="86e1e-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="86e1e-112">Il primo comando ottiene l'endpoint Azure denominato Contoso dal profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="86e1e-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="86e1e-113">Il secondo comando rimuove un intervallo di indirizzi IP dall'endpoint archiviato in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="86e1e-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="86e1e-114">Il comando finale aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="86e1e-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="86e1e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86e1e-115">PARAMETERS</span></span>

### <span data-ttu-id="86e1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e1e-116">-DefaultProfile</span></span>
<span data-ttu-id="86e1e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86e1e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86e1e-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86e1e-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="86e1e-119">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="86e1e-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="86e1e-120">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="86e1e-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="86e1e-121">Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzTrafficManagerEndpoint o New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="86e1e-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="86e1e-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86e1e-122">-Confirm</span></span>
<span data-ttu-id="86e1e-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86e1e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86e1e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e1e-124">-WhatIf</span></span>
<span data-ttu-id="86e1e-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86e1e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86e1e-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86e1e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86e1e-127">-Primo</span><span class="sxs-lookup"><span data-stu-id="86e1e-127">-First</span></span>
<span data-ttu-id="86e1e-128">Specifica il primo indirizzo IP nell'intervallo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="86e1e-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="86e1e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e1e-129">CommonParameters</span></span>
<span data-ttu-id="86e1e-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e1e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e1e-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86e1e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e1e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86e1e-132">INPUTS</span></span>

### <span data-ttu-id="86e1e-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86e1e-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="86e1e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86e1e-134">OUTPUTS</span></span>

### <span data-ttu-id="86e1e-135">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86e1e-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="86e1e-136">Note</span><span class="sxs-lookup"><span data-stu-id="86e1e-136">NOTES</span></span>

## <span data-ttu-id="86e1e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86e1e-137">RELATED LINKS</span></span>

[<span data-ttu-id="86e1e-138">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="86e1e-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="86e1e-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="86e1e-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="86e1e-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86e1e-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="86e1e-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86e1e-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
