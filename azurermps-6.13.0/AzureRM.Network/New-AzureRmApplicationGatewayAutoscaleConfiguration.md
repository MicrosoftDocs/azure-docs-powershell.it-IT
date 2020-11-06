---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f19a2e9f1531f6e009561a9d45ecae07d1bb0a3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520171"
---
# <span data-ttu-id="6d493-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d493-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="6d493-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d493-102">SYNOPSIS</span></span>
<span data-ttu-id="6d493-103">Crea una configurazione di scala automatica per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6d493-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d493-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d493-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d493-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d493-105">DESCRIPTION</span></span>
<span data-ttu-id="6d493-106">Il cmdlet **New-AzureRmApplicationGatewayAutoscaleConfiguration** crea la configurazione di scala automatica per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="6d493-106">The **New-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="6d493-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d493-107">EXAMPLES</span></span>

### <span data-ttu-id="6d493-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6d493-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="6d493-109">Il primo comando crea una configurazione di scala automatica con capacità minima 3.</span><span class="sxs-lookup"><span data-stu-id="6d493-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="6d493-110">Il secondo comando crea un gateway dell'applicazione con la configurazione di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="6d493-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="6d493-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d493-111">PARAMETERS</span></span>

### <span data-ttu-id="6d493-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d493-112">-DefaultProfile</span></span>
<span data-ttu-id="6d493-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d493-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d493-114">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="6d493-114">-MinCapacity</span></span>
<span data-ttu-id="6d493-115">Unità di capacità minima che saranno sempre disponibili [e caricate] per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6d493-115">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="6d493-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d493-116">-Confirm</span></span>
<span data-ttu-id="6d493-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d493-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d493-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d493-118">-WhatIf</span></span>
<span data-ttu-id="6d493-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d493-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d493-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d493-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d493-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d493-121">CommonParameters</span></span>
<span data-ttu-id="6d493-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d493-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d493-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d493-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d493-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d493-124">INPUTS</span></span>

### <span data-ttu-id="6d493-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6d493-125">None</span></span>

## <span data-ttu-id="6d493-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d493-126">OUTPUTS</span></span>

### <span data-ttu-id="6d493-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d493-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="6d493-128">Note</span><span class="sxs-lookup"><span data-stu-id="6d493-128">NOTES</span></span>

## <span data-ttu-id="6d493-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d493-129">RELATED LINKS</span></span>
