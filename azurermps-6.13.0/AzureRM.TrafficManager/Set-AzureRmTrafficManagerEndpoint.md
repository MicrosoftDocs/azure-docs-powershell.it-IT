---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: a6a5b9ed5dbf1faa4a2be345039e53bb3daae291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508951"
---
# <span data-ttu-id="cf446-101">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf446-101">Set-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="cf446-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf446-102">SYNOPSIS</span></span>
<span data-ttu-id="cf446-103">Aggiorna un endpoint di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="cf446-103">Updates a Traffic Manager endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf446-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf446-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf446-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf446-105">DESCRIPTION</span></span>
<span data-ttu-id="cf446-106">Il cmdlet **set-AzureRmTrafficManagerEndpoint** aggiorna un endpoint in Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="cf446-106">The **Set-AzureRmTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="cf446-107">Questo cmdlet aggiorna le impostazioni da un oggetto endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="cf446-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="cf446-108">Puoi specificare l'oggetto endpoint usando il parametro *TrafficManagerEndpoint* o usando la pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf446-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="cf446-109">Puoi ottenere un oggetto local che rappresenta un endpoint usando il cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cf446-109">You can obtain a local object that represents an endpoint by using the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="cf446-110">Modificare l'oggetto localmente e quindi usare **set-AzureRmTrafficManagerEndpoint** per eseguire il commit delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="cf446-110">Modify the object locally and then use **Set-AzureRmTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="cf446-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf446-111">EXAMPLES</span></span>

### <span data-ttu-id="cf446-112">Esempio 1: aggiornare un endpoint</span><span class="sxs-lookup"><span data-stu-id="cf446-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="cf446-113">Il primo comando ottiene un endpoint di Azure Traffic Manager usando il cmdlet **Get-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="cf446-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="cf446-114">Il comando Archivia l'endpoint localmente nella variabile $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cf446-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="cf446-115">Il secondo comando cambia l'endpoint localmente.</span><span class="sxs-lookup"><span data-stu-id="cf446-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="cf446-116">Questo comando imposta il peso dell'endpoint su 20.</span><span class="sxs-lookup"><span data-stu-id="cf446-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="cf446-117">Il terzo comando Aggiorna l'endpoint in gestione traffico per corrispondere al valore locale in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cf446-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="cf446-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf446-118">PARAMETERS</span></span>

### <span data-ttu-id="cf446-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf446-119">-DefaultProfile</span></span>
<span data-ttu-id="cf446-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf446-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf446-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf446-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="cf446-122">Specifica un oggetto **TrafficManagerEndpoint** locale.</span><span class="sxs-lookup"><span data-stu-id="cf446-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="cf446-123">Questo cmdlet aggiorna Traffic Manager in base a questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="cf446-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="cf446-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf446-124">CommonParameters</span></span>
<span data-ttu-id="cf446-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf446-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf446-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf446-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf446-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf446-127">INPUTS</span></span>

### <span data-ttu-id="cf446-128">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf446-128">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="cf446-129">Questo cmdlet accetta un oggetto **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="cf446-129">This cmdlet accepts a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="cf446-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf446-130">OUTPUTS</span></span>

### <span data-ttu-id="cf446-131">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf446-131">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="cf446-132">Questo cmdlet restituisce un oggetto **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="cf446-132">This cmdlet returns a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="cf446-133">Note</span><span class="sxs-lookup"><span data-stu-id="cf446-133">NOTES</span></span>

## <span data-ttu-id="cf446-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf446-134">RELATED LINKS</span></span>
