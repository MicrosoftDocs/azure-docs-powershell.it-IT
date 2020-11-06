---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 1ca390eb8c99ad991f5a15c6a3959d366ae5f983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511676"
---
# <span data-ttu-id="c2de7-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2de7-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="c2de7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2de7-102">SYNOPSIS</span></span>
<span data-ttu-id="c2de7-103">Rimuove la configurazione di scala automatica da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c2de7-103">Removes Autoscale Configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2de7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2de7-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2de7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2de7-105">DESCRIPTION</span></span>
<span data-ttu-id="c2de7-106">Il cmdlet **Remove-AzureRmApplicationGatewayAutoscaleConfiguration** rimuove la configurazione di scala automatica da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c2de7-106">The **Remove-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="c2de7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2de7-107">EXAMPLES</span></span>

### <span data-ttu-id="c2de7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2de7-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="c2de7-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="c2de7-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="c2de7-110">Il secondo comando rimuove la configurazione di scala automatica dal gateway applicationg.</span><span class="sxs-lookup"><span data-stu-id="c2de7-110">The second command removes the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="c2de7-111">Il terzo comando Aggiorna il gateway dell'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="c2de7-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="c2de7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2de7-112">PARAMETERS</span></span>

### <span data-ttu-id="c2de7-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2de7-113">-ApplicationGateway</span></span>
<span data-ttu-id="c2de7-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2de7-114">The applicationGateway</span></span>

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

### <span data-ttu-id="c2de7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2de7-115">-DefaultProfile</span></span>
<span data-ttu-id="c2de7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2de7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2de7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c2de7-117">-Force</span></span>
<span data-ttu-id="c2de7-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c2de7-118">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2de7-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2de7-119">-Confirm</span></span>
<span data-ttu-id="c2de7-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2de7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2de7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2de7-121">-WhatIf</span></span>
<span data-ttu-id="c2de7-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2de7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2de7-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2de7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2de7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2de7-124">CommonParameters</span></span>
<span data-ttu-id="c2de7-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2de7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2de7-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2de7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2de7-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2de7-127">INPUTS</span></span>

### <span data-ttu-id="c2de7-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2de7-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c2de7-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2de7-129">OUTPUTS</span></span>

### <span data-ttu-id="c2de7-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2de7-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c2de7-131">Note</span><span class="sxs-lookup"><span data-stu-id="c2de7-131">NOTES</span></span>

## <span data-ttu-id="c2de7-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2de7-132">RELATED LINKS</span></span>
