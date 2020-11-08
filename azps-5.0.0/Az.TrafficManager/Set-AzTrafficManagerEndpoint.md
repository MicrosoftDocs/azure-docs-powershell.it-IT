---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203398"
---
# <span data-ttu-id="b7413-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7413-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="b7413-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7413-102">SYNOPSIS</span></span>
<span data-ttu-id="b7413-103">Aggiorna un endpoint di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="b7413-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="b7413-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7413-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7413-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7413-105">DESCRIPTION</span></span>
<span data-ttu-id="b7413-106">Il cmdlet **set-AzTrafficManagerEndpoint** aggiorna un endpoint in Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="b7413-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="b7413-107">Questo cmdlet aggiorna le impostazioni da un oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="b7413-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="b7413-108">Puoi specificare l'oggetto endpoint usando il parametro *TrafficManagerEndpoint* o usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="b7413-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="b7413-109">Puoi ottenere un oggetto local che rappresenta un endpoint usando il cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b7413-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="b7413-110">Modificare l'oggetto localmente e quindi usare **set-AzTrafficManagerEndpoint** per eseguire il commit delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="b7413-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="b7413-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7413-111">EXAMPLES</span></span>

### <span data-ttu-id="b7413-112">Esempio 1: aggiornare un endpoint</span><span class="sxs-lookup"><span data-stu-id="b7413-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="b7413-113">Il primo comando ottiene un endpoint di Azure Traffic Manager usando il cmdlet **Get-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="b7413-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="b7413-114">Il comando Archivia l'endpoint localmente nella variabile $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b7413-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="b7413-115">Il secondo comando cambia l'endpoint localmente.</span><span class="sxs-lookup"><span data-stu-id="b7413-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="b7413-116">Questo comando imposta il peso dell'endpoint su 20.</span><span class="sxs-lookup"><span data-stu-id="b7413-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="b7413-117">Il terzo comando Aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b7413-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="b7413-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7413-118">PARAMETERS</span></span>

### <span data-ttu-id="b7413-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7413-119">-DefaultProfile</span></span>
<span data-ttu-id="b7413-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7413-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7413-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7413-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="b7413-122">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="b7413-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="b7413-123">Questo cmdlet aggiorna Traffic Manager in base a questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="b7413-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="b7413-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7413-124">CommonParameters</span></span>
<span data-ttu-id="b7413-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7413-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7413-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7413-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7413-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7413-127">INPUTS</span></span>

### <span data-ttu-id="b7413-128">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7413-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="b7413-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7413-129">OUTPUTS</span></span>

### <span data-ttu-id="b7413-130">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7413-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="b7413-131">Note</span><span class="sxs-lookup"><span data-stu-id="b7413-131">NOTES</span></span>

## <span data-ttu-id="b7413-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7413-132">RELATED LINKS</span></span>
