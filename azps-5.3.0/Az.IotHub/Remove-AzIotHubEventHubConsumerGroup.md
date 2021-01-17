---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 9fa0a9d85dc9c7b1a6cc56c3c329b1810cceaa18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386693"
---
# <span data-ttu-id="5668f-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5668f-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="5668f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5668f-102">SYNOPSIS</span></span>
<span data-ttu-id="5668f-103">Elimina un consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="5668f-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="5668f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5668f-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5668f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5668f-105">DESCRIPTION</span></span>
<span data-ttu-id="5668f-106">Elimina un consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="5668f-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="5668f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5668f-107">EXAMPLES</span></span>

### <span data-ttu-id="5668f-108">Esempio 1 rimuovere eventhub consumergroup dalla eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="5668f-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="5668f-109">Rimuove il consumergroup denominato myconsumergroup dal IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="5668f-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5668f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5668f-110">PARAMETERS</span></span>

### <span data-ttu-id="5668f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5668f-111">-DefaultProfile</span></span>
<span data-ttu-id="5668f-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5668f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5668f-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="5668f-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="5668f-114">EventHub ConsumerGroup nome.</span><span class="sxs-lookup"><span data-stu-id="5668f-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5668f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5668f-115">-Name</span></span>
<span data-ttu-id="5668f-116">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="5668f-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="5668f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5668f-117">-ResourceGroupName</span></span>
<span data-ttu-id="5668f-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5668f-118">Resource Group Name</span></span>

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

### <span data-ttu-id="5668f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5668f-119">-Confirm</span></span>
<span data-ttu-id="5668f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5668f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5668f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5668f-121">-WhatIf</span></span>
<span data-ttu-id="5668f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5668f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5668f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5668f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5668f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5668f-124">CommonParameters</span></span>
<span data-ttu-id="5668f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5668f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5668f-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5668f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5668f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5668f-127">INPUTS</span></span>

### <span data-ttu-id="5668f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5668f-128">System.String</span></span>

## <span data-ttu-id="5668f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5668f-129">OUTPUTS</span></span>

### <span data-ttu-id="5668f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5668f-130">System.String</span></span>

## <span data-ttu-id="5668f-131">Note</span><span class="sxs-lookup"><span data-stu-id="5668f-131">NOTES</span></span>

## <span data-ttu-id="5668f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5668f-132">RELATED LINKS</span></span>
