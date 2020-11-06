---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 5b88ce6edc92cb6483b8d6df95599fcea854f805
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515743"
---
# <span data-ttu-id="47adb-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="47adb-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="47adb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47adb-102">SYNOPSIS</span></span>
<span data-ttu-id="47adb-103">Elimina il gruppo di utenti hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="47adb-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47adb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47adb-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47adb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47adb-105">DESCRIPTION</span></span>
<span data-ttu-id="47adb-106">Il cmdlet Remove-AzureRmEventHubConsumerGroup rimuove ed Elimina il gruppo di utenti specificato dall'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="47adb-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="47adb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47adb-107">EXAMPLES</span></span>

### <span data-ttu-id="47adb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="47adb-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="47adb-109">Elimina il gruppo Consumer \` MyConsumerGroupName \` dall'hub eventi \` MyEventHubName \` , ambito dello \` \` spazio dei nomi MyNamespace.</span><span class="sxs-lookup"><span data-stu-id="47adb-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="47adb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47adb-110">PARAMETERS</span></span>

### <span data-ttu-id="47adb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47adb-111">-DefaultProfile</span></span>
<span data-ttu-id="47adb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47adb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47adb-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="47adb-113">-EventHub</span></span>
<span data-ttu-id="47adb-114">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="47adb-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47adb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="47adb-115">-Name</span></span>
<span data-ttu-id="47adb-116">Nome ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="47adb-116">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47adb-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="47adb-117">-Namespace</span></span>
<span data-ttu-id="47adb-118">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="47adb-118">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47adb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47adb-119">-ResourceGroupName</span></span>
<span data-ttu-id="47adb-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="47adb-120">Resource Group Name</span></span>

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

### <span data-ttu-id="47adb-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47adb-121">-Confirm</span></span>
<span data-ttu-id="47adb-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47adb-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47adb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47adb-123">-WhatIf</span></span>
<span data-ttu-id="47adb-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47adb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47adb-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47adb-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47adb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47adb-126">CommonParameters</span></span>
<span data-ttu-id="47adb-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47adb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="47adb-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47adb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47adb-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47adb-129">INPUTS</span></span>

### <span data-ttu-id="47adb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="47adb-130">System.String</span></span>


## <span data-ttu-id="47adb-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47adb-131">OUTPUTS</span></span>

### <span data-ttu-id="47adb-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="47adb-132">System.Object</span></span>

## <span data-ttu-id="47adb-133">Note</span><span class="sxs-lookup"><span data-stu-id="47adb-133">NOTES</span></span>

## <span data-ttu-id="47adb-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47adb-134">RELATED LINKS</span></span>
