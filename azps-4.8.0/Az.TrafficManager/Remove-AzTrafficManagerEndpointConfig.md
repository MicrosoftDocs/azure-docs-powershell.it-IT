---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4795e89013acaadcc08477370441ff5acdded85a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191104"
---
# <span data-ttu-id="af167-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="af167-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="af167-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af167-102">SYNOPSIS</span></span>
<span data-ttu-id="af167-103">Rimuove un endpoint da un oggetto profilo di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="af167-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="af167-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af167-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af167-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af167-105">DESCRIPTION</span></span>
<span data-ttu-id="af167-106">Il cmdlet **Remove-AzTrafficManagerEndpointConfig** rimuove un endpoint da un oggetto profilo di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="af167-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="af167-107">Puoi ottenere un profilo usando il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="af167-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="af167-108">Questo cmdlet opera nell'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="af167-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="af167-109">Eseguire il commit delle modifiche apportate al profilo per Traffic Manager usando il cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="af167-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="af167-110">Per rimuovere un endpoint e eseguire il commit delle modifiche in una singola operazione, usare il cmdlet Remove-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="af167-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="af167-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af167-111">EXAMPLES</span></span>

### <span data-ttu-id="af167-112">Esempio 1: rimuovere un endpoint</span><span class="sxs-lookup"><span data-stu-id="af167-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="af167-113">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="af167-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="af167-114">Il comando Archivia il profilo locale nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="af167-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="af167-115">Il secondo comando rimuove un endpoint Azure denominato Contoso dal profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="af167-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="af167-116">Questo comando modifica solo l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="af167-116">This command changes only the local object.</span></span>

<span data-ttu-id="af167-117">Il comando finale aggiorna il profilo di Traffic Manager denominato ContosoProfile in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="af167-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="af167-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af167-118">PARAMETERS</span></span>

### <span data-ttu-id="af167-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af167-119">-DefaultProfile</span></span>
<span data-ttu-id="af167-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af167-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af167-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="af167-121">-EndpointName</span></span>
<span data-ttu-id="af167-122">Specifica il nome dell'endpoint di gestione traffico rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af167-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="af167-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af167-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="af167-124">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="af167-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="af167-125">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="af167-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="af167-126">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="af167-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af167-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af167-127">CommonParameters</span></span>
<span data-ttu-id="af167-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af167-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af167-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af167-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af167-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af167-130">INPUTS</span></span>

### <span data-ttu-id="af167-131">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af167-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="af167-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af167-132">OUTPUTS</span></span>

### <span data-ttu-id="af167-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af167-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="af167-134">Note</span><span class="sxs-lookup"><span data-stu-id="af167-134">NOTES</span></span>

## <span data-ttu-id="af167-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af167-135">RELATED LINKS</span></span>

[<span data-ttu-id="af167-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="af167-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="af167-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af167-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="af167-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="af167-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="af167-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="af167-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


