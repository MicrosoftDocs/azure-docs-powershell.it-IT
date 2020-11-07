---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusTopic.md
ms.openlocfilehash: 8fe78fff4d297233ee322b58c426099f160b2990
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677132"
---
# <span data-ttu-id="6614e-101">New-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="6614e-101">New-AzServiceBusTopic</span></span>

## <span data-ttu-id="6614e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6614e-102">SYNOPSIS</span></span>
<span data-ttu-id="6614e-103">Crea un nuovo argomento di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="6614e-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6614e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6614e-104">SYNTAX</span></span>

```
New-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6614e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6614e-105">DESCRIPTION</span></span>
<span data-ttu-id="6614e-106">Il cmdlet **New-AzServiceBusTopic** crea un nuovo argomento Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="6614e-106">The **New-AzServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6614e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6614e-107">EXAMPLES</span></span>

### <span data-ttu-id="6614e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6614e-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 11:51:24 PM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : False
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : True
UpdatedAt                           : 10/11/2018 11:51:24 PM
```

<span data-ttu-id="6614e-109">Crea un nuovo argomento di Service Bus `SB-Topic_exampl1` nello spazio dei nomi Service Bus specificato `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="6614e-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="6614e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6614e-110">PARAMETERS</span></span>

### <span data-ttu-id="6614e-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="6614e-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="6614e-112">Specifica l'intervallo di inattività [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) dopo il quale l'argomento viene eliminato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6614e-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="6614e-113">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="6614e-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="6614e-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="6614e-115">Specifica la durata dopo la quale il messaggio scade, a partire da quando il messaggio viene inviato a Service Bus.</span><span class="sxs-lookup"><span data-stu-id="6614e-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6614e-116">-DefaultProfile</span></span>
<span data-ttu-id="6614e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6614e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6614e-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="6614e-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="6614e-119">Specifica la struttura [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) che definisce la durata della cronologia dei rilevamenti duplicati.</span><span class="sxs-lookup"><span data-stu-id="6614e-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="6614e-120">Il valore predefinito è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="6614e-120">The default value is 10 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="6614e-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="6614e-122">Indica se le operazioni in batch sul lato server sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="6614e-122">Indicates whether server-side batched operations are enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="6614e-123">-EnableExpress</span></span>
<span data-ttu-id="6614e-124">Indica se le entità espresse sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="6614e-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="6614e-125">Una coda espressa contiene temporaneamente un messaggio in memoria prima di scriverlo nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="6614e-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="6614e-126">-EnablePartitioning</span></span>
<span data-ttu-id="6614e-127">Specifica se abilitare l'argomento da partizionare in più intermediari dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="6614e-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="6614e-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="6614e-129">Le dimensioni massime dell'argomento in megabyte, ovvero le dimensioni della memoria allocata per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="6614e-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="6614e-130">-Name</span></span>
<span data-ttu-id="6614e-131">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="6614e-131">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-132">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6614e-132">-Namespace</span></span>
<span data-ttu-id="6614e-133">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6614e-133">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="6614e-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="6614e-135">Indica se l'argomento richiede il rilevamento della duplicazione.</span><span class="sxs-lookup"><span data-stu-id="6614e-135">Indicates whether the topic requires duplication detection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6614e-136">-ResourceGroupName</span></span>
<span data-ttu-id="6614e-137">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6614e-137">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="6614e-138">-SizeInBytes</span></span>
<span data-ttu-id="6614e-139">Specifica le dimensioni dell'argomento in byte.</span><span class="sxs-lookup"><span data-stu-id="6614e-139">Specifies the size of the topic in bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="6614e-140">-SupportOrdering</span></span>
<span data-ttu-id="6614e-141">Indica se l'argomento supporta l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="6614e-141">Indicates whether the topic supports ordering.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6614e-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6614e-142">-Confirm</span></span>
<span data-ttu-id="6614e-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6614e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6614e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6614e-144">-WhatIf</span></span>
<span data-ttu-id="6614e-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6614e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6614e-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6614e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6614e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6614e-147">CommonParameters</span></span>
<span data-ttu-id="6614e-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6614e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6614e-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6614e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6614e-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6614e-150">INPUTS</span></span>

### <span data-ttu-id="6614e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="6614e-151">System.String</span></span>

### <span data-ttu-id="6614e-152">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6614e-152">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6614e-153">System. Nullable ' 1 [[System. Int64, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6614e-153">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6614e-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6614e-154">OUTPUTS</span></span>

### <span data-ttu-id="6614e-155">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="6614e-155">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="6614e-156">Note</span><span class="sxs-lookup"><span data-stu-id="6614e-156">NOTES</span></span>

## <span data-ttu-id="6614e-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6614e-157">RELATED LINKS</span></span>
