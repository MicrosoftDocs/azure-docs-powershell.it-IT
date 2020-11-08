---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202040"
---
# <span data-ttu-id="99275-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="99275-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="99275-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99275-102">SYNOPSIS</span></span>
<span data-ttu-id="99275-103">Crea una configurazione di scala automatica per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="99275-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="99275-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99275-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99275-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99275-105">DESCRIPTION</span></span>
<span data-ttu-id="99275-106">Il cmdlet **New-AzApplicationGatewayAutoscaleConfiguration** crea la configurazione di scala automatica per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="99275-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="99275-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99275-107">EXAMPLES</span></span>

### <span data-ttu-id="99275-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99275-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="99275-109">Il primo comando crea una configurazione di scala automatica con capacità minima 3.</span><span class="sxs-lookup"><span data-stu-id="99275-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="99275-110">Il secondo comando crea un gateway dell'applicazione con la configurazione di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="99275-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="99275-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99275-111">PARAMETERS</span></span>

### <span data-ttu-id="99275-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99275-112">-DefaultProfile</span></span>
<span data-ttu-id="99275-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99275-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99275-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="99275-114">-MaxCapacity</span></span>
<span data-ttu-id="99275-115">Unità di capacità massima che saranno sempre disponibili [e caricate] per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="99275-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99275-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="99275-116">-MinCapacity</span></span>
<span data-ttu-id="99275-117">Unità di capacità minima che saranno sempre disponibili [e caricate] per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="99275-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="99275-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99275-118">-Confirm</span></span>
<span data-ttu-id="99275-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99275-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99275-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99275-120">-WhatIf</span></span>
<span data-ttu-id="99275-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99275-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99275-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99275-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99275-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99275-123">CommonParameters</span></span>
<span data-ttu-id="99275-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99275-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99275-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99275-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99275-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99275-126">INPUTS</span></span>

### <span data-ttu-id="99275-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="99275-127">None</span></span>

## <span data-ttu-id="99275-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99275-128">OUTPUTS</span></span>

### <span data-ttu-id="99275-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="99275-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="99275-130">Note</span><span class="sxs-lookup"><span data-stu-id="99275-130">NOTES</span></span>

## <span data-ttu-id="99275-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99275-131">RELATED LINKS</span></span>

[<span data-ttu-id="99275-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="99275-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="99275-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="99275-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="99275-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="99275-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
