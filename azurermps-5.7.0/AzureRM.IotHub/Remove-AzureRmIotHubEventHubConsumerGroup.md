---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 5f4324ab7a27b711d33042eede5c3b88d38c4511
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512584"
---
# <span data-ttu-id="d93a2-101">Remove-AzureRmIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d93a2-101">Remove-AzureRmIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="d93a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d93a2-102">SYNOPSIS</span></span>
<span data-ttu-id="d93a2-103">Elimina un consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="d93a2-103">Deletes an eventhub consumergroup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d93a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d93a2-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubEndpointName] <String> [-EventHubConsumerGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d93a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d93a2-105">DESCRIPTION</span></span>
<span data-ttu-id="d93a2-106">Elimina un consumergroup eventhub.</span><span class="sxs-lookup"><span data-stu-id="d93a2-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="d93a2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d93a2-107">EXAMPLES</span></span>

### <span data-ttu-id="d93a2-108">Esempio 1 rimuovere eventhub consumergroup dalla eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="d93a2-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzureRmIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName events -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="d93a2-109">Rimuove il consumergroup denominato myconsumergroup dal IotHub denominato "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d93a2-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d93a2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d93a2-110">PARAMETERS</span></span>

### <span data-ttu-id="d93a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d93a2-111">-DefaultProfile</span></span>
<span data-ttu-id="d93a2-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d93a2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93a2-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="d93a2-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="d93a2-114">EventHub ConsumerGroup nome.</span><span class="sxs-lookup"><span data-stu-id="d93a2-114">EventHub ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d93a2-115">-EventHubEndpointName</span><span class="sxs-lookup"><span data-stu-id="d93a2-115">-EventHubEndpointName</span></span>
<span data-ttu-id="d93a2-116">Nome dell'endpoint EventHub.</span><span class="sxs-lookup"><span data-stu-id="d93a2-116">EventHub Endpoint Name.</span></span>
<span data-ttu-id="d93a2-117">Eventi di valori possibili, operationsMonitoringEvents</span><span class="sxs-lookup"><span data-stu-id="d93a2-117">Possible values events, operationsMonitoringEvents</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: events, operationsMonitoringEvents

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93a2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d93a2-118">-Name</span></span>
<span data-ttu-id="d93a2-119">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="d93a2-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d93a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d93a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="d93a2-121">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d93a2-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d93a2-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d93a2-122">-Confirm</span></span>
<span data-ttu-id="d93a2-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d93a2-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93a2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d93a2-124">-WhatIf</span></span>
<span data-ttu-id="d93a2-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d93a2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d93a2-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d93a2-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93a2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93a2-127">CommonParameters</span></span>
<span data-ttu-id="d93a2-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d93a2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93a2-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d93a2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93a2-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d93a2-130">INPUTS</span></span>

### <span data-ttu-id="d93a2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d93a2-131">System.String</span></span>

## <span data-ttu-id="d93a2-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d93a2-132">OUTPUTS</span></span>

### <span data-ttu-id="d93a2-133">System. Collections. Generic. IEnumerable ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d93a2-133">System.Collections.Generic.IEnumerable\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d93a2-134">Note</span><span class="sxs-lookup"><span data-stu-id="d93a2-134">NOTES</span></span>

## <span data-ttu-id="d93a2-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d93a2-135">RELATED LINKS</span></span>

