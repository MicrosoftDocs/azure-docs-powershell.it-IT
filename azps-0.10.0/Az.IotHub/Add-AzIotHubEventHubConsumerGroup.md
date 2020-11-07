---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 2592284be483793ea246d30e95a4c9065fdd6e3c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863146"
---
# <span data-ttu-id="7a1f0-101">Add-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7a1f0-101">Add-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="7a1f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="7a1f0-103">Crea un gruppo di consumi eventhub.</span><span class="sxs-lookup"><span data-stu-id="7a1f0-103">Creates an eventhub consumer group.</span></span>

## <span data-ttu-id="7a1f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a1f0-104">SYNTAX</span></span>

```
Add-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a1f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a1f0-105">DESCRIPTION</span></span>
<span data-ttu-id="7a1f0-106">Crea un gruppo consumer in Eventhub associato al IotHub specificato.</span><span class="sxs-lookup"><span data-stu-id="7a1f0-106">Creates a consumer group in the Eventhub associated with the specified IotHub.</span></span>

## <span data-ttu-id="7a1f0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a1f0-107">EXAMPLES</span></span>

### <span data-ttu-id="7a1f0-108">Esempio 1: aggiungere un gruppo Consumer alla eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="7a1f0-108">Example 1: Add a consumer group to the telemetry eventhub</span></span>
```
PS C:\> Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

<span data-ttu-id="7a1f0-109">Aggiunge una nuova consumergroup denominata "myconsumergroup" al eventhub per gli eventi di telemetria nella iothub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="7a1f0-109">Adds a new consumergroup named "myconsumergroup" to the eventhub for telemetry events in the iothub named "myiothub"</span></span>

## <span data-ttu-id="7a1f0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a1f0-110">PARAMETERS</span></span>

### <span data-ttu-id="7a1f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a1f0-111">-DefaultProfile</span></span>
<span data-ttu-id="7a1f0-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7a1f0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a1f0-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="7a1f0-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="7a1f0-114">Nome del EventHub ConsumerGroup che si vuole aggiungere.</span><span class="sxs-lookup"><span data-stu-id="7a1f0-114">Name of the EventHub ConsumerGroup that you want to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a1f0-115">-Name</span></span>
<span data-ttu-id="7a1f0-116">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="7a1f0-116">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a1f0-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a1f0-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a1f0-118">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f0-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a1f0-119">-Confirm</span></span>
<span data-ttu-id="7a1f0-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a1f0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a1f0-121">-WhatIf</span></span>
<span data-ttu-id="7a1f0-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a1f0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a1f0-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a1f0-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a1f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a1f0-124">CommonParameters</span></span>
<span data-ttu-id="7a1f0-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a1f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a1f0-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a1f0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a1f0-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a1f0-127">INPUTS</span></span>

### <span data-ttu-id="7a1f0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7a1f0-128">System.String</span></span>

## <span data-ttu-id="7a1f0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a1f0-129">OUTPUTS</span></span>

### <span data-ttu-id="7a1f0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7a1f0-130">System.String</span></span>

## <span data-ttu-id="7a1f0-131">Note</span><span class="sxs-lookup"><span data-stu-id="7a1f0-131">NOTES</span></span>

## <span data-ttu-id="7a1f0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a1f0-132">RELATED LINKS</span></span>
