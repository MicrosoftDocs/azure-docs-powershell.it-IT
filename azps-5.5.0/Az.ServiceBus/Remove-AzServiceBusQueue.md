---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: c93f0d8a44a67195d2c901dd581505276b7ae2f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201630"
---
# <span data-ttu-id="9f5a6-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="9f5a6-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="9f5a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f5a6-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5a6-103">Rimuove la coda dallo spazio dei nomi del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="9f5a6-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9f5a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f5a6-104">SYNTAX</span></span>

### <span data-ttu-id="9f5a6-105">QueuePropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9f5a6-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5a6-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9f5a6-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f5a6-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9f5a6-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f5a6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9f5a6-108">DESCRIPTION</span></span>
<span data-ttu-id="9f5a6-109">Il cmdlet **Remove-AzServiceBusQueue** rimuove la coda dallo spazio dei nomi del bus di servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="9f5a6-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9f5a6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f5a6-110">EXAMPLES</span></span>

### <span data-ttu-id="9f5a6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9f5a6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="9f5a6-112">Rimuove la coda del bus di `SB-Queue_exampl1` servizio dallo spazio dei `SB-Example1` nomi.</span><span class="sxs-lookup"><span data-stu-id="9f5a6-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="9f5a6-113">Esempio 2: InputObject - Variabile Using:</span><span class="sxs-lookup"><span data-stu-id="9f5a6-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="9f5a6-114">Rimuove la coda di bus di servizio specificata nel parametro $inputobject for -InputObject</span><span class="sxs-lookup"><span data-stu-id="9f5a6-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="9f5a6-115">Esempio 3: InputObject - Uso di Piping:</span><span class="sxs-lookup"><span data-stu-id="9f5a6-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="9f5a6-116">Esempio 4: ResourceId - Variabile Using:</span><span class="sxs-lookup"><span data-stu-id="9f5a6-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="9f5a6-117">Rimuove la coda di bus di servizio specificata nell'ID ARM servizio in $resourceid/stringa per il parametro -ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f5a6-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="9f5a6-118">Esempio 5: ResourceId - passaggio come stringa:</span><span class="sxs-lookup"><span data-stu-id="9f5a6-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="9f5a6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f5a6-119">PARAMETERS</span></span>

### <span data-ttu-id="9f5a6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f5a6-120">-AsJob</span></span>
<span data-ttu-id="9f5a6-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9f5a6-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5a6-122">-DefaultProfile</span></span>
<span data-ttu-id="9f5a6-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f5a6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f5a6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f5a6-124">-InputObject</span></span>
<span data-ttu-id="9f5a6-125">Oggetto coda bus di servizio</span><span class="sxs-lookup"><span data-stu-id="9f5a6-125">Service Bus Queue Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: QueueInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5a6-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9f5a6-126">-Name</span></span>
<span data-ttu-id="9f5a6-127">Nome coda</span><span class="sxs-lookup"><span data-stu-id="9f5a6-127">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5a6-128">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f5a6-128">-Namespace</span></span>
<span data-ttu-id="9f5a6-129">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f5a6-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5a6-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f5a6-130">-PassThru</span></span>
<span data-ttu-id="9f5a6-131">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9f5a6-131">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5a6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f5a6-132">-ResourceGroupName</span></span>
<span data-ttu-id="9f5a6-133">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9f5a6-133">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5a6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f5a6-134">-ResourceId</span></span>
<span data-ttu-id="9f5a6-135">ID risorsa coda di bus di servizio</span><span class="sxs-lookup"><span data-stu-id="9f5a6-135">Service Bus Queue Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: QueueResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f5a6-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f5a6-136">-Confirm</span></span>
<span data-ttu-id="9f5a6-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f5a6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f5a6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f5a6-138">-WhatIf</span></span>
<span data-ttu-id="9f5a6-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f5a6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f5a6-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f5a6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f5a6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5a6-141">CommonParameters</span></span>
<span data-ttu-id="9f5a6-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f5a6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5a6-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f5a6-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5a6-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="9f5a6-144">INPUTS</span></span>

### <span data-ttu-id="9f5a6-145">System.String</span><span class="sxs-lookup"><span data-stu-id="9f5a6-145">System.String</span></span>

### <span data-ttu-id="9f5a6-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="9f5a6-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="9f5a6-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f5a6-147">OUTPUTS</span></span>

### <span data-ttu-id="9f5a6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9f5a6-148">System.Boolean</span></span>

## <span data-ttu-id="9f5a6-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="9f5a6-149">NOTES</span></span>

## <span data-ttu-id="9f5a6-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f5a6-150">RELATED LINKS</span></span>
