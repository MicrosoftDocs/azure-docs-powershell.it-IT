---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNamespace.md
ms.openlocfilehash: 29f2b961637a398470f6455d0d2330ce5fd863a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200367"
---
# <span data-ttu-id="02d89-101">Remove-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="02d89-101">Remove-AzEventHubNamespace</span></span>

## <span data-ttu-id="02d89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02d89-102">SYNOPSIS</span></span>
<span data-ttu-id="02d89-103">Rimuove lo spazio dei nomi hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="02d89-103">Removes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="02d89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02d89-104">SYNTAX</span></span>

### <span data-ttu-id="02d89-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="02d89-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02d89-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="02d89-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02d89-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02d89-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02d89-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="02d89-108">DESCRIPTION</span></span>
<span data-ttu-id="02d89-109">Il cmdlet Remove-AzEventHubNamespace rimuove ed elimina lo spazio dei nomi Hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="02d89-109">The Remove-AzEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="02d89-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02d89-110">EXAMPLES</span></span>

### <span data-ttu-id="02d89-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02d89-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="02d89-112">Rimuove lo spazio dei nomi Hub eventi \` MyWithName \` nel gruppo di risorse \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="02d89-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="02d89-113">Esempio 2: InputObject - Using Variable:</span><span class="sxs-lookup"><span data-stu-id="02d89-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputObject = Get-AzEventHubNamespace <params> 
PS C:\> Remove-AzEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="02d89-114">Esempio 3: InputObject - Uso di Piping:</span><span class="sxs-lookup"><span data-stu-id="02d89-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHubNamespace <params> | Remove-AzEventHubNamespace
```

### <span data-ttu-id="02d89-115">Esempio 4: ResourceId - Using Variable</span><span class="sxs-lookup"><span data-stu-id="02d89-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubNamespace <params>
PS C:\> Remove-AzEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="02d89-116">Esempio 5: ResourceId - Uso di Piping:</span><span class="sxs-lookup"><span data-stu-id="02d89-116">Example 5: ResourceId - Using Piping:</span></span>
```powershell
PS C:\> Get-AzResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzEventHubNamespace
```

### <span data-ttu-id="02d89-117">Esempio 6: ResourceId - Uso della stringa:</span><span class="sxs-lookup"><span data-stu-id="02d89-117">Example 6: ResourceId - Using String:</span></span>
```powershell
PS C:\> Remove-AzEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="02d89-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02d89-118">PARAMETERS</span></span>

### <span data-ttu-id="02d89-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02d89-119">-AsJob</span></span>
<span data-ttu-id="02d89-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="02d89-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02d89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d89-121">-DefaultProfile</span></span>
<span data-ttu-id="02d89-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="02d89-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02d89-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02d89-123">-InputObject</span></span>
<span data-ttu-id="02d89-124">Oggetto Spazio dei nomi di EventHubs</span><span class="sxs-lookup"><span data-stu-id="02d89-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="02d89-125">-Name</span><span class="sxs-lookup"><span data-stu-id="02d89-125">-Name</span></span>
<span data-ttu-id="02d89-126">Nome spazio dei nomi di EventHub</span><span class="sxs-lookup"><span data-stu-id="02d89-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="02d89-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02d89-127">-PassThru</span></span>
<span data-ttu-id="02d89-128">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="02d89-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="02d89-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d89-129">-ResourceGroupName</span></span>
<span data-ttu-id="02d89-130">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="02d89-130">Resource Group Name</span></span>

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

### <span data-ttu-id="02d89-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02d89-131">-ResourceId</span></span>
<span data-ttu-id="02d89-132">ID risorsa spazio dei nomi di EventHubs</span><span class="sxs-lookup"><span data-stu-id="02d89-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="02d89-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02d89-133">-Confirm</span></span>
<span data-ttu-id="02d89-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02d89-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02d89-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02d89-135">-WhatIf</span></span>
<span data-ttu-id="02d89-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02d89-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02d89-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02d89-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02d89-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d89-138">CommonParameters</span></span>
<span data-ttu-id="02d89-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d89-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d89-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d89-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d89-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="02d89-141">INPUTS</span></span>

### <span data-ttu-id="02d89-142">System.String</span><span class="sxs-lookup"><span data-stu-id="02d89-142">System.String</span></span>

### <span data-ttu-id="02d89-143">Microsoft.Azure.Commands.EventHub.Models.PSAttributes</span><span class="sxs-lookup"><span data-stu-id="02d89-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="02d89-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02d89-144">OUTPUTS</span></span>

### <span data-ttu-id="02d89-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="02d89-145">System.Void</span></span>

## <span data-ttu-id="02d89-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="02d89-146">NOTES</span></span>

## <span data-ttu-id="02d89-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02d89-147">RELATED LINKS</span></span>
