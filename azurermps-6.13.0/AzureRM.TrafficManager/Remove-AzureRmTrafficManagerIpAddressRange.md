---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 5bb661dbc5a65b9a245fcfa35cdc194bbcded1eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508956"
---
# <span data-ttu-id="7d872-101">Remove-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="7d872-101">Remove-AzureRmTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="7d872-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d872-102">SYNOPSIS</span></span>
<span data-ttu-id="7d872-103">Rimuove un intervallo di indirizzi o una subnet da un oggetto endpoint di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="7d872-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d872-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d872-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d872-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d872-105">DESCRIPTION</span></span>
<span data-ttu-id="7d872-106">Il cmdlet **Remove-AzureRmTrafficManagerIpAddressRange** rimuove un intervallo di indirizzi IP da un oggetto endpoint di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="7d872-106">The **Remove-AzureRmTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="7d872-107">Puoi ottenere un endpoint usando i cmdlet New-AzureRmTrafficManagerEndpoint o Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7d872-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="7d872-108">Questo cmdlet funziona sull'oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="7d872-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="7d872-109">Eseguire il commit delle modifiche apportate all'endpoint per Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7d872-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="7d872-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d872-110">EXAMPLES</span></span>

### <span data-ttu-id="7d872-111">Esempio 1: rimuovere gli intervalli di indirizzi IP da un endpoint</span><span class="sxs-lookup"><span data-stu-id="7d872-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="7d872-112">Il primo comando ottiene l'endpoint Azure denominato Contoso dal profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11 e quindi archivia tale oggetto nella variabile $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7d872-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="7d872-113">Il secondo comando rimuove un intervallo di indirizzi IP dall'endpoint archiviato in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7d872-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="7d872-114">Il comando finale aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7d872-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="7d872-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d872-115">PARAMETERS</span></span>

### <span data-ttu-id="7d872-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d872-116">-DefaultProfile</span></span>
<span data-ttu-id="7d872-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d872-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d872-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d872-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="7d872-119">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="7d872-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="7d872-120">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="7d872-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="7d872-121">Per ottenere un oggetto **TrafficManagerEndpoint** , usa il cmdlet Get-AzureRmTrafficManagerEndpoint o New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7d872-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="7d872-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d872-122">-Confirm</span></span>
<span data-ttu-id="7d872-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d872-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d872-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d872-124">-WhatIf</span></span>
<span data-ttu-id="7d872-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d872-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d872-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d872-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d872-127">-Primo</span><span class="sxs-lookup"><span data-stu-id="7d872-127">-First</span></span>
<span data-ttu-id="7d872-128">Specifica il primo indirizzo IP nell'intervallo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7d872-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="7d872-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d872-129">CommonParameters</span></span>
<span data-ttu-id="7d872-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d872-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d872-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d872-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d872-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d872-132">INPUTS</span></span>

### <span data-ttu-id="7d872-133">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d872-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="7d872-134">Questo cmdlet accetta un oggetto **TrafficManagerEndpoint** per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d872-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="7d872-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d872-135">OUTPUTS</span></span>

### <span data-ttu-id="7d872-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d872-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="7d872-137">Questo cmdlet restituisce un oggetto TrafficManagerEndpoint modificato.</span><span class="sxs-lookup"><span data-stu-id="7d872-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="7d872-138">Note</span><span class="sxs-lookup"><span data-stu-id="7d872-138">NOTES</span></span>

## <span data-ttu-id="7d872-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d872-139">RELATED LINKS</span></span>

[<span data-ttu-id="7d872-140">Add-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="7d872-140">Add-AzureRmTrafficManagerIpAddressRange</span></span>](./Add-AzureRmTrafficManagerIpAddressRange.md)

[<span data-ttu-id="7d872-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7d872-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7d872-142">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d872-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7d872-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d872-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
