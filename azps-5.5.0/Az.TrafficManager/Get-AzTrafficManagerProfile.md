---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198247"
---
# <span data-ttu-id="5c5d4-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c5d4-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="5c5d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5d4-103">Ottiene un profilo di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="5c5d4-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="5c5d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c5d4-104">SYNTAX</span></span>

### <span data-ttu-id="5c5d4-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c5d4-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c5d4-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c5d4-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c5d4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5c5d4-107">DESCRIPTION</span></span>
<span data-ttu-id="5c5d4-108">Il cmdlet **Get-AzTrafficManagerProfile** ottiene un profilo di Gestione traffico di Azure e restituisce un oggetto che rappresenta tale profilo.</span><span class="sxs-lookup"><span data-stu-id="5c5d4-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="5c5d4-109">Specificare un profilo in base al nome e al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5c5d4-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="5c5d4-110">È possibile modificare l'oggetto in locale e quindi applicarvi le modifiche usando il cmdlet Set-AzTrafficManagerProfile></span><span class="sxs-lookup"><span data-stu-id="5c5d4-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="5c5d4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c5d4-111">EXAMPLES</span></span>

### <span data-ttu-id="5c5d4-112">Esempio 1: Ottenere un profilo</span><span class="sxs-lookup"><span data-stu-id="5c5d4-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="5c5d4-113">Questo comando recupera il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5c5d4-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="5c5d4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c5d4-114">PARAMETERS</span></span>

### <span data-ttu-id="5c5d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c5d4-115">-DefaultProfile</span></span>
<span data-ttu-id="5c5d4-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5d4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c5d4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5c5d4-117">-Name</span></span>
<span data-ttu-id="5c5d4-118">Specifica il nome del profilo di Gestione traffico che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c5d4-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c5d4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c5d4-119">-ResourceGroupName</span></span>
<span data-ttu-id="5c5d4-120">Specifica il nome di un gruppo di risorse che contiene il profilo di Gestione traffico che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c5d4-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c5d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5d4-121">CommonParameters</span></span>
<span data-ttu-id="5c5d4-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c5d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5d4-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c5d4-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5d4-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="5c5d4-124">INPUTS</span></span>

### <span data-ttu-id="5c5d4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="5c5d4-125">System.String</span></span>

## <span data-ttu-id="5c5d4-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c5d4-126">OUTPUTS</span></span>

### <span data-ttu-id="5c5d4-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c5d4-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5c5d4-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="5c5d4-128">NOTES</span></span>

## <span data-ttu-id="5c5d4-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c5d4-129">RELATED LINKS</span></span>

[<span data-ttu-id="5c5d4-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c5d4-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="5c5d4-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c5d4-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="5c5d4-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c5d4-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="5c5d4-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c5d4-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="5c5d4-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c5d4-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


