---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: 1e563126bb57986bed752184340808991f7e2a00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974846"
---
# <span data-ttu-id="114de-101">Remove-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="114de-101">Remove-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="114de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="114de-102">SYNOPSIS</span></span>
<span data-ttu-id="114de-103">Elimina un gruppo consumer eventhub.</span><span class="sxs-lookup"><span data-stu-id="114de-103">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="114de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="114de-104">SYNTAX</span></span>

```
Remove-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-EventHubConsumerGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="114de-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="114de-105">DESCRIPTION</span></span>
<span data-ttu-id="114de-106">Elimina un gruppo consumer eventhub.</span><span class="sxs-lookup"><span data-stu-id="114de-106">Deletes an eventhub consumergroup.</span></span>

## <span data-ttu-id="114de-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="114de-107">EXAMPLES</span></span>

### <span data-ttu-id="114de-108">Esempio 1 Rimuovere il gruppo consumer eventhub dal dashboard di telemetria</span><span class="sxs-lookup"><span data-stu-id="114de-108">Example 1 Remove eventhub consumergroup from the telemetry eventhub</span></span>
```
PS C:\> Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

<span data-ttu-id="114de-109">Rimuove il gruppo di utenti consumer denominato gruppoconsumtore dalla cartella IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="114de-109">Removes the consumergroup named myconsumergroup from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="114de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="114de-110">PARAMETERS</span></span>

### <span data-ttu-id="114de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114de-111">-DefaultProfile</span></span>
<span data-ttu-id="114de-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="114de-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="114de-113">-EventHubConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="114de-113">-EventHubConsumerGroupName</span></span>
<span data-ttu-id="114de-114">Nome ConsumerGroup di EventHub.</span><span class="sxs-lookup"><span data-stu-id="114de-114">EventHub ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="114de-115">-Name</span><span class="sxs-lookup"><span data-stu-id="114de-115">-Name</span></span>
<span data-ttu-id="114de-116">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="114de-116">Name of the IotHub</span></span>

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

### <span data-ttu-id="114de-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="114de-117">-ResourceGroupName</span></span>
<span data-ttu-id="114de-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="114de-118">Resource Group Name</span></span>

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

### <span data-ttu-id="114de-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="114de-119">-Confirm</span></span>
<span data-ttu-id="114de-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="114de-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="114de-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="114de-121">-WhatIf</span></span>
<span data-ttu-id="114de-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="114de-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="114de-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="114de-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="114de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114de-124">CommonParameters</span></span>
<span data-ttu-id="114de-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="114de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114de-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="114de-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114de-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="114de-127">INPUTS</span></span>

### <span data-ttu-id="114de-128">System.String</span><span class="sxs-lookup"><span data-stu-id="114de-128">System.String</span></span>

## <span data-ttu-id="114de-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="114de-129">OUTPUTS</span></span>

### <span data-ttu-id="114de-130">System.String</span><span class="sxs-lookup"><span data-stu-id="114de-130">System.String</span></span>

## <span data-ttu-id="114de-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="114de-131">NOTES</span></span>

## <span data-ttu-id="114de-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="114de-132">RELATED LINKS</span></span>
