---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: b326f7228a60f7549fc6dcd227b9bad947f22add
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521227"
---
# <span data-ttu-id="b0572-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b0572-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b0572-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0572-102">SYNOPSIS</span></span>
<span data-ttu-id="b0572-103">Elimina un consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="b0572-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0572-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0572-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0572-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0572-105">DESCRIPTION</span></span>
<span data-ttu-id="b0572-106">Elimina un consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="b0572-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="b0572-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0572-107">EXAMPLES</span></span>

### <span data-ttu-id="b0572-108">Esempio 1 rimuovere eventhub consumergroup dalla eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="b0572-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="b0572-109">Rimuove il consumergroup denominato myconsumergroup dal IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b0572-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b0572-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0572-110">PARAMETERS</span></span>

### <span data-ttu-id="b0572-111">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="b0572-111">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="b0572-112">EventHub ConsumerGroup nome.</span><span class="sxs-lookup"><span data-stu-id="b0572-112">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0572-113">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="b0572-113">-EventHubEndpointName</span></span>
<span data-ttu-id="b0572-114">Nome dell'endpoint EventHub.</span><span class="sxs-lookup"><span data-stu-id="b0572-114">EventHub Endpoint Name.</span></span>
<span data-ttu-id="b0572-115">Eventi di valori possibili, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="b0572-115">Possible values events, operationsMonitoringEvents</span></span>

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

### <span data-ttu-id="b0572-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0572-116">-Name</span></span>
<span data-ttu-id="b0572-117">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="b0572-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="b0572-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0572-118">-ResourceGroupName</span></span>
<span data-ttu-id="b0572-119">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b0572-119">Resource Group Name</span></span>

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

### <span data-ttu-id="b0572-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0572-120">-Confirm</span></span>
<span data-ttu-id="b0572-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0572-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0572-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0572-122">-WhatIf</span></span>
<span data-ttu-id="b0572-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0572-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0572-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0572-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0572-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0572-125">-DefaultProfile</span></span>
<span data-ttu-id="b0572-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0572-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0572-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0572-127">CommonParameters</span></span>
<span data-ttu-id="b0572-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0572-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0572-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0572-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0572-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0572-130">INPUTS</span></span>

### <span data-ttu-id="b0572-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b0572-131">System.String</span></span>

## <span data-ttu-id="b0572-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0572-132">OUTPUTS</span></span>

### <span data-ttu-id="b0572-133">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b0572-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b0572-134">Note</span><span class="sxs-lookup"><span data-stu-id="b0572-134">NOTES</span></span>

## <span data-ttu-id="b0572-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0572-135">RELATED LINKS</span></span>

