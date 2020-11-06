---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: 099088bb560606990baa4f1774d8f46c5f68f04b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512988"
---
# <span data-ttu-id="8d407-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="8d407-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="8d407-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8d407-102">SYNOPSIS</span></span>
<span data-ttu-id="8d407-103">Crea un nuovo argomento di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="8d407-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d407-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d407-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-EnableSubscriptionPartitioning <Boolean>]
 [-FilteringMessagesBeforePublishing <Boolean>] [-IsAnonymousAccessible <Boolean>] [-IsExpress <Boolean>]
 [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>] [-SupportOrdering <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d407-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d407-105">DESCRIPTION</span></span>
<span data-ttu-id="8d407-106">Il cmdlet **New-AzureRmServiceBusTopic** crea un nuovo argomento Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="8d407-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="8d407-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d407-107">EXAMPLES</span></span>

### <span data-ttu-id="8d407-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8d407-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="8d407-109">Crea un nuovo argomento di Service Bus `SB-Topic_exampl1` nello spazio dei nomi Service Bus specificato `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="8d407-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="8d407-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8d407-110">PARAMETERS</span></span>

### <span data-ttu-id="8d407-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="8d407-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="8d407-112">Specifica l'intervallo di inattività [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) dopo il quale l'argomento viene eliminato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8d407-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="8d407-113">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="8d407-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="8d407-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="8d407-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="8d407-115">Specifica la durata dopo la quale il messaggio scade, a partire da quando il messaggio viene inviato a Service Bus.</span><span class="sxs-lookup"><span data-stu-id="8d407-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

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

### <span data-ttu-id="8d407-116">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="8d407-116">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="8d407-117">Specifica la struttura [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) che definisce la durata della cronologia dei rilevamenti duplicati.</span><span class="sxs-lookup"><span data-stu-id="8d407-117">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="8d407-118">Il valore predefinito è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="8d407-118">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="8d407-119">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="8d407-119">-EnableBatchedOperations</span></span>
<span data-ttu-id="8d407-120">Indica se le operazioni in batch sul lato server sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="8d407-120">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="8d407-121">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="8d407-121">-EnableExpress</span></span>
<span data-ttu-id="8d407-122">Indica se le entità espresse sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="8d407-122">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="8d407-123">Una coda espressa contiene temporaneamente un messaggio in memoria prima di scriverlo nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="8d407-123">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="8d407-124">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="8d407-124">-EnablePartitioning</span></span>
<span data-ttu-id="8d407-125">Specifica se abilitare l'argomento da partizionare in più intermediari dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="8d407-125">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

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

### <span data-ttu-id="8d407-126">-EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="8d407-126">-EnableSubscriptionPartitioning</span></span>
<span data-ttu-id="8d407-127">Specifica se abilitare il partizionamento della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8d407-127">Specifies whether to enable subscription partitioning.</span></span>

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

### <span data-ttu-id="8d407-128">-FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="8d407-128">-FilteringMessagesBeforePublishing</span></span>
<span data-ttu-id="8d407-129">Indica se il filtro è abilitato per i messaggi prima della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="8d407-129">Indicates whether filtering is enabled for messages before publishing.</span></span>

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

### <span data-ttu-id="8d407-130">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="8d407-130">-IsAnonymousAccessible</span></span>
<span data-ttu-id="8d407-131">Indica se il messaggio consente l'accesso anonimo.</span><span class="sxs-lookup"><span data-stu-id="8d407-131">Indicates whether the message allows anonymous access.</span></span>

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

### <span data-ttu-id="8d407-132">-Imexpress</span><span class="sxs-lookup"><span data-stu-id="8d407-132">-IsExpress</span></span>
<span data-ttu-id="8d407-133">Indica se l'argomento è abilitato Express.</span><span class="sxs-lookup"><span data-stu-id="8d407-133">Indicates whether the topic is express enabled.</span></span>

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

### <span data-ttu-id="8d407-134">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="8d407-134">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="8d407-135">Le dimensioni massime dell'argomento in megabyte, ovvero le dimensioni della memoria allocata per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="8d407-135">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

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

### <span data-ttu-id="8d407-136">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="8d407-136">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="8d407-137">Indica se l'argomento richiede il rilevamento della duplicazione.</span><span class="sxs-lookup"><span data-stu-id="8d407-137">Indicates whether the topic requires duplication detection.</span></span>

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

### <span data-ttu-id="8d407-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="8d407-138">-SizeInBytes</span></span>
<span data-ttu-id="8d407-139">Specifica le dimensioni dell'argomento in byte.</span><span class="sxs-lookup"><span data-stu-id="8d407-139">Specifies the size of the topic in bytes.</span></span>

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

### <span data-ttu-id="8d407-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="8d407-140">-SupportOrdering</span></span>
<span data-ttu-id="8d407-141">Indica se l'argomento supporta l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="8d407-141">Indicates whether the topic supports ordering.</span></span>

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

### <span data-ttu-id="8d407-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8d407-142">-Confirm</span></span>
<span data-ttu-id="8d407-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d407-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d407-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d407-144">-WhatIf</span></span>
<span data-ttu-id="8d407-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d407-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d407-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d407-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d407-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d407-147">-DefaultProfile</span></span>
<span data-ttu-id="8d407-148">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d407-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d407-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d407-149">-Name</span></span>
<span data-ttu-id="8d407-150">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="8d407-150">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d407-151">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8d407-151">-Namespace</span></span>
<span data-ttu-id="8d407-152">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8d407-152">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d407-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d407-153">-ResourceGroupName</span></span>
<span data-ttu-id="8d407-154">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8d407-154">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d407-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d407-155">CommonParameters</span></span>
<span data-ttu-id="8d407-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d407-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d407-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d407-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d407-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8d407-158">INPUTS</span></span>

### <span data-ttu-id="8d407-159">System. String</span><span class="sxs-lookup"><span data-stu-id="8d407-159">System.String</span></span>
<span data-ttu-id="8d407-160">System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="8d407-160">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="8d407-161">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8d407-161">-ResourceGroup</span></span>
 <span data-ttu-id="8d407-162">System. String</span><span class="sxs-lookup"><span data-stu-id="8d407-162">System.String</span></span>

### <span data-ttu-id="8d407-163">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8d407-163">-NamespaceName</span></span>
 <span data-ttu-id="8d407-164">System. String</span><span class="sxs-lookup"><span data-stu-id="8d407-164">System.String</span></span>

### <span data-ttu-id="8d407-165">-TopicName</span><span class="sxs-lookup"><span data-stu-id="8d407-165">-TopicName</span></span>
 <span data-ttu-id="8d407-166">System. String</span><span class="sxs-lookup"><span data-stu-id="8d407-166">System.String</span></span>

### <span data-ttu-id="8d407-167">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="8d407-167">-EnablePartitioning</span></span>
 <span data-ttu-id="8d407-168">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="8d407-168">System.Boolean?</span></span>

## <span data-ttu-id="8d407-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d407-169">OUTPUTS</span></span>

### <span data-ttu-id="8d407-170">Microsoft. Azure. Commands. ServiceBus. Models. TopicAttributes</span><span class="sxs-lookup"><span data-stu-id="8d407-170">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="8d407-171">Nome: SB-Topic_exampl1 posizione: ID ovest degli Stati Uniti:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 tipo: Microsoft. ServiceBus/topic AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:42 AM CountDetails: DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: true EnableExpress: false EnablePartitioning: true EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: false IsAnonymousAccessible: false Express: false MaxSizeInMegabytes: 16384 RequiresDuplicateDetection: false SizeInBytes: 0 status: Active SubscriptionCount: SupportOrdering: false UpdatedAt: 1/20/2017 3:16:43 AM</span><span class="sxs-lookup"><span data-stu-id="8d407-171">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:42 AM CountDetails                        : DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="8d407-172">Note</span><span class="sxs-lookup"><span data-stu-id="8d407-172">NOTES</span></span>

## <span data-ttu-id="8d407-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d407-173">RELATED LINKS</span></span>

