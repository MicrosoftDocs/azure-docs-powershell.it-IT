---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: daa63859c9649d9467f750f77d5b0e466d03ff56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193418"
---
# <span data-ttu-id="9d6a3-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="9d6a3-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="9d6a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="9d6a3-103">Rimuove l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="9d6a3-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="9d6a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d6a3-104">SYNTAX</span></span>

### <span data-ttu-id="9d6a3-105">EventhubDefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d6a3-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d6a3-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9d6a3-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d6a3-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d6a3-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d6a3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d6a3-108">DESCRIPTION</span></span>
<span data-ttu-id="9d6a3-109">Il cmdlet Remove-AzEventHub rimuove ed Elimina il hub dell'evento specificato dallo spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="9d6a3-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="9d6a3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d6a3-110">EXAMPLES</span></span>

### <span data-ttu-id="9d6a3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d6a3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="9d6a3-112">Rimuove l'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="9d6a3-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="9d6a3-113">Esempio 2: InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="9d6a3-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="9d6a3-114">Esempio 3: InputObject con piping:</span><span class="sxs-lookup"><span data-stu-id="9d6a3-114">Example 3: InputObject Using Piping:</span></span>
```powershell
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="9d6a3-115">Esempio 4: ResourceId-using Variable:</span><span class="sxs-lookup"><span data-stu-id="9d6a3-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="9d6a3-116">Esempio 5: ResourceId-using string:</span><span class="sxs-lookup"><span data-stu-id="9d6a3-116">Example 5: ResourceId - Using string:</span></span>
```powershell
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="9d6a3-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d6a3-117">PARAMETERS</span></span>

### <span data-ttu-id="9d6a3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d6a3-118">-AsJob</span></span>
<span data-ttu-id="9d6a3-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9d6a3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d6a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d6a3-120">-DefaultProfile</span></span>
<span data-ttu-id="9d6a3-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d6a3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d6a3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d6a3-122">-InputObject</span></span>
<span data-ttu-id="9d6a3-123">Oggetto Eventhub</span><span class="sxs-lookup"><span data-stu-id="9d6a3-123">Eventhub Object</span></span>

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

### <span data-ttu-id="9d6a3-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d6a3-124">-Name</span></span>
<span data-ttu-id="9d6a3-125">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="9d6a3-125">EventHub Name</span></span>

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

### <span data-ttu-id="9d6a3-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d6a3-126">-Namespace</span></span>
<span data-ttu-id="9d6a3-127">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d6a3-127">Namespace Name</span></span>

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

### <span data-ttu-id="9d6a3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d6a3-128">-PassThru</span></span>
<span data-ttu-id="9d6a3-129">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="9d6a3-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9d6a3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d6a3-130">-ResourceGroupName</span></span>
<span data-ttu-id="9d6a3-131">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9d6a3-131">Resource Group Name</span></span>

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

### <span data-ttu-id="9d6a3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d6a3-132">-ResourceId</span></span>
<span data-ttu-id="9d6a3-133">ID risorsa Eventhub</span><span class="sxs-lookup"><span data-stu-id="9d6a3-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="9d6a3-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d6a3-134">-Confirm</span></span>
<span data-ttu-id="9d6a3-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d6a3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d6a3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d6a3-136">-WhatIf</span></span>
<span data-ttu-id="9d6a3-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d6a3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d6a3-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d6a3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d6a3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d6a3-139">CommonParameters</span></span>
<span data-ttu-id="9d6a3-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d6a3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d6a3-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d6a3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d6a3-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d6a3-142">INPUTS</span></span>

### <span data-ttu-id="9d6a3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9d6a3-143">System.String</span></span>

### <span data-ttu-id="9d6a3-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="9d6a3-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="9d6a3-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d6a3-145">OUTPUTS</span></span>

### <span data-ttu-id="9d6a3-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d6a3-146">System.Boolean</span></span>

## <span data-ttu-id="9d6a3-147">Note</span><span class="sxs-lookup"><span data-stu-id="9d6a3-147">NOTES</span></span>

## <span data-ttu-id="9d6a3-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d6a3-148">RELATED LINKS</span></span>