---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: f7ac75789e4020d3d0e645e5dac8ef2430795eb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517279"
---
# <span data-ttu-id="cca13-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cca13-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="cca13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cca13-102">SYNOPSIS</span></span>
<span data-ttu-id="cca13-103">Abilita un profilo di Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="cca13-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cca13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cca13-104">SYNTAX</span></span>

### <span data-ttu-id="cca13-105">Campi</span><span class="sxs-lookup"><span data-stu-id="cca13-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cca13-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="cca13-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cca13-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cca13-107">DESCRIPTION</span></span>
<span data-ttu-id="cca13-108">Il cmdlet **Enable-AzureRmTrafficManagerProfile** Abilita un profilo di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="cca13-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="cca13-109">Puoi specificare l'oggetto profile usando la pipeline o come valore di parametro.</span><span class="sxs-lookup"><span data-stu-id="cca13-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="cca13-110">In alternativa, puoi specificare il profilo usando i parametri *Name* e *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="cca13-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="cca13-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cca13-111">EXAMPLES</span></span>

### <span data-ttu-id="cca13-112">Esempio 1: abilitare un profilo specificato per nome</span><span class="sxs-lookup"><span data-stu-id="cca13-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="cca13-113">Questo comando consente di abilitare il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cca13-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="cca13-114">Esempio 2: abilitare un profilo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="cca13-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="cca13-115">Questo comando ottiene il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cca13-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="cca13-116">Il comando passa quindi il profilo al cmdlet **Enable-AzureRmTrafficManagerProfile** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="cca13-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cca13-117">Questo cmdlet abilita tale profilo.</span><span class="sxs-lookup"><span data-stu-id="cca13-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="cca13-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cca13-118">PARAMETERS</span></span>

### <span data-ttu-id="cca13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca13-119">-DefaultProfile</span></span>
<span data-ttu-id="cca13-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cca13-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cca13-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="cca13-121">-Name</span></span>
<span data-ttu-id="cca13-122">Specifica il nome del profilo di Traffic Manager attivato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cca13-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca13-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cca13-123">-ResourceGroupName</span></span>
<span data-ttu-id="cca13-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cca13-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cca13-125">Questo cmdlet Abilita un profilo di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="cca13-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca13-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cca13-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="cca13-127">Specifica un oggetto **TrafficManagerProfile** da abilitare.</span><span class="sxs-lookup"><span data-stu-id="cca13-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="cca13-128">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="cca13-128">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cca13-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca13-129">CommonParameters</span></span>
<span data-ttu-id="cca13-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca13-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca13-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cca13-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca13-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cca13-132">INPUTS</span></span>

### <span data-ttu-id="cca13-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cca13-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="cca13-134">Questo cmdlet accetta un oggetto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="cca13-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="cca13-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cca13-135">OUTPUTS</span></span>

### <span data-ttu-id="cca13-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cca13-136">System.Boolean</span></span>

## <span data-ttu-id="cca13-137">Note</span><span class="sxs-lookup"><span data-stu-id="cca13-137">NOTES</span></span>

## <span data-ttu-id="cca13-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cca13-138">RELATED LINKS</span></span>

[<span data-ttu-id="cca13-139">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cca13-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cca13-140">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cca13-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cca13-141">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cca13-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cca13-142">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cca13-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cca13-143">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cca13-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


