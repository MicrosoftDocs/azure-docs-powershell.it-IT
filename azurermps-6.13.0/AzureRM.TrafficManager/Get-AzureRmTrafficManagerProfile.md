---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 239e0147b1955c59dbe34591f85273f05aa12c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508976"
---
# <span data-ttu-id="f8440-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8440-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="f8440-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8440-102">SYNOPSIS</span></span>
<span data-ttu-id="f8440-103">Ottiene un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="f8440-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8440-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8440-104">SYNTAX</span></span>

### <span data-ttu-id="f8440-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8440-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8440-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8440-106">AccountNameParameterSet</span></span>
```
Get-AzureRmTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8440-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8440-107">DESCRIPTION</span></span>
<span data-ttu-id="f8440-108">Il cmdlet **Get-AzureRmTrafficManagerProfile** ottiene un profilo di Azure Traffic Manager e restituisce un oggetto che rappresenta tale profilo.</span><span class="sxs-lookup"><span data-stu-id="f8440-108">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="f8440-109">Specificare un profilo in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f8440-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="f8440-110">Puoi modificare l'oggetto localmente e quindi applicare le modifiche al profilo usando il cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f8440-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="f8440-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8440-111">EXAMPLES</span></span>

### <span data-ttu-id="f8440-112">Esempio 1: ottenere un profilo</span><span class="sxs-lookup"><span data-stu-id="f8440-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f8440-113">Questo comando ottiene il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f8440-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="f8440-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8440-114">PARAMETERS</span></span>

### <span data-ttu-id="f8440-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8440-115">-DefaultProfile</span></span>
<span data-ttu-id="f8440-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8440-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8440-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8440-117">-Name</span></span>
<span data-ttu-id="f8440-118">Specifica il nome del profilo di Traffic Manager ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8440-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f8440-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8440-119">-ResourceGroupName</span></span>
<span data-ttu-id="f8440-120">Specifica il nome di un gruppo di risorse che contiene il profilo di gestione traffico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8440-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f8440-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8440-121">CommonParameters</span></span>
<span data-ttu-id="f8440-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8440-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8440-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8440-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8440-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8440-124">INPUTS</span></span>

### <span data-ttu-id="f8440-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f8440-125">None</span></span>
<span data-ttu-id="f8440-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f8440-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8440-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8440-127">OUTPUTS</span></span>

### <span data-ttu-id="f8440-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8440-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f8440-129">Questo cmdlet restituisce un oggetto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f8440-129">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f8440-130">Puoi modificare questo oggetto e quindi applicare le modifiche a Traffic Manager usando **set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="f8440-130">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="f8440-131">Note</span><span class="sxs-lookup"><span data-stu-id="f8440-131">NOTES</span></span>

## <span data-ttu-id="f8440-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8440-132">RELATED LINKS</span></span>

[<span data-ttu-id="f8440-133">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8440-133">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f8440-134">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8440-134">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f8440-135">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8440-135">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f8440-136">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8440-136">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f8440-137">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8440-137">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


