---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 2d7fa9dd9030f1e5878293276a248c2f6718efe5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518632"
---
# <span data-ttu-id="f891b-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f891b-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f891b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f891b-102">SYNOPSIS</span></span>
<span data-ttu-id="f891b-103">Aggiorna la configurazione di un gateway applicazione in scala automatica.</span><span class="sxs-lookup"><span data-stu-id="f891b-103">Updates Autoscale Configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f891b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f891b-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 -MinCapacity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f891b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f891b-105">DESCRIPTION</span></span>
<span data-ttu-id="f891b-106">Il cmdlet **set-AzureRmApplicationGatewayAutoscaleConfiguration** modifica la configurazione di scala automatica esistente di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f891b-106">The **Set-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="f891b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f891b-107">EXAMPLES</span></span>

### <span data-ttu-id="f891b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f891b-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="f891b-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="f891b-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="f891b-110">Il secondo comando Aggiorna la configurazione di scala automatica dal gateway applicationg.</span><span class="sxs-lookup"><span data-stu-id="f891b-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="f891b-111">Il terzo comando Aggiorna il gateway dell'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="f891b-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="f891b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f891b-112">PARAMETERS</span></span>

### <span data-ttu-id="f891b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f891b-113">-ApplicationGateway</span></span>
<span data-ttu-id="f891b-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f891b-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f891b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f891b-115">-DefaultProfile</span></span>
<span data-ttu-id="f891b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f891b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f891b-117">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="f891b-117">-MinCapacity</span></span>
<span data-ttu-id="f891b-118">Portata minima per gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f891b-118">Minimum capcity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f891b-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f891b-119">-Confirm</span></span>
<span data-ttu-id="f891b-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f891b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f891b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f891b-121">-WhatIf</span></span>
<span data-ttu-id="f891b-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f891b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f891b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f891b-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f891b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f891b-124">CommonParameters</span></span>
<span data-ttu-id="f891b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f891b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f891b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f891b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f891b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f891b-127">INPUTS</span></span>

### <span data-ttu-id="f891b-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f891b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f891b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f891b-129">OUTPUTS</span></span>

### <span data-ttu-id="f891b-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f891b-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f891b-131">Note</span><span class="sxs-lookup"><span data-stu-id="f891b-131">NOTES</span></span>

## <span data-ttu-id="f891b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f891b-132">RELATED LINKS</span></span>
