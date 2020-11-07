---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHub.md
ms.openlocfilehash: c67793371b6842e4aa8190055580b0cdfefd3e08
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861462"
---
# <span data-ttu-id="f11e0-101">Remove-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="f11e0-101">Remove-AzEventHub</span></span>

## <span data-ttu-id="f11e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f11e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f11e0-103">Rimuove l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="f11e0-103">Removes the specified Event Hub.</span></span>

## <span data-ttu-id="f11e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f11e0-104">SYNTAX</span></span>

### <span data-ttu-id="f11e0-105">EventhubDefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f11e0-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f11e0-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f11e0-106">EventhubInputObjectSet</span></span>
```
Remove-AzEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f11e0-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f11e0-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f11e0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f11e0-108">DESCRIPTION</span></span>
<span data-ttu-id="f11e0-109">Il cmdlet Remove-AzEventHub rimuove ed Elimina il hub dell'evento specificato dallo spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="f11e0-109">The Remove-AzEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="f11e0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f11e0-110">EXAMPLES</span></span>

### <span data-ttu-id="f11e0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f11e0-111">Example 1</span></span>
```
PS C:\> Remove-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="f11e0-112">Rimuove l'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="f11e0-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="f11e0-113">Esempio 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="f11e0-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -InputObject $inputobject
```

### <span data-ttu-id="f11e0-114">Esempio 2,2-InputObject using piping:</span><span class="sxs-lookup"><span data-stu-id="f11e0-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzEventHub <params> | Remove-AzEventHub
```

### <span data-ttu-id="f11e0-115">Esempio 3,1-ResourceId-using Variable:</span><span class="sxs-lookup"><span data-stu-id="f11e0-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzEventHub <params>
PS C:\> Remove-AzEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="f11e0-116">Esempio 3,1-ResourceId-using string:</span><span class="sxs-lookup"><span data-stu-id="f11e0-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="f11e0-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f11e0-117">PARAMETERS</span></span>

### <span data-ttu-id="f11e0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f11e0-118">-AsJob</span></span>
<span data-ttu-id="f11e0-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f11e0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f11e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11e0-120">-DefaultProfile</span></span>
<span data-ttu-id="f11e0-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f11e0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f11e0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f11e0-122">-InputObject</span></span>
<span data-ttu-id="f11e0-123">Oggetto Eventhub</span><span class="sxs-lookup"><span data-stu-id="f11e0-123">Eventhub Object</span></span>

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

### <span data-ttu-id="f11e0-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f11e0-124">-Name</span></span>
<span data-ttu-id="f11e0-125">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="f11e0-125">EventHub Name</span></span>

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

### <span data-ttu-id="f11e0-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f11e0-126">-Namespace</span></span>
<span data-ttu-id="f11e0-127">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f11e0-127">Namespace Name</span></span>

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

### <span data-ttu-id="f11e0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f11e0-128">-PassThru</span></span>
<span data-ttu-id="f11e0-129">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="f11e0-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f11e0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f11e0-130">-ResourceGroupName</span></span>
<span data-ttu-id="f11e0-131">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f11e0-131">Resource Group Name</span></span>

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

### <span data-ttu-id="f11e0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f11e0-132">-ResourceId</span></span>
<span data-ttu-id="f11e0-133">ID risorsa Eventhub</span><span class="sxs-lookup"><span data-stu-id="f11e0-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="f11e0-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f11e0-134">-Confirm</span></span>
<span data-ttu-id="f11e0-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f11e0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f11e0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f11e0-136">-WhatIf</span></span>
<span data-ttu-id="f11e0-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f11e0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f11e0-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f11e0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f11e0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11e0-139">CommonParameters</span></span>
<span data-ttu-id="f11e0-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f11e0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11e0-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f11e0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11e0-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f11e0-142">INPUTS</span></span>

### <span data-ttu-id="f11e0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f11e0-143">System.String</span></span>

### <span data-ttu-id="f11e0-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="f11e0-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="f11e0-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f11e0-145">OUTPUTS</span></span>

### <span data-ttu-id="f11e0-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f11e0-146">System.Boolean</span></span>

## <span data-ttu-id="f11e0-147">Note</span><span class="sxs-lookup"><span data-stu-id="f11e0-147">NOTES</span></span>

## <span data-ttu-id="f11e0-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f11e0-148">RELATED LINKS</span></span>
