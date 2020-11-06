---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: 31ed4d8765599fcc99f58870b347a14cdaf00162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518664"
---
# <span data-ttu-id="49c8e-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="49c8e-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="49c8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="49c8e-103">Rimuove l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="49c8e-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49c8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49c8e-104">SYNTAX</span></span>

### <span data-ttu-id="49c8e-105">EventhubDefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="49c8e-105">EventhubDefaultSet (Default)</span></span>
```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49c8e-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="49c8e-106">EventhubInputObjectSet</span></span>
```
Remove-AzureRmEventHub [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49c8e-107">EventhubResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49c8e-107">EventhubResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHub [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49c8e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49c8e-108">DESCRIPTION</span></span>
<span data-ttu-id="49c8e-109">Il cmdlet Remove-AzureRmEventHub rimuove ed Elimina il hub dell'evento specificato dallo spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="49c8e-109">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="49c8e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49c8e-110">EXAMPLES</span></span>

### <span data-ttu-id="49c8e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49c8e-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="49c8e-112">Rimuove l'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="49c8e-112">Removes the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="49c8e-113">Esempio 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="49c8e-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -InputObject $inputobject
```

### <span data-ttu-id="49c8e-114">Esempio 2,2-InputObject using piping:</span><span class="sxs-lookup"><span data-stu-id="49c8e-114">Example 2.2 - InputObject Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHub <params> | Remove-AzureRmEventHub
```

### <span data-ttu-id="49c8e-115">Esempio 3,1-ResourceId-using Variable:</span><span class="sxs-lookup"><span data-stu-id="49c8e-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHub <params>
PS C:\> Remove-AzureRmEventHub -ResourceId $resourceid.Id
```

### <span data-ttu-id="49c8e-116">Esempio 3,1-ResourceId-using string:</span><span class="sxs-lookup"><span data-stu-id="49c8e-116">Example 3.1 - ResourceId - Using string:</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName"
```

## <span data-ttu-id="49c8e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49c8e-117">PARAMETERS</span></span>

### <span data-ttu-id="49c8e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49c8e-118">-AsJob</span></span>
<span data-ttu-id="49c8e-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="49c8e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49c8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c8e-120">-DefaultProfile</span></span>
<span data-ttu-id="49c8e-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49c8e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49c8e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49c8e-122">-InputObject</span></span>
<span data-ttu-id="49c8e-123">Oggetto Eventhub</span><span class="sxs-lookup"><span data-stu-id="49c8e-123">Eventhub Object</span></span>

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

### <span data-ttu-id="49c8e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="49c8e-124">-Name</span></span>
<span data-ttu-id="49c8e-125">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="49c8e-125">EventHub Name</span></span>

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

### <span data-ttu-id="49c8e-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="49c8e-126">-Namespace</span></span>
<span data-ttu-id="49c8e-127">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="49c8e-127">Namespace Name</span></span>

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

### <span data-ttu-id="49c8e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49c8e-128">-PassThru</span></span>
<span data-ttu-id="49c8e-129">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="49c8e-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="49c8e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c8e-130">-ResourceGroupName</span></span>
<span data-ttu-id="49c8e-131">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="49c8e-131">Resource Group Name</span></span>

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

### <span data-ttu-id="49c8e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49c8e-132">-ResourceId</span></span>
<span data-ttu-id="49c8e-133">ID risorsa Eventhub</span><span class="sxs-lookup"><span data-stu-id="49c8e-133">Eventhub Resource Id</span></span>

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

### <span data-ttu-id="49c8e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="49c8e-134">-Confirm</span></span>
<span data-ttu-id="49c8e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49c8e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49c8e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49c8e-136">-WhatIf</span></span>
<span data-ttu-id="49c8e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49c8e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49c8e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49c8e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49c8e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c8e-139">CommonParameters</span></span>
<span data-ttu-id="49c8e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c8e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c8e-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49c8e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c8e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49c8e-142">INPUTS</span></span>

### <span data-ttu-id="49c8e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="49c8e-143">System.String</span></span>

### <span data-ttu-id="49c8e-144">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="49c8e-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>
<span data-ttu-id="49c8e-145">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="49c8e-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="49c8e-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49c8e-146">OUTPUTS</span></span>

### <span data-ttu-id="49c8e-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49c8e-147">System.Boolean</span></span>

## <span data-ttu-id="49c8e-148">Note</span><span class="sxs-lookup"><span data-stu-id="49c8e-148">NOTES</span></span>

## <span data-ttu-id="49c8e-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49c8e-149">RELATED LINKS</span></span>
