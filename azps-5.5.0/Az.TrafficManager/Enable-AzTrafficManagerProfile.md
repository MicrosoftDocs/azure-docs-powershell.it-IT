---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198255"
---
# <span data-ttu-id="56744-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56744-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="56744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56744-102">SYNOPSIS</span></span>
<span data-ttu-id="56744-103">Abilita un profilo di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="56744-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="56744-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56744-104">SYNTAX</span></span>

### <span data-ttu-id="56744-105">Campi</span><span class="sxs-lookup"><span data-stu-id="56744-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56744-106">Oggetto</span><span class="sxs-lookup"><span data-stu-id="56744-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56744-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56744-107">DESCRIPTION</span></span>
<span data-ttu-id="56744-108">Il cmdlet **Enable-AzTrafficManagerProfile** abilita un profilo di Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="56744-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="56744-109">È possibile specificare l'oggetto profilo usando la pipeline o come valore di parametro.</span><span class="sxs-lookup"><span data-stu-id="56744-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="56744-110">In alternativa, è possibile specificare il profilo usando i parametri *Name* e *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="56744-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="56744-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56744-111">EXAMPLES</span></span>

### <span data-ttu-id="56744-112">Esempio 1: Abilitare un profilo specificato in base al nome</span><span class="sxs-lookup"><span data-stu-id="56744-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="56744-113">Questo comando abilita il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="56744-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="56744-114">Esempio 2: Abilitare un profilo tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="56744-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="56744-115">Questo comando recupera il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="56744-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="56744-116">Il comando passa quindi il profilo al cmdlet **Enable-AzTrafficManagerProfile** usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="56744-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="56744-117">Questo cmdlet abilita il profilo.</span><span class="sxs-lookup"><span data-stu-id="56744-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="56744-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56744-118">PARAMETERS</span></span>

### <span data-ttu-id="56744-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56744-119">-DefaultProfile</span></span>
<span data-ttu-id="56744-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56744-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56744-121">-Name</span><span class="sxs-lookup"><span data-stu-id="56744-121">-Name</span></span>
<span data-ttu-id="56744-122">Specifica il nome del profilo di Gestione traffico che questo cmdlet abilita.</span><span class="sxs-lookup"><span data-stu-id="56744-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="56744-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56744-123">-ResourceGroupName</span></span>
<span data-ttu-id="56744-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56744-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="56744-125">Questo cmdlet abilita un profilo di Gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="56744-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="56744-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56744-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="56744-127">Specifica un **oggetto TrafficManagerProfile** da abilitare.</span><span class="sxs-lookup"><span data-stu-id="56744-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="56744-128">Per ottenere un **oggetto TrafficManagerProfile,** usare il cmdlet Get-AzTrafficManagerProfile TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="56744-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="56744-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56744-129">CommonParameters</span></span>
<span data-ttu-id="56744-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56744-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56744-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56744-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56744-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="56744-132">INPUTS</span></span>

### <span data-ttu-id="56744-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56744-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="56744-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56744-134">OUTPUTS</span></span>

### <span data-ttu-id="56744-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="56744-135">System.Boolean</span></span>

## <span data-ttu-id="56744-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="56744-136">NOTES</span></span>

## <span data-ttu-id="56744-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56744-137">RELATED LINKS</span></span>

[<span data-ttu-id="56744-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56744-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="56744-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56744-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="56744-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56744-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="56744-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56744-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="56744-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56744-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


