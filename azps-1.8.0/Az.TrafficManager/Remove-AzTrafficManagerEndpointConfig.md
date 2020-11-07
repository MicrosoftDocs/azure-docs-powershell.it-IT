---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: f40587460cf5e4a1d7f06bfb88229f6e4e3f7975
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676346"
---
# <span data-ttu-id="48203-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="48203-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="48203-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48203-102">SYNOPSIS</span></span>
<span data-ttu-id="48203-103">Rimuove un endpoint da un oggetto profilo di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="48203-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="48203-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48203-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48203-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48203-105">DESCRIPTION</span></span>
<span data-ttu-id="48203-106">Il cmdlet **Remove-AzTrafficManagerEndpointConfig** rimuove un endpoint da un oggetto profilo di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="48203-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="48203-107">Puoi ottenere un profilo usando il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="48203-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="48203-108">Questo cmdlet opera nell'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="48203-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="48203-109">Eseguire il commit delle modifiche apportate al profilo per Traffic Manager usando il cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="48203-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="48203-110">Per rimuovere un endpoint e eseguire il commit delle modifiche in una singola operazione, usare il cmdlet Remove-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="48203-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="48203-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48203-111">EXAMPLES</span></span>

### <span data-ttu-id="48203-112">Esempio 1: rimuovere un endpoint</span><span class="sxs-lookup"><span data-stu-id="48203-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="48203-113">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="48203-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="48203-114">Il comando Archivia il profilo locale nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="48203-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="48203-115">Il secondo comando rimuove un endpoint Azure denominato Contoso dal profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="48203-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="48203-116">Questo comando modifica solo l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="48203-116">This command changes only the local object.</span></span>

<span data-ttu-id="48203-117">Il comando finale aggiorna il profilo di Traffic Manager denominato ContosoProfile in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="48203-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="48203-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48203-118">PARAMETERS</span></span>

### <span data-ttu-id="48203-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48203-119">-DefaultProfile</span></span>
<span data-ttu-id="48203-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="48203-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48203-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="48203-121">-EndpointName</span></span>
<span data-ttu-id="48203-122">Specifica il nome dell'endpoint di gestione traffico rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48203-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="48203-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="48203-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="48203-124">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="48203-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="48203-125">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="48203-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="48203-126">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="48203-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="48203-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48203-127">CommonParameters</span></span>
<span data-ttu-id="48203-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48203-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48203-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48203-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48203-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48203-130">INPUTS</span></span>

### <span data-ttu-id="48203-131">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="48203-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="48203-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48203-132">OUTPUTS</span></span>

### <span data-ttu-id="48203-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="48203-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="48203-134">Note</span><span class="sxs-lookup"><span data-stu-id="48203-134">NOTES</span></span>

## <span data-ttu-id="48203-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48203-135">RELATED LINKS</span></span>

[<span data-ttu-id="48203-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="48203-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="48203-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="48203-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="48203-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="48203-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="48203-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="48203-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


