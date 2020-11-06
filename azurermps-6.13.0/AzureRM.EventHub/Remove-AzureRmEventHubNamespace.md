---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6df8d5539bf340df5e00ad69ac557bc2cbb8ccaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515359"
---
# <span data-ttu-id="9d516-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="9d516-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="9d516-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d516-102">SYNOPSIS</span></span>
<span data-ttu-id="9d516-103">Rimuove lo spazio dei nomi degli hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="9d516-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d516-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d516-104">SYNTAX</span></span>

### <span data-ttu-id="9d516-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d516-105">NamespaceParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d516-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9d516-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmEventHubNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d516-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d516-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d516-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d516-108">DESCRIPTION</span></span>
<span data-ttu-id="9d516-109">Il cmdlet Remove-AzureRmEventHubNamespace rimuove ed Elimina lo spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="9d516-109">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="9d516-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d516-110">EXAMPLES</span></span>

### <span data-ttu-id="9d516-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d516-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="9d516-112">Rimuove lo spazio dei nomi degli hub di eventi MyNamespace \` \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9d516-112">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9d516-113">Esempio 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="9d516-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputObject = Get-AzureRmEventHubNamespace <params> 
PS C:\> Remove-AzureRmEventHubNamespace -InputObject $inputObject
```

### <span data-ttu-id="9d516-114">Esempio 2,1-InputObject-using piping:</span><span class="sxs-lookup"><span data-stu-id="9d516-114">Example 2.1 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace <params> | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="9d516-115">Esempio 3,1-ResourceId-using Variable</span><span class="sxs-lookup"><span data-stu-id="9d516-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubNamespace <params>
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId $resourceid.Id
```

### <span data-ttu-id="9d516-116">Esempio 3,2-ResourceId-using piping:</span><span class="sxs-lookup"><span data-stu-id="9d516-116">Example 3.2 - ResourceId - Using Piping:</span></span>
```
PS C:\> Get-AzureRmResource -ResourceType Microsoft.EventHub/Namespaces | Remove-AzureRmEventHubNamespace
```

### <span data-ttu-id="9d516-117">Esempio 3,3-ResourceId-using string:</span><span class="sxs-lookup"><span data-stu-id="9d516-117">Example 3.3 - ResourceId - Using String:</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName"
```

## <span data-ttu-id="9d516-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d516-118">PARAMETERS</span></span>

### <span data-ttu-id="9d516-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d516-119">-AsJob</span></span>
<span data-ttu-id="9d516-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9d516-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d516-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d516-121">-DefaultProfile</span></span>
<span data-ttu-id="9d516-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d516-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d516-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d516-123">-InputObject</span></span>
<span data-ttu-id="9d516-124">Oggetto spazio dei nomi EventHubs</span><span class="sxs-lookup"><span data-stu-id="9d516-124">EventHubs Namespace Object</span></span>

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

### <span data-ttu-id="9d516-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d516-125">-Name</span></span>
<span data-ttu-id="9d516-126">Nome dello spazio dei nomi EventHub</span><span class="sxs-lookup"><span data-stu-id="9d516-126">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="9d516-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d516-127">-PassThru</span></span>
<span data-ttu-id="9d516-128">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="9d516-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9d516-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d516-129">-ResourceGroupName</span></span>
<span data-ttu-id="9d516-130">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9d516-130">Resource Group Name</span></span>

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

### <span data-ttu-id="9d516-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d516-131">-ResourceId</span></span>
<span data-ttu-id="9d516-132">ID risorsa dello spazio dei nomi EventHubs</span><span class="sxs-lookup"><span data-stu-id="9d516-132">EventHubs Namespace Resource Id</span></span>

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

### <span data-ttu-id="9d516-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9d516-133">-Confirm</span></span>
<span data-ttu-id="9d516-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d516-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d516-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d516-135">-WhatIf</span></span>
<span data-ttu-id="9d516-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d516-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d516-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d516-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d516-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d516-138">CommonParameters</span></span>
<span data-ttu-id="9d516-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d516-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d516-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d516-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d516-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d516-141">INPUTS</span></span>

### <span data-ttu-id="9d516-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9d516-142">System.String</span></span>

### <span data-ttu-id="9d516-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9d516-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="9d516-144">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9d516-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9d516-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d516-145">OUTPUTS</span></span>

### <span data-ttu-id="9d516-146">System. void</span><span class="sxs-lookup"><span data-stu-id="9d516-146">System.Void</span></span>

## <span data-ttu-id="9d516-147">Note</span><span class="sxs-lookup"><span data-stu-id="9d516-147">NOTES</span></span>

## <span data-ttu-id="9d516-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d516-148">RELATED LINKS</span></span>
