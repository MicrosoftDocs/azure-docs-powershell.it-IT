---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182559"
---
# <span data-ttu-id="2f653-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2f653-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="2f653-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f653-102">SYNOPSIS</span></span>
<span data-ttu-id="2f653-103">Aggiorna un profilo di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="2f653-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="2f653-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f653-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f653-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2f653-105">DESCRIPTION</span></span>
<span data-ttu-id="2f653-106">Il cmdlet **Set-AzTrafficManagerProfile** aggiorna un profilo di Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="2f653-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="2f653-107">Questo cmdlet aggiorna le impostazioni del profilo da un oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="2f653-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="2f653-108">È possibile specificare l'oggetto profilo usando il *parametro TrafficManagerProfile* o la pipeline.</span><span class="sxs-lookup"><span data-stu-id="2f653-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="2f653-109">È possibile ottenere un oggetto locale che rappresenta un profilo usando il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2f653-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="2f653-110">Modificare l'oggetto in locale e quindi usare **Set-AzTrafficManagerProfile** per eseguire il commit delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="2f653-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="2f653-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f653-111">EXAMPLES</span></span>

### <span data-ttu-id="2f653-112">Esempio 1: Aggiornare un profilo</span><span class="sxs-lookup"><span data-stu-id="2f653-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="2f653-113">Il primo comando ottiene un profilo di Gestione traffico di Azure usando il cmdlet Get-AzTrafficManagerProfile Azure.</span><span class="sxs-lookup"><span data-stu-id="2f653-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="2f653-114">Il comando archivia il profilo in locale nella $TrafficManagerProfile variabile.</span><span class="sxs-lookup"><span data-stu-id="2f653-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="2f653-115">Il secondo comando modifica il profilo in locale.</span><span class="sxs-lookup"><span data-stu-id="2f653-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="2f653-116">Questo comando disabilita il profilo.</span><span class="sxs-lookup"><span data-stu-id="2f653-116">This command disables the profile.</span></span>

<span data-ttu-id="2f653-117">Il terzo comando aggiorna il profilo di Gestione traffico denominato ContosoProfile in modo che corrisponda al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2f653-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="2f653-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f653-118">PARAMETERS</span></span>

### <span data-ttu-id="2f653-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f653-119">-DefaultProfile</span></span>
<span data-ttu-id="2f653-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f653-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f653-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2f653-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="2f653-122">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="2f653-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="2f653-123">Questo cmdlet aggiorna Gestione traffico in modo che corrisponda all'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="2f653-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="2f653-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f653-124">CommonParameters</span></span>
<span data-ttu-id="2f653-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f653-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f653-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f653-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f653-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="2f653-127">INPUTS</span></span>

### <span data-ttu-id="2f653-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2f653-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="2f653-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f653-129">OUTPUTS</span></span>

### <span data-ttu-id="2f653-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2f653-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="2f653-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="2f653-131">NOTES</span></span>

## <span data-ttu-id="2f653-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f653-132">RELATED LINKS</span></span>

[<span data-ttu-id="2f653-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2f653-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="2f653-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2f653-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="2f653-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2f653-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="2f653-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2f653-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="2f653-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2f653-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


