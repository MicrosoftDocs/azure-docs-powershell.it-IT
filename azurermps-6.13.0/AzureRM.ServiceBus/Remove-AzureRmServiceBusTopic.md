---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 8434893dd3661bbfb1f78a4973dc206f44e9f400
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509071"
---
# <span data-ttu-id="d94d0-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="d94d0-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="d94d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d94d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d94d0-103">Rimuove l'argomento dallo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="d94d0-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d94d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d94d0-104">SYNTAX</span></span>

### <span data-ttu-id="d94d0-105">TopicPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d94d0-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d94d0-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d94d0-106">TopicInputObjectSet</span></span>
```
Remove-AzureRmServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d94d0-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d94d0-107">TopicResourceIdSet</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d94d0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d94d0-108">DESCRIPTION</span></span>
<span data-ttu-id="d94d0-109">Il cmdlet **Remove-AzureRmServiceBusTopic** rimuove l'argomento dallo spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="d94d0-109">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d94d0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d94d0-110">EXAMPLES</span></span>

### <span data-ttu-id="d94d0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d94d0-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="d94d0-112">Rimuove l'argomento `SB-Topic_exampl1` dallo spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="d94d0-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="d94d0-113">Esempio 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="d94d0-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusTopic <parmas>
PS C:\> Remove-AzureRmServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="d94d0-114">Esempio 2,2-InputObject-using piping:</span><span class="sxs-lookup"><span data-stu-id="d94d0-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic <parmas> | Remove-AzureRmServiceBusTopic
```

### <span data-ttu-id="d94d0-115">Esempio 3,1-ResourceId con la variabile:</span><span class="sxs-lookup"><span data-stu-id="d94d0-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusTopic <params>
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="d94d0-116">Esempio 3,2-ResourceId usando il valore stringa</span><span class="sxs-lookup"><span data-stu-id="d94d0-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="d94d0-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d94d0-117">PARAMETERS</span></span>

### <span data-ttu-id="d94d0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d94d0-118">-AsJob</span></span>
<span data-ttu-id="d94d0-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d94d0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d94d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94d0-120">-DefaultProfile</span></span>
<span data-ttu-id="d94d0-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d94d0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d94d0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d94d0-122">-InputObject</span></span>
<span data-ttu-id="d94d0-123">Oggetto argomento Service Bus</span><span class="sxs-lookup"><span data-stu-id="d94d0-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d94d0-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d94d0-124">-Name</span></span>
<span data-ttu-id="d94d0-125">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="d94d0-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d94d0-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d94d0-126">-Namespace</span></span>
<span data-ttu-id="d94d0-127">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d94d0-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d94d0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d94d0-128">-PassThru</span></span>
<span data-ttu-id="d94d0-129">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="d94d0-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d94d0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d94d0-130">-ResourceGroupName</span></span>
<span data-ttu-id="d94d0-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d94d0-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d94d0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d94d0-132">-ResourceId</span></span>
<span data-ttu-id="d94d0-133">ID risorsa argomento Service Bus</span><span class="sxs-lookup"><span data-stu-id="d94d0-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d94d0-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d94d0-134">-Confirm</span></span>
<span data-ttu-id="d94d0-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d94d0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d94d0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d94d0-136">-WhatIf</span></span>
<span data-ttu-id="d94d0-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d94d0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d94d0-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d94d0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d94d0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94d0-139">CommonParameters</span></span>
<span data-ttu-id="d94d0-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d94d0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94d0-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d94d0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94d0-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d94d0-142">INPUTS</span></span>

### <span data-ttu-id="d94d0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d94d0-143">System.String</span></span>

### <span data-ttu-id="d94d0-144">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="d94d0-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="d94d0-145">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d94d0-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d94d0-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d94d0-146">OUTPUTS</span></span>

### <span data-ttu-id="d94d0-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d94d0-147">System.Boolean</span></span>

## <span data-ttu-id="d94d0-148">Note</span><span class="sxs-lookup"><span data-stu-id="d94d0-148">NOTES</span></span>

## <span data-ttu-id="d94d0-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d94d0-149">RELATED LINKS</span></span>
