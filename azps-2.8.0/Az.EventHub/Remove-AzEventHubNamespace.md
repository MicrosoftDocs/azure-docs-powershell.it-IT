---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 4d5ddbc4dff2922b90bc6d1117ff32473afd9042
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674421"
---
# <span data-ttu-id="4eb75-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4eb75-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="4eb75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4eb75-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb75-103">Rimuove lo spazio dei nomi degli hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="4eb75-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="4eb75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4eb75-104">SYNTAX</span></span>

### <span data-ttu-id="4eb75-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4eb75-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb75-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4eb75-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eb75-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eb75-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb75-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4eb75-108">DESCRIPTION</span></span>
<span data-ttu-id="4eb75-109">Il cmdlet Remove-AzEventHubNamespace rimuove ed Elimina lo spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="4eb75-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="4eb75-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4eb75-110">EXAMPLES</span></span>

### <span data-ttu-id="4eb75-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4eb75-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="4eb75-112">Rimuove lo spazio dei nomi degli hub di eventi MyNamespace \` \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="4eb75-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4eb75-113">Esempio 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="4eb75-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="4eb75-114">Esempio 2,1-InputObject-using piping:</span><span class="sxs-lookup"><span data-stu-id="4eb75-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="4eb75-115">Esempio 3,1-ResourceId-using Variable</span><span class="sxs-lookup"><span data-stu-id="4eb75-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="4eb75-116">Esempio 3,2-ResourceId-using piping:</span><span class="sxs-lookup"><span data-stu-id="4eb75-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="4eb75-117">Esempio 3,3-ResourceId-using string:</span><span class="sxs-lookup"><span data-stu-id="4eb75-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="4eb75-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4eb75-118">PARAMETERS</span></span>

### <span data-ttu-id="4eb75-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4eb75-119">-AsJob</span></span>
<span data-ttu-id="4eb75-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4eb75-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4eb75-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb75-121">-DefaultProfile</span></span>
<span data-ttu-id="4eb75-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4eb75-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb75-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4eb75-123">-InputObject</span></span>
<span data-ttu-id="4eb75-124">Oggetto spazio dei nomi EventHubs</span><span class="sxs-lookup"><span data-stu-id="4eb75-124">EventHubs Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb75-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4eb75-125">-Name</span></span>
<span data-ttu-id="4eb75-126">Nome dello spazio dei nomi EventHub</span><span class="sxs-lookup"><span data-stu-id="4eb75-126">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb75-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4eb75-127">-PassThru</span></span>
<span data-ttu-id="4eb75-128">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="4eb75-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4eb75-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb75-129">-ResourceGroupName</span></span>
<span data-ttu-id="4eb75-130">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4eb75-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb75-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4eb75-131">-ResourceId</span></span>
<span data-ttu-id="4eb75-132">ID risorsa dello spazio dei nomi EventHubs</span><span class="sxs-lookup"><span data-stu-id="4eb75-132">EventHubs Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb75-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4eb75-133">-Confirm</span></span>
<span data-ttu-id="4eb75-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eb75-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb75-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb75-135">-WhatIf</span></span>
<span data-ttu-id="4eb75-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4eb75-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb75-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4eb75-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb75-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb75-138">CommonParameters</span></span>
<span data-ttu-id="4eb75-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb75-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb75-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb75-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb75-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4eb75-141">INPUTS</span></span>

### <span data-ttu-id="4eb75-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4eb75-142">System.String</span></span>

### <span data-ttu-id="4eb75-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4eb75-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="4eb75-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4eb75-144">OUTPUTS</span></span>

### <span data-ttu-id="4eb75-145">System. void</span><span class="sxs-lookup"><span data-stu-id="4eb75-145">System.Void</span></span>

## <span data-ttu-id="4eb75-146">Note</span><span class="sxs-lookup"><span data-stu-id="4eb75-146">NOTES</span></span>

## <span data-ttu-id="4eb75-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4eb75-147">RELATED LINKS</span></span>