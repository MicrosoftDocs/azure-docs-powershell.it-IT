---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 1dac991645d6f57ba4fe30a82955531b7fdb3f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987264"
---
# <span data-ttu-id="efbf2-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="efbf2-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="efbf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efbf2-102">SYNOPSIS</span></span>
<span data-ttu-id="efbf2-103">Rimuove un endpoint da un oggetto profilo di Gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="efbf2-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="efbf2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efbf2-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efbf2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="efbf2-105">DESCRIPTION</span></span>
<span data-ttu-id="efbf2-106">Il cmdlet **Remove-AzTrafficManagerEndpointConfig** rimuove un endpoint da un oggetto profilo di Gestione traffico Di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="efbf2-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="efbf2-107">È possibile ottenere un profilo usando il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="efbf2-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="efbf2-108">Questo cmdlet opera sull'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="efbf2-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="efbf2-109">Eseguire il commit delle modifiche nel profilo per Gestione traffico usando il cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="efbf2-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="efbf2-110">Per rimuovere un endpoint ed eseguire il commit delle modifiche in una singola operazione, usare il cmdlet Remove-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="efbf2-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="efbf2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efbf2-111">EXAMPLES</span></span>

### <span data-ttu-id="efbf2-112">Esempio 1: Rimuovere un endpoint</span><span class="sxs-lookup"><span data-stu-id="efbf2-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="efbf2-113">Il primo comando ottiene un profilo di Gestione traffico di Azure usando il cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="efbf2-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="efbf2-114">Il comando archivia il profilo locale nella $TrafficManagerProfile variabile.</span><span class="sxs-lookup"><span data-stu-id="efbf2-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="efbf2-115">Il secondo comando rimuove un endpoint di Azure denominato contoso dal profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="efbf2-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="efbf2-116">Questo comando modifica solo l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="efbf2-116">This command changes only the local object.</span></span>

<span data-ttu-id="efbf2-117">Il comando finale aggiorna il profilo di Gestione traffico denominato ContosoProfile in modo che corrisponda al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="efbf2-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="efbf2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efbf2-118">PARAMETERS</span></span>

### <span data-ttu-id="efbf2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efbf2-119">-DefaultProfile</span></span>
<span data-ttu-id="efbf2-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efbf2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efbf2-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="efbf2-121">-EndpointName</span></span>
<span data-ttu-id="efbf2-122">Specifica il nome dell'endpoint di Gestione traffico rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efbf2-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="efbf2-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="efbf2-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="efbf2-124">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="efbf2-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="efbf2-125">Questo cmdlet modifica l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="efbf2-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="efbf2-126">Per ottenere un **oggetto TrafficManagerProfile,** usare il cmdlet Get-AzTrafficManagerProfile TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="efbf2-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="efbf2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efbf2-127">CommonParameters</span></span>
<span data-ttu-id="efbf2-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efbf2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efbf2-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efbf2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efbf2-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="efbf2-130">INPUTS</span></span>

### <span data-ttu-id="efbf2-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="efbf2-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="efbf2-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efbf2-132">OUTPUTS</span></span>

### <span data-ttu-id="efbf2-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="efbf2-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="efbf2-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="efbf2-134">NOTES</span></span>

## <span data-ttu-id="efbf2-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efbf2-135">RELATED LINKS</span></span>

[<span data-ttu-id="efbf2-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="efbf2-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="efbf2-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="efbf2-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="efbf2-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="efbf2-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="efbf2-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="efbf2-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


