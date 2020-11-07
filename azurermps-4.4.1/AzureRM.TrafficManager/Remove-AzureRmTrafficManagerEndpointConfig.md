---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4f936569b5a3c7b3ba63a471aedd6828ef6f36d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685512"
---
# <span data-ttu-id="6c617-101">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6c617-101">Remove-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="6c617-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c617-102">SYNOPSIS</span></span>
<span data-ttu-id="6c617-103">Rimuove un endpoint da un oggetto profilo di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="6c617-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c617-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c617-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c617-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c617-105">DESCRIPTION</span></span>
<span data-ttu-id="6c617-106">Il cmdlet **Remove-AzureRmTrafficManagerEndpointConfig** rimuove un endpoint da un oggetto profilo di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="6c617-106">The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="6c617-107">Puoi ottenere un profilo usando il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6c617-107">You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="6c617-108">Questo cmdlet opera nell'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="6c617-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="6c617-109">Eseguire il commit delle modifiche apportate al profilo per Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6c617-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="6c617-110">Per rimuovere un endpoint e eseguire il commit delle modifiche in una singola operazione, usare il cmdlet Remove-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6c617-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="6c617-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c617-111">EXAMPLES</span></span>

### <span data-ttu-id="6c617-112">Esempio 1: rimuovere un endpoint</span><span class="sxs-lookup"><span data-stu-id="6c617-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="6c617-113">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="6c617-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="6c617-114">Il comando Archivia il profilo locale nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6c617-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="6c617-115">Il secondo comando rimuove un endpoint Azure denominato Contoso dal profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6c617-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="6c617-116">Questo comando modifica solo l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="6c617-116">This command changes only the local object.</span></span>

<span data-ttu-id="6c617-117">Il comando finale aggiorna il profilo di Traffic Manager denominato ContosoProfile in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6c617-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="6c617-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c617-118">PARAMETERS</span></span>

### <span data-ttu-id="6c617-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6c617-119">-EndpointName</span></span>
<span data-ttu-id="6c617-120">Specifica il nome dell'endpoint di gestione traffico rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c617-120">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6c617-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6c617-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="6c617-122">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="6c617-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="6c617-123">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="6c617-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="6c617-124">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6c617-124">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="6c617-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c617-125">-DefaultProfile</span></span>
<span data-ttu-id="6c617-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c617-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c617-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c617-127">CommonParameters</span></span>
<span data-ttu-id="6c617-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c617-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c617-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c617-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c617-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c617-130">INPUTS</span></span>

### <span data-ttu-id="6c617-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6c617-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="6c617-132">Questo cmdlet accetta un oggetto **TrafficManagerProfile** per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c617-132">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="6c617-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c617-133">OUTPUTS</span></span>

### <span data-ttu-id="6c617-134">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6c617-134">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="6c617-135">Questo cmdlet restituisce un oggetto TrafficManagerProfile modificato.</span><span class="sxs-lookup"><span data-stu-id="6c617-135">This cmdlet returns a modified TrafficManagerProfile object.</span></span>

## <span data-ttu-id="6c617-136">Note</span><span class="sxs-lookup"><span data-stu-id="6c617-136">NOTES</span></span>

## <span data-ttu-id="6c617-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c617-137">RELATED LINKS</span></span>

[<span data-ttu-id="6c617-138">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6c617-138">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="6c617-139">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6c617-139">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="6c617-140">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c617-140">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="6c617-141">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6c617-141">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

