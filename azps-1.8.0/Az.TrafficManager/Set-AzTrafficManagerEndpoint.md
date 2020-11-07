---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 31201d607d1b9f0825236fe162bf86028b148193
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676341"
---
# <span data-ttu-id="02d7e-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="02d7e-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="02d7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="02d7e-103">Aggiorna un endpoint di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="02d7e-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="02d7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02d7e-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02d7e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02d7e-105">DESCRIPTION</span></span>
<span data-ttu-id="02d7e-106">Il cmdlet **set-AzTrafficManagerEndpoint** aggiorna un endpoint in Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="02d7e-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="02d7e-107">Questo cmdlet aggiorna le impostazioni da un oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="02d7e-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="02d7e-108">Puoi specificare l'oggetto endpoint usando il parametro *TrafficManagerEndpoint* o usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="02d7e-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="02d7e-109">Puoi ottenere un oggetto local che rappresenta un endpoint usando il cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="02d7e-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="02d7e-110">Modificare l'oggetto localmente e quindi usare **set-AzTrafficManagerEndpoint** per eseguire il commit delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="02d7e-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="02d7e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02d7e-111">EXAMPLES</span></span>

### <span data-ttu-id="02d7e-112">Esempio 1: aggiornare un endpoint</span><span class="sxs-lookup"><span data-stu-id="02d7e-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="02d7e-113">Il primo comando ottiene un endpoint di Azure Traffic Manager usando il cmdlet **Get-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="02d7e-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="02d7e-114">Il comando Archivia l'endpoint localmente nella variabile $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="02d7e-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="02d7e-115">Il secondo comando cambia l'endpoint localmente.</span><span class="sxs-lookup"><span data-stu-id="02d7e-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="02d7e-116">Questo comando imposta il peso dell'endpoint su 20.</span><span class="sxs-lookup"><span data-stu-id="02d7e-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="02d7e-117">Il terzo comando Aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="02d7e-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="02d7e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02d7e-118">PARAMETERS</span></span>

### <span data-ttu-id="02d7e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d7e-119">-DefaultProfile</span></span>
<span data-ttu-id="02d7e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="02d7e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02d7e-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="02d7e-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="02d7e-122">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="02d7e-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="02d7e-123">Questo cmdlet aggiorna Traffic Manager in base a questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="02d7e-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="02d7e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d7e-124">CommonParameters</span></span>
<span data-ttu-id="02d7e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d7e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d7e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d7e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d7e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02d7e-127">INPUTS</span></span>

### <span data-ttu-id="02d7e-128">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="02d7e-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="02d7e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02d7e-129">OUTPUTS</span></span>

### <span data-ttu-id="02d7e-130">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="02d7e-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="02d7e-131">Note</span><span class="sxs-lookup"><span data-stu-id="02d7e-131">NOTES</span></span>

## <span data-ttu-id="02d7e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02d7e-132">RELATED LINKS</span></span>