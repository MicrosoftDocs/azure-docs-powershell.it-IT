---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 75da2231dae7ea0dc587d48ca832b7631fc24986
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369232"
---
# <span data-ttu-id="f5703-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="f5703-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="f5703-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f5703-102">SYNOPSIS</span></span>
<span data-ttu-id="f5703-103">Rimuove l'argomento dallo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="f5703-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f5703-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5703-104">SYNTAX</span></span>

### <span data-ttu-id="f5703-105">TopicPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f5703-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5703-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f5703-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5703-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f5703-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5703-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5703-108">DESCRIPTION</span></span>
<span data-ttu-id="f5703-109">Il cmdlet **Remove-AzServiceBusTopic** rimuove l'argomento dallo spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="f5703-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f5703-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5703-110">EXAMPLES</span></span>

### <span data-ttu-id="f5703-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f5703-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="f5703-112">Rimuove l'argomento `SB-Topic_exampl1` dallo spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="f5703-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="f5703-113">Esempio 2: InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="f5703-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="f5703-114">Esempio 3: InputObject-using piping:</span><span class="sxs-lookup"><span data-stu-id="f5703-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="f5703-115">Esempio 4: ResourceId con la variabile:</span><span class="sxs-lookup"><span data-stu-id="f5703-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="f5703-116">Esempio 5: ResourceId con il valore stringa</span><span class="sxs-lookup"><span data-stu-id="f5703-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="f5703-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f5703-117">PARAMETERS</span></span>

### <span data-ttu-id="f5703-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5703-118">-AsJob</span></span>
<span data-ttu-id="f5703-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f5703-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5703-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5703-120">-DefaultProfile</span></span>
<span data-ttu-id="f5703-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5703-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5703-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5703-122">-InputObject</span></span>
<span data-ttu-id="f5703-123">Oggetto argomento Service Bus</span><span class="sxs-lookup"><span data-stu-id="f5703-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="f5703-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5703-124">-Name</span></span>
<span data-ttu-id="f5703-125">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="f5703-125">Topic Name</span></span>

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

### <span data-ttu-id="f5703-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5703-126">-Namespace</span></span>
<span data-ttu-id="f5703-127">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5703-127">Namespace Name</span></span>

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

### <span data-ttu-id="f5703-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5703-128">-PassThru</span></span>
<span data-ttu-id="f5703-129">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="f5703-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f5703-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5703-130">-ResourceGroupName</span></span>
<span data-ttu-id="f5703-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f5703-131">The name of the resource group</span></span>

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

### <span data-ttu-id="f5703-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5703-132">-ResourceId</span></span>
<span data-ttu-id="f5703-133">ID risorsa argomento Service Bus</span><span class="sxs-lookup"><span data-stu-id="f5703-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="f5703-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f5703-134">-Confirm</span></span>
<span data-ttu-id="f5703-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5703-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5703-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5703-136">-WhatIf</span></span>
<span data-ttu-id="f5703-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5703-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5703-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5703-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5703-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5703-139">CommonParameters</span></span>
<span data-ttu-id="f5703-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5703-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5703-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5703-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5703-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f5703-142">INPUTS</span></span>

### <span data-ttu-id="f5703-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f5703-143">System.String</span></span>

### <span data-ttu-id="f5703-144">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="f5703-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="f5703-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5703-145">OUTPUTS</span></span>

### <span data-ttu-id="f5703-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5703-146">System.Boolean</span></span>

## <span data-ttu-id="f5703-147">Note</span><span class="sxs-lookup"><span data-stu-id="f5703-147">NOTES</span></span>

## <span data-ttu-id="f5703-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5703-148">RELATED LINKS</span></span>
