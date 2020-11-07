---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 0a2bfe70e986b3ed92cef215cc23245216c0e961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688234"
---
# <span data-ttu-id="02d84-101">New-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="02d84-101">New-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="02d84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02d84-102">SYNOPSIS</span></span>
<span data-ttu-id="02d84-103">Rigenera le stringhe di connessione primarie o secondarie per la coda di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="02d84-103">Regenerates the primary or secondary connection strings for the Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02d84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02d84-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueKey [-ResourceGroup] <String> [-NamespaceName] <String> [-QueueName] <String>
 [-AuthorizationRuleName] <String> [-RegenerateKeys] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02d84-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02d84-105">DESCRIPTION</span></span>
<span data-ttu-id="02d84-106">Il cmdlet **New-AzureRmServiceBusQueueKey** rigenera le stringhe di connessione primarie o secondarie per la regola di autorizzazione e la coda di Service Bus specificata.</span><span class="sxs-lookup"><span data-stu-id="02d84-106">The **New-AzureRmServiceBusQueueKey** cmdlet regenerates the primary or secondary connection strings for the specified Service Bus queue and authorization rule.</span></span>

## <span data-ttu-id="02d84-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02d84-107">EXAMPLES</span></span>

### <span data-ttu-id="02d84-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02d84-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="02d84-109">Rigenera la stringa di connessione primaria per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="02d84-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="02d84-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="02d84-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="02d84-111">Rigenera la stringa di connessione secondaria per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="02d84-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="02d84-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02d84-112">PARAMETERS</span></span>

### <span data-ttu-id="02d84-113">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="02d84-113">-AuthorizationRuleName</span></span>
<span data-ttu-id="02d84-114">Nome della regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="02d84-114">The authorization rule name.</span></span>

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

### <span data-ttu-id="02d84-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="02d84-115">-NamespaceName</span></span>
<span data-ttu-id="02d84-116">Nome dello spazio dei nomi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="02d84-116">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="02d84-117">-QueueName</span><span class="sxs-lookup"><span data-stu-id="02d84-117">-QueueName</span></span>
<span data-ttu-id="02d84-118">Nome della coda di Service Bus.</span><span class="sxs-lookup"><span data-stu-id="02d84-118">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02d84-119">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="02d84-119">-RegenerateKeys</span></span>
<span data-ttu-id="02d84-120">Specifica se rigenerare le chiavi primarie o secondarie.</span><span class="sxs-lookup"><span data-stu-id="02d84-120">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02d84-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="02d84-121">-ResourceGroup</span></span>
<span data-ttu-id="02d84-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="02d84-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="02d84-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="02d84-123">-Confirm</span></span>
<span data-ttu-id="02d84-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02d84-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02d84-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02d84-125">-WhatIf</span></span>
<span data-ttu-id="02d84-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02d84-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02d84-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02d84-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02d84-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d84-128">CommonParameters</span></span>
<span data-ttu-id="02d84-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d84-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d84-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d84-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d84-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02d84-131">INPUTS</span></span>

### <span data-ttu-id="02d84-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="02d84-132">-ResourceGroup</span></span>
 <span data-ttu-id="02d84-133">System. String</span><span class="sxs-lookup"><span data-stu-id="02d84-133">System.String</span></span>
 

### <span data-ttu-id="02d84-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="02d84-134">-NamespaceName</span></span>
 <span data-ttu-id="02d84-135">System. String</span><span class="sxs-lookup"><span data-stu-id="02d84-135">System.String</span></span>
 

### <span data-ttu-id="02d84-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="02d84-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="02d84-137">System. String</span><span class="sxs-lookup"><span data-stu-id="02d84-137">System.String</span></span>
 

### <span data-ttu-id="02d84-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="02d84-138">-QueueName</span></span>
 <span data-ttu-id="02d84-139">System. String</span><span class="sxs-lookup"><span data-stu-id="02d84-139">System.String</span></span>
 

### <span data-ttu-id="02d84-140">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="02d84-140">-RegenerateKeys</span></span>
 <span data-ttu-id="02d84-141">System. String</span><span class="sxs-lookup"><span data-stu-id="02d84-141">System.String</span></span>

## <span data-ttu-id="02d84-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02d84-142">OUTPUTS</span></span>

### <span data-ttu-id="02d84-143">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="02d84-143">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="02d84-144">PrimaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-valore}; EntityPath = SB-Queue_exa mpl1 SecondaryConnectionString: endpoint = SB://SB-Example1.ServiceBus.Windows.NET/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-valore}; EntityPath = SB-Queue_exa mpl1 PrimaryKey: {PrimaryKey value} SecondaryKey: {SecondaryKey value} nome di pagina: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="02d84-144">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_exa mpl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="02d84-145">Note</span><span class="sxs-lookup"><span data-stu-id="02d84-145">NOTES</span></span>

## <span data-ttu-id="02d84-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02d84-146">RELATED LINKS</span></span>

