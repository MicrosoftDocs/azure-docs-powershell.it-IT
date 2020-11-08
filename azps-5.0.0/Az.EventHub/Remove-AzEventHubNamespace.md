---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 29f2b961637a398470f6455d0d2330ce5fd863a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200908"
---
# <span data-ttu-id="1324c-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="1324c-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="1324c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1324c-102">SYNOPSIS</span></span>
<span data-ttu-id="1324c-103">Rimuove lo spazio dei nomi degli hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="1324c-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="1324c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1324c-104">SYNTAX</span></span>

### <span data-ttu-id="1324c-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1324c-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1324c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1324c-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1324c-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1324c-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1324c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1324c-108">DESCRIPTION</span></span>
<span data-ttu-id="1324c-109">Il cmdlet Remove-AzEventHubNamespace rimuove ed Elimina lo spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="1324c-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="1324c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1324c-110">EXAMPLES</span></span>

### <span data-ttu-id="1324c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1324c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="1324c-112">Rimuove lo spazio dei nomi degli hub di eventi MyNamespace \` \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="1324c-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="1324c-113">Esempio 2: InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="1324c-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="1324c-114">Esempio 3: InputObject-using piping:</span><span class="sxs-lookup"><span data-stu-id="1324c-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="1324c-115">Esempio 4: ResourceId-utilizzo della variabile</span><span class="sxs-lookup"><span data-stu-id="1324c-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="1324c-116">Esempio 5: ResourceId-using piping:</span><span class="sxs-lookup"><span data-stu-id="1324c-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="1324c-117">Esempio 6: ResourceId-using string:</span><span class="sxs-lookup"><span data-stu-id="1324c-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="1324c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1324c-118">PARAMETERS</span></span>

### <span data-ttu-id="1324c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1324c-119">-AsJob</span></span>
<span data-ttu-id="1324c-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1324c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1324c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1324c-121">-DefaultProfile</span></span>
<span data-ttu-id="1324c-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1324c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1324c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1324c-123">-InputObject</span></span>
<span data-ttu-id="1324c-124">Oggetto spazio dei nomi EventHubs</span><span class="sxs-lookup"><span data-stu-id="1324c-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="1324c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1324c-125">-Name</span></span>
<span data-ttu-id="1324c-126">Nome dello spazio dei nomi EventHub</span><span class="sxs-lookup"><span data-stu-id="1324c-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="1324c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1324c-127">-PassThru</span></span>
<span data-ttu-id="1324c-128">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="1324c-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1324c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1324c-129">-ResourceGroupName</span></span>
<span data-ttu-id="1324c-130">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1324c-130">Resource Group Name</span></span>

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

### <span data-ttu-id="1324c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1324c-131">-ResourceId</span></span>
<span data-ttu-id="1324c-132">ID risorsa dello spazio dei nomi EventHubs</span><span class="sxs-lookup"><span data-stu-id="1324c-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="1324c-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1324c-133">-Confirm</span></span>
<span data-ttu-id="1324c-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1324c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1324c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1324c-135">-WhatIf</span></span>
<span data-ttu-id="1324c-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1324c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1324c-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1324c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1324c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1324c-138">CommonParameters</span></span>
<span data-ttu-id="1324c-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1324c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1324c-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1324c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1324c-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1324c-141">INPUTS</span></span>

### <span data-ttu-id="1324c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1324c-142">System.String</span></span>

### <span data-ttu-id="1324c-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1324c-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="1324c-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1324c-144">OUTPUTS</span></span>

### <span data-ttu-id="1324c-145">System. void</span><span class="sxs-lookup"><span data-stu-id="1324c-145">System.Void</span></span>

## <span data-ttu-id="1324c-146">Note</span><span class="sxs-lookup"><span data-stu-id="1324c-146">NOTES</span></span>

## <span data-ttu-id="1324c-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1324c-147">RELATED LINKS</span></span>
