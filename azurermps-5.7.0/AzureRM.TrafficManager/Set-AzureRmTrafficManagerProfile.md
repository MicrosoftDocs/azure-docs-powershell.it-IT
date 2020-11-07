---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 58811a34a2f3d2b4684813c42723a5cab354a13f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519815"
---
# <span data-ttu-id="cda8e-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cda8e-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="cda8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cda8e-102">SYNOPSIS</span></span>
<span data-ttu-id="cda8e-103">Aggiorna un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="cda8e-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cda8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cda8e-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cda8e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cda8e-105">DESCRIPTION</span></span>
<span data-ttu-id="cda8e-106">Il cmdlet **set-AzureRmTrafficManagerProfile** aggiorna un profilo di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="cda8e-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="cda8e-107">Questo cmdlet aggiorna le impostazioni del profilo da un oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="cda8e-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="cda8e-108">Puoi specificare l'oggetto profile usando il parametro *TrafficManagerProfile* o usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="cda8e-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="cda8e-109">Puoi ottenere un oggetto locale che rappresenta un profilo usando il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="cda8e-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="cda8e-110">Modificare l'oggetto localmente e quindi usare **set-AzureRmTrafficManagerProfile** per eseguire il commit delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="cda8e-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="cda8e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cda8e-111">EXAMPLES</span></span>

### <span data-ttu-id="cda8e-112">Esempio 1: aggiornare un profilo</span><span class="sxs-lookup"><span data-stu-id="cda8e-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="cda8e-113">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="cda8e-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="cda8e-114">Il comando Archivia il profilo localmente nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="cda8e-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="cda8e-115">Il secondo comando cambia il profilo localmente.</span><span class="sxs-lookup"><span data-stu-id="cda8e-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="cda8e-116">Questo comando Disabilita il profilo.</span><span class="sxs-lookup"><span data-stu-id="cda8e-116">This command disables the profile.</span></span>

<span data-ttu-id="cda8e-117">Il terzo comando Aggiorna il profilo di Traffic Manager denominato ContosoProfile in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="cda8e-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="cda8e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cda8e-118">PARAMETERS</span></span>

### <span data-ttu-id="cda8e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda8e-119">-DefaultProfile</span></span>
<span data-ttu-id="cda8e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cda8e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cda8e-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cda8e-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="cda8e-122">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="cda8e-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="cda8e-123">Questo cmdlet aggiorna Traffic Manager in base a questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="cda8e-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cda8e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda8e-124">CommonParameters</span></span>
<span data-ttu-id="cda8e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda8e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda8e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cda8e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda8e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cda8e-127">INPUTS</span></span>

### <span data-ttu-id="cda8e-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cda8e-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="cda8e-129">Questo cmdlet accetta un oggetto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="cda8e-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="cda8e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cda8e-130">OUTPUTS</span></span>

### <span data-ttu-id="cda8e-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cda8e-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="cda8e-132">Questo cmdlet restituisce un oggetto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="cda8e-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="cda8e-133">Note</span><span class="sxs-lookup"><span data-stu-id="cda8e-133">NOTES</span></span>

## <span data-ttu-id="cda8e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cda8e-134">RELATED LINKS</span></span>

[<span data-ttu-id="cda8e-135">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="cda8e-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="cda8e-136">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cda8e-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cda8e-137">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cda8e-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cda8e-138">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="cda8e-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="cda8e-139">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cda8e-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

