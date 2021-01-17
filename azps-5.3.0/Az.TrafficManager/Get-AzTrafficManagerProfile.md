---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382868"
---
# <span data-ttu-id="a25f2-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a25f2-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="a25f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a25f2-102">SYNOPSIS</span></span>
<span data-ttu-id="a25f2-103">Ottiene un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="a25f2-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="a25f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a25f2-104">SYNTAX</span></span>

### <span data-ttu-id="a25f2-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a25f2-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a25f2-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a25f2-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a25f2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a25f2-107">DESCRIPTION</span></span>
<span data-ttu-id="a25f2-108">Il cmdlet **Get-AzTrafficManagerProfile** ottiene un profilo di Azure Traffic Manager e restituisce un oggetto che rappresenta tale profilo.</span><span class="sxs-lookup"><span data-stu-id="a25f2-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="a25f2-109">Specificare un profilo in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a25f2-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="a25f2-110">Puoi modificare l'oggetto localmente e quindi applicare le modifiche al profilo usando il cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a25f2-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="a25f2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a25f2-111">EXAMPLES</span></span>

### <span data-ttu-id="a25f2-112">Esempio 1: ottenere un profilo</span><span class="sxs-lookup"><span data-stu-id="a25f2-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a25f2-113">Questo comando ottiene il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a25f2-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="a25f2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a25f2-114">PARAMETERS</span></span>

### <span data-ttu-id="a25f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25f2-115">-DefaultProfile</span></span>
<span data-ttu-id="a25f2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a25f2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a25f2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a25f2-117">-Name</span></span>
<span data-ttu-id="a25f2-118">Specifica il nome del profilo di Traffic Manager ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a25f2-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a25f2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a25f2-119">-ResourceGroupName</span></span>
<span data-ttu-id="a25f2-120">Specifica il nome di un gruppo di risorse che contiene il profilo di gestione traffico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a25f2-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a25f2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25f2-121">CommonParameters</span></span>
<span data-ttu-id="a25f2-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a25f2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25f2-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a25f2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25f2-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a25f2-124">INPUTS</span></span>

### <span data-ttu-id="a25f2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a25f2-125">System.String</span></span>

## <span data-ttu-id="a25f2-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a25f2-126">OUTPUTS</span></span>

### <span data-ttu-id="a25f2-127">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a25f2-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="a25f2-128">Note</span><span class="sxs-lookup"><span data-stu-id="a25f2-128">NOTES</span></span>

## <span data-ttu-id="a25f2-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a25f2-129">RELATED LINKS</span></span>

[<span data-ttu-id="a25f2-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a25f2-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="a25f2-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a25f2-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="a25f2-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a25f2-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="a25f2-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a25f2-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="a25f2-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a25f2-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


