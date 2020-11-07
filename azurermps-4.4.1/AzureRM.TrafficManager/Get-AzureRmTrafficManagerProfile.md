---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 6be04cea9e3e73a06cdbb1ee449adaefd4fe803e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688212"
---
# <span data-ttu-id="4ed21-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed21-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="4ed21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ed21-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed21-103">Ottiene un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="4ed21-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ed21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ed21-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ed21-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ed21-105">DESCRIPTION</span></span>
<span data-ttu-id="4ed21-106">Il cmdlet **Get-AzureRmTrafficManagerProfile** ottiene un profilo di Azure Traffic Manager e restituisce un oggetto che rappresenta tale profilo.</span><span class="sxs-lookup"><span data-stu-id="4ed21-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="4ed21-107">Specificare un profilo in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ed21-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="4ed21-108">Puoi modificare l'oggetto localmente e quindi applicare le modifiche al profilo usando il cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="4ed21-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="4ed21-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ed21-109">EXAMPLES</span></span>

### <span data-ttu-id="4ed21-110">Esempio 1: ottenere un profilo</span><span class="sxs-lookup"><span data-stu-id="4ed21-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="4ed21-111">Questo comando ottiene il profilo denominato ContosoProfile in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4ed21-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="4ed21-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ed21-112">PARAMETERS</span></span>

### <span data-ttu-id="4ed21-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ed21-113">-Name</span></span>
<span data-ttu-id="4ed21-114">Specifica il nome del profilo di Traffic Manager ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed21-114">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed21-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ed21-115">-ResourceGroupName</span></span>
<span data-ttu-id="4ed21-116">Specifica il nome di un gruppo di risorse che contiene il profilo di gestione traffico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed21-116">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed21-117">-DefaultProfile</span></span>
<span data-ttu-id="4ed21-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed21-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ed21-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed21-119">CommonParameters</span></span>
<span data-ttu-id="4ed21-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed21-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed21-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed21-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed21-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ed21-122">INPUTS</span></span>

## <span data-ttu-id="4ed21-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ed21-123">OUTPUTS</span></span>

### <span data-ttu-id="4ed21-124">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed21-124">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="4ed21-125">Questo cmdlet restituisce un oggetto **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="4ed21-125">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="4ed21-126">Puoi modificare questo oggetto e quindi applicare le modifiche a Traffic Manager usando **set-AzureRmTrafficManagerProfile**.</span><span class="sxs-lookup"><span data-stu-id="4ed21-126">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="4ed21-127">Note</span><span class="sxs-lookup"><span data-stu-id="4ed21-127">NOTES</span></span>

## <span data-ttu-id="4ed21-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ed21-128">RELATED LINKS</span></span>

[<span data-ttu-id="4ed21-129">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed21-129">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="4ed21-130">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed21-130">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="4ed21-131">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed21-131">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="4ed21-132">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed21-132">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="4ed21-133">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4ed21-133">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


