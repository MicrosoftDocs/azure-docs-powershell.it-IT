---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopic.md
ms.openlocfilehash: a79afdbba1293c3340e499387b5df745d8b76228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686300"
---
# <span data-ttu-id="64add-101">New-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="64add-101">New-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="64add-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64add-102">SYNOPSIS</span></span>
<span data-ttu-id="64add-103">Crea un nuovo argomento di Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="64add-103">Creates a new Service Bus topic in  the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64add-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64add-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -EnablePartitioning <Boolean> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DuplicateDetectionHistoryTimeWindow <String>] [-EnableBatchedOperations <Boolean>]
 [-EnableExpress <Boolean>] [-MaxSizeInMegabytes <Int64>] [-RequiresDuplicateDetection <Boolean>]
 [-SupportOrdering <Boolean>] [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64add-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64add-105">DESCRIPTION</span></span>
<span data-ttu-id="64add-106">Il cmdlet **New-AzureRmServiceBusTopic** crea un nuovo argomento Service Bus nello spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="64add-106">The **New-AzureRmServiceBusTopic** cmdlet creates a new Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="64add-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64add-107">EXAMPLES</span></span>

### <span data-ttu-id="64add-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="64add-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -EnablePartitioning $True

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S
                                      B-Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:42 AM
CountDetails                        : 
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 3:16:43 AM

```
<span data-ttu-id="64add-109">Crea un nuovo argomento di Service Bus `SB-Topic_exampl1` nello spazio dei nomi Service Bus specificato `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="64add-109">Creates a new Service Bus topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="64add-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64add-110">PARAMETERS</span></span>

### <span data-ttu-id="64add-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="64add-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="64add-112">Specifica l'intervallo di inattività [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) dopo il quale l'argomento viene eliminato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="64add-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval after which the topic is automatically deleted.</span></span> <span data-ttu-id="64add-113">La durata minima è di 5 minuti.</span><span class="sxs-lookup"><span data-stu-id="64add-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-114">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="64add-114">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="64add-115">Specifica la durata dopo la quale il messaggio scade, a partire da quando il messaggio viene inviato a Service Bus.</span><span class="sxs-lookup"><span data-stu-id="64add-115">Specifies the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64add-116">-DefaultProfile</span></span>
<span data-ttu-id="64add-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64add-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64add-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="64add-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="64add-119">Specifica la struttura [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) che definisce la durata della cronologia dei rilevamenti duplicati.</span><span class="sxs-lookup"><span data-stu-id="64add-119">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) structure that defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="64add-120">Il valore predefinito è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="64add-120">The default value is 10 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="64add-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="64add-122">Indica se le operazioni in batch sul lato server sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="64add-122">Indicates whether server-side batched operations are enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="64add-123">-EnableExpress</span></span>
<span data-ttu-id="64add-124">Indica se le entità espresse sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="64add-124">Indicates whether Express Entities are enabled.</span></span> <span data-ttu-id="64add-125">Una coda espressa contiene temporaneamente un messaggio in memoria prima di scriverlo nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="64add-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="64add-126">-EnablePartitioning</span></span>
<span data-ttu-id="64add-127">Specifica se abilitare l'argomento da partizionare in più intermediari dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="64add-127">Specifies whether to enable the topic to be partitioned across multiple message brokers.</span></span> 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-128">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="64add-128">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="64add-129">Le dimensioni massime dell'argomento in megabyte, ovvero le dimensioni della memoria allocata per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="64add-129">The maximum size of the topic in megabytes, which is the size of memory allocated for the topic.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="64add-130">-Name</span></span>
<span data-ttu-id="64add-131">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="64add-131">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-132">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="64add-132">-Namespace</span></span>
<span data-ttu-id="64add-133">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="64add-133">Namespace Name.</span></span>

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

### <span data-ttu-id="64add-134">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="64add-134">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="64add-135">Indica se l'argomento richiede il rilevamento della duplicazione.</span><span class="sxs-lookup"><span data-stu-id="64add-135">Indicates whether the topic requires duplication detection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64add-136">-ResourceGroupName</span></span>
<span data-ttu-id="64add-137">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="64add-137">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-138">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="64add-138">-SizeInBytes</span></span>
<span data-ttu-id="64add-139">Specifica le dimensioni dell'argomento in byte.</span><span class="sxs-lookup"><span data-stu-id="64add-139">Specifies the size of the topic in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-140">-SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="64add-140">-SupportOrdering</span></span>
<span data-ttu-id="64add-141">Indica se l'argomento supporta l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="64add-141">Indicates whether the topic supports ordering.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64add-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64add-142">-Confirm</span></span>
<span data-ttu-id="64add-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64add-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64add-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64add-144">-WhatIf</span></span>
<span data-ttu-id="64add-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64add-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64add-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64add-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64add-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64add-147">CommonParameters</span></span>
<span data-ttu-id="64add-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64add-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64add-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64add-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64add-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64add-150">INPUTS</span></span>

### <span data-ttu-id="64add-151">System. String</span><span class="sxs-lookup"><span data-stu-id="64add-151">System.String</span></span>
<span data-ttu-id="64add-152">System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="64add-152">System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

### <span data-ttu-id="64add-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="64add-153">-ResourceGroup</span></span>
 <span data-ttu-id="64add-154">System. String</span><span class="sxs-lookup"><span data-stu-id="64add-154">System.String</span></span>

### <span data-ttu-id="64add-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="64add-155">-NamespaceName</span></span>
 <span data-ttu-id="64add-156">System. String</span><span class="sxs-lookup"><span data-stu-id="64add-156">System.String</span></span>

### <span data-ttu-id="64add-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="64add-157">-TopicName</span></span>
 <span data-ttu-id="64add-158">System. String</span><span class="sxs-lookup"><span data-stu-id="64add-158">System.String</span></span>

### <span data-ttu-id="64add-159">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="64add-159">-EnablePartitioning</span></span>
 <span data-ttu-id="64add-160">System. Boolean?</span><span class="sxs-lookup"><span data-stu-id="64add-160">System.Boolean?</span></span>

## <span data-ttu-id="64add-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64add-161">OUTPUTS</span></span>

### <span data-ttu-id="64add-162">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="64add-162">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="64add-163">Note</span><span class="sxs-lookup"><span data-stu-id="64add-163">NOTES</span></span>

## <span data-ttu-id="64add-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64add-164">RELATED LINKS</span></span>

