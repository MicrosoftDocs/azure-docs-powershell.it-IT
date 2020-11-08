---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191400"
---
# <span data-ttu-id="5f957-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5f957-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="5f957-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f957-102">SYNOPSIS</span></span>
<span data-ttu-id="5f957-103">Aggiorna un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="5f957-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="5f957-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f957-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f957-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f957-105">DESCRIPTION</span></span>
<span data-ttu-id="5f957-106">Il cmdlet **set-AzTrafficManagerProfile** aggiorna un profilo di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="5f957-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="5f957-107">Questo cmdlet aggiorna le impostazioni del profilo da un oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="5f957-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="5f957-108">Puoi specificare l'oggetto profile usando il parametro *TrafficManagerProfile* o usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f957-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="5f957-109">Puoi ottenere un oggetto locale che rappresenta un profilo usando il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5f957-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="5f957-110">Modificare l'oggetto localmente e quindi usare **set-AzTrafficManagerProfile** per eseguire il commit delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="5f957-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="5f957-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f957-111">EXAMPLES</span></span>

### <span data-ttu-id="5f957-112">Esempio 1: aggiornare un profilo</span><span class="sxs-lookup"><span data-stu-id="5f957-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="5f957-113">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5f957-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="5f957-114">Il comando Archivia il profilo localmente nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5f957-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="5f957-115">Il secondo comando cambia il profilo localmente.</span><span class="sxs-lookup"><span data-stu-id="5f957-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="5f957-116">Questo comando Disabilita il profilo.</span><span class="sxs-lookup"><span data-stu-id="5f957-116">This command disables the profile.</span></span>

<span data-ttu-id="5f957-117">Il terzo comando Aggiorna il profilo di Traffic Manager denominato ContosoProfile in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5f957-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="5f957-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f957-118">PARAMETERS</span></span>

### <span data-ttu-id="5f957-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f957-119">-DefaultProfile</span></span>
<span data-ttu-id="5f957-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f957-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f957-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5f957-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="5f957-122">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="5f957-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="5f957-123">Questo cmdlet aggiorna Traffic Manager in base a questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="5f957-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="5f957-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f957-124">CommonParameters</span></span>
<span data-ttu-id="5f957-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f957-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f957-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f957-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f957-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f957-127">INPUTS</span></span>

### <span data-ttu-id="5f957-128">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5f957-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5f957-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f957-129">OUTPUTS</span></span>

### <span data-ttu-id="5f957-130">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5f957-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5f957-131">Note</span><span class="sxs-lookup"><span data-stu-id="5f957-131">NOTES</span></span>

## <span data-ttu-id="5f957-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f957-132">RELATED LINKS</span></span>

[<span data-ttu-id="5f957-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="5f957-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="5f957-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5f957-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="5f957-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5f957-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="5f957-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="5f957-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="5f957-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5f957-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

