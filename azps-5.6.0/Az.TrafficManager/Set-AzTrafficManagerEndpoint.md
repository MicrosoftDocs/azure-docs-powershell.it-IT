---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 8f8ba0297ac0302e50dfdfdc25ddc3941fb10e34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987236"
---
# <span data-ttu-id="dce82-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dce82-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="dce82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dce82-102">SYNOPSIS</span></span>
<span data-ttu-id="dce82-103">Aggiorna un endpoint di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="dce82-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="dce82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dce82-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dce82-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dce82-105">DESCRIPTION</span></span>
<span data-ttu-id="dce82-106">Il cmdlet **Set-AzTrafficManagerEndpoint** aggiorna un endpoint in Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="dce82-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="dce82-107">Questo cmdlet aggiorna le impostazioni da un oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="dce82-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="dce82-108">È possibile specificare l'oggetto endpoint usando il *parametro TrafficManagerEndpoint* o la pipeline.</span><span class="sxs-lookup"><span data-stu-id="dce82-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="dce82-109">È possibile ottenere un oggetto locale che rappresenta un endpoint usando il cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dce82-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="dce82-110">Modificare l'oggetto in locale e quindi usare **Set-AzTrafficManagerEndpoint** per eseguire il commit delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="dce82-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="dce82-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dce82-111">EXAMPLES</span></span>

### <span data-ttu-id="dce82-112">Esempio 1: Aggiornare un endpoint</span><span class="sxs-lookup"><span data-stu-id="dce82-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="dce82-113">Il primo comando ottiene un endpoint di Gestione traffico di Azure usando il cmdlet **Get-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="dce82-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="dce82-114">Il comando archivia l'endpoint in locale nella $TrafficManagerEndpoint variabile.</span><span class="sxs-lookup"><span data-stu-id="dce82-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="dce82-115">Il secondo comando modifica l'endpoint in locale.</span><span class="sxs-lookup"><span data-stu-id="dce82-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="dce82-116">Questo comando modifica il peso del punto finale in 20.</span><span class="sxs-lookup"><span data-stu-id="dce82-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="dce82-117">Il terzo comando aggiorna l'endpoint in Gestione traffico in modo che corrisponda al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dce82-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="dce82-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dce82-118">PARAMETERS</span></span>

### <span data-ttu-id="dce82-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce82-119">-DefaultProfile</span></span>
<span data-ttu-id="dce82-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dce82-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dce82-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dce82-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="dce82-122">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="dce82-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="dce82-123">Questo cmdlet aggiorna Gestione traffico in modo che corrisponda all'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="dce82-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dce82-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce82-124">CommonParameters</span></span>
<span data-ttu-id="dce82-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce82-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce82-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce82-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce82-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="dce82-127">INPUTS</span></span>

### <span data-ttu-id="dce82-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dce82-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="dce82-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dce82-129">OUTPUTS</span></span>

### <span data-ttu-id="dce82-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dce82-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="dce82-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="dce82-131">NOTES</span></span>

## <span data-ttu-id="dce82-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dce82-132">RELATED LINKS</span></span>
