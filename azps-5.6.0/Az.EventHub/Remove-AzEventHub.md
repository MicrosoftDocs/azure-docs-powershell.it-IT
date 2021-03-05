---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: 2d3f2ee9a4dc55dd709be3113770df402434c911
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992780"
---
# <span data-ttu-id="9029f-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="9029f-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="9029f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9029f-102">SYNOPSIS</span></span>
<span data-ttu-id="9029f-103">Rimuove l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="9029f-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="9029f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9029f-104">SYNTAX</span></span>

### <span data-ttu-id="9029f-105">EventhubDefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9029f-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9029f-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9029f-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9029f-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9029f-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9029f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9029f-108">DESCRIPTION</span></span>
<span data-ttu-id="9029f-109">Il cmdlet Remove-AzEventHub rimuove ed elimina l'hub eventi specificato dallo spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="9029f-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="9029f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9029f-110">EXAMPLES</span></span>

### <span data-ttu-id="9029f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9029f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="9029f-112">Rimuove l'hub eventi \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="9029f-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="9029f-113">Esempio 2: InputObject - Using Variable:</span><span class="sxs-lookup"><span data-stu-id="9029f-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="9029f-114">Esempio 3: InputObject tramite Piping:</span><span class="sxs-lookup"><span data-stu-id="9029f-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="9029f-115">Esempio 4: ResourceId - Uso della variabile:</span><span class="sxs-lookup"><span data-stu-id="9029f-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="9029f-116">Esempio 5: ResourceId - Uso della stringa:</span><span class="sxs-lookup"><span data-stu-id="9029f-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="9029f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9029f-117">PARAMETERS</span></span>

### <span data-ttu-id="9029f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9029f-118">-AsJob</span></span>
<span data-ttu-id="9029f-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9029f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9029f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9029f-120">-DefaultProfile</span></span>
<span data-ttu-id="9029f-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9029f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9029f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9029f-122">-InputObject</span></span>
<span data-ttu-id="9029f-123">Oggetto Eventhub</span><span class="sxs-lookup"><span data-stu-id="9029f-123">Eventhub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9029f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9029f-124">-Name</span></span>
<span data-ttu-id="9029f-125">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="9029f-125">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9029f-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9029f-126">-Namespace</span></span>
<span data-ttu-id="9029f-127">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9029f-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9029f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9029f-128">-PassThru</span></span>
<span data-ttu-id="9029f-129">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9029f-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9029f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9029f-130">-ResourceGroupName</span></span>
<span data-ttu-id="9029f-131">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9029f-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9029f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9029f-132">-ResourceId</span></span>
<span data-ttu-id="9029f-133">ID risorsa Eventhub</span><span class="sxs-lookup"><span data-stu-id="9029f-133">Eventhub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9029f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9029f-134">-Confirm</span></span>
<span data-ttu-id="9029f-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9029f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9029f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9029f-136">-WhatIf</span></span>
<span data-ttu-id="9029f-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9029f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9029f-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9029f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9029f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9029f-139">CommonParameters</span></span>
<span data-ttu-id="9029f-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9029f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9029f-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9029f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9029f-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="9029f-142">INPUTS</span></span>

### <span data-ttu-id="9029f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9029f-143">System.String</span></span>

### <span data-ttu-id="9029f-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="9029f-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="9029f-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9029f-145">OUTPUTS</span></span>

### <span data-ttu-id="9029f-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9029f-146">System.Boolean</span></span>

## <span data-ttu-id="9029f-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="9029f-147">NOTES</span></span>

## <span data-ttu-id="9029f-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9029f-148">RELATED LINKS</span></span>
