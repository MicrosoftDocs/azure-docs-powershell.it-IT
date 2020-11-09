---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: c93f0d8a44a67195d2c901dd581505276b7ae2f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296755"
---
# <span data-ttu-id="45211-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="45211-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="45211-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45211-102">SYNOPSIS</span></span>
<span data-ttu-id="45211-103">Rimuove la coda dallo spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="45211-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="45211-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45211-104">SYNTAX</span></span>

### <span data-ttu-id="45211-105">QueuePropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="45211-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45211-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="45211-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45211-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="45211-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45211-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45211-108">DESCRIPTION</span></span>
<span data-ttu-id="45211-109">Il cmdlet **Remove-AzServiceBusQueue** rimuove la coda dallo spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="45211-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="45211-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45211-110">EXAMPLES</span></span>

### <span data-ttu-id="45211-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="45211-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="45211-112">Rimuove la coda di Service Bus `SB-Queue_exampl1` dallo spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="45211-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="45211-113">Esempio 2: InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="45211-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="45211-114">Rimuove la coda di Service Bus specificata nel parametro $inputobject for-InputObject</span><span class="sxs-lookup"><span data-stu-id="45211-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="45211-115">Esempio 3: InputObject-using piping:</span><span class="sxs-lookup"><span data-stu-id="45211-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="45211-116">Esempio 4: ResourceId-using Variable:</span><span class="sxs-lookup"><span data-stu-id="45211-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="45211-117">Rimuove la coda di Service Bus fornita nell'ID ARM in $resourceid parametro/String for-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45211-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="45211-118">Esempio 5: ResourceId-passaggio come stringa:</span><span class="sxs-lookup"><span data-stu-id="45211-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="45211-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45211-119">PARAMETERS</span></span>

### <span data-ttu-id="45211-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45211-120">-AsJob</span></span>
<span data-ttu-id="45211-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="45211-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45211-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45211-122">-DefaultProfile</span></span>
<span data-ttu-id="45211-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45211-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45211-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45211-124">-InputObject</span></span>
<span data-ttu-id="45211-125">Oggetto coda bus di servizio</span><span class="sxs-lookup"><span data-stu-id="45211-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="45211-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="45211-126">-Name</span></span>
<span data-ttu-id="45211-127">Nome coda</span><span class="sxs-lookup"><span data-stu-id="45211-127">Queue Name</span></span>

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

### <span data-ttu-id="45211-128">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="45211-128">-Namespace</span></span>
<span data-ttu-id="45211-129">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="45211-129">Namespace Name</span></span>

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

### <span data-ttu-id="45211-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45211-130">-PassThru</span></span>
<span data-ttu-id="45211-131">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="45211-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="45211-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45211-132">-ResourceGroupName</span></span>
<span data-ttu-id="45211-133">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="45211-133">The name of the resource group</span></span>

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

### <span data-ttu-id="45211-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45211-134">-ResourceId</span></span>
<span data-ttu-id="45211-135">ID risorsa coda bus di servizio</span><span class="sxs-lookup"><span data-stu-id="45211-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="45211-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45211-136">-Confirm</span></span>
<span data-ttu-id="45211-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45211-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45211-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45211-138">-WhatIf</span></span>
<span data-ttu-id="45211-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45211-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45211-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45211-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45211-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45211-141">CommonParameters</span></span>
<span data-ttu-id="45211-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45211-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45211-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45211-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45211-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45211-144">INPUTS</span></span>

### <span data-ttu-id="45211-145">System. String</span><span class="sxs-lookup"><span data-stu-id="45211-145">System.String</span></span>

### <span data-ttu-id="45211-146">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="45211-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="45211-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45211-147">OUTPUTS</span></span>

### <span data-ttu-id="45211-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45211-148">System.Boolean</span></span>

## <span data-ttu-id="45211-149">Note</span><span class="sxs-lookup"><span data-stu-id="45211-149">NOTES</span></span>

## <span data-ttu-id="45211-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45211-150">RELATED LINKS</span></span>
