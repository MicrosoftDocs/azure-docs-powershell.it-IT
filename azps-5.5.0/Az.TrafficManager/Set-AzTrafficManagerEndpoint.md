---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182567"
---
# <span data-ttu-id="2159c-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2159c-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="2159c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2159c-102">SYNOPSIS</span></span>
<span data-ttu-id="2159c-103">Aggiorna un endpoint di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="2159c-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="2159c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2159c-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2159c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2159c-105">DESCRIPTION</span></span>
<span data-ttu-id="2159c-106">Il cmdlet **Set-AzTrafficManagerEndpoint** aggiorna un endpoint in Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="2159c-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="2159c-107">Questo cmdlet aggiorna le impostazioni da un oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="2159c-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="2159c-108">È possibile specificare l'oggetto endpoint usando il *parametro TrafficManagerEndpoint* o la pipeline.</span><span class="sxs-lookup"><span data-stu-id="2159c-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="2159c-109">È possibile ottenere un oggetto locale che rappresenta un endpoint usando il cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2159c-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="2159c-110">Modificare l'oggetto in locale e quindi usare **Set-AzTrafficManagerEndpoint** per eseguire il commit delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="2159c-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="2159c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2159c-111">EXAMPLES</span></span>

### <span data-ttu-id="2159c-112">Esempio 1: Aggiornare un endpoint</span><span class="sxs-lookup"><span data-stu-id="2159c-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="2159c-113">Il primo comando ottiene un endpoint di Gestione traffico di Azure usando il cmdlet **Get-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="2159c-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="2159c-114">Il comando archivia l'endpoint in locale nella $TrafficManagerEndpoint variabile.</span><span class="sxs-lookup"><span data-stu-id="2159c-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="2159c-115">Il secondo comando modifica l'endpoint in locale.</span><span class="sxs-lookup"><span data-stu-id="2159c-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="2159c-116">Questo comando modifica il peso del punto finale in 20.</span><span class="sxs-lookup"><span data-stu-id="2159c-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="2159c-117">Il terzo comando aggiorna l'endpoint in Gestione traffico in modo che corrisponda al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2159c-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="2159c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2159c-118">PARAMETERS</span></span>

### <span data-ttu-id="2159c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2159c-119">-DefaultProfile</span></span>
<span data-ttu-id="2159c-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2159c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2159c-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2159c-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="2159c-122">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="2159c-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="2159c-123">Questo cmdlet aggiorna Gestione traffico in modo che corrisponda all'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="2159c-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="2159c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2159c-124">CommonParameters</span></span>
<span data-ttu-id="2159c-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2159c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2159c-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2159c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2159c-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="2159c-127">INPUTS</span></span>

### <span data-ttu-id="2159c-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2159c-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="2159c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2159c-129">OUTPUTS</span></span>

### <span data-ttu-id="2159c-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2159c-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="2159c-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="2159c-131">NOTES</span></span>

## <span data-ttu-id="2159c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2159c-132">RELATED LINKS</span></span>
