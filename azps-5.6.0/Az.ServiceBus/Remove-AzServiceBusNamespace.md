---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 7f6a7225742356e0410d3cc49aef60e50e1954a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978109"
---
# <span data-ttu-id="e3e50-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="e3e50-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="e3e50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3e50-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e50-103">Rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="e3e50-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="e3e50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3e50-104">SYNTAX</span></span>

### <span data-ttu-id="e3e50-105">NamespacePropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3e50-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e50-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e3e50-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3e50-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3e50-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3e50-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3e50-108">DESCRIPTION</span></span>
<span data-ttu-id="e3e50-109">Il cmdlet **Remove-AzServiceBus Consente di** rimuovere lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="e3e50-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="e3e50-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3e50-110">EXAMPLES</span></span>

### <span data-ttu-id="e3e50-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3e50-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="e3e50-112">Rimuove lo spazio dei nomi del bus di `SB-Example1` servizio dal gruppo di risorse `Default-ServiceBus-WestUS` specificato.</span><span class="sxs-lookup"><span data-stu-id="e3e50-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="e3e50-113">Esempio 2.1 - InputObject - Uso della variabile:</span><span class="sxs-lookup"><span data-stu-id="e3e50-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="e3e50-114">Rimuove lo spazio dei nomi dei bus di servizio fornito tramite il $inputobject.</span><span class="sxs-lookup"><span data-stu-id="e3e50-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="e3e50-115">Esempio 2.2 - InputObject - Uso di Piping:</span><span class="sxs-lookup"><span data-stu-id="e3e50-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="e3e50-116">Rimuove lo spazio dei nomi dei bus di servizio tramite Piping.</span><span class="sxs-lookup"><span data-stu-id="e3e50-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="e3e50-117">Esempio 3 - ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3e50-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="e3e50-118">Rimuove lo spazio dei nomi del bus di servizio fornito tramite ARM ID servizio in $resourceid parametro per -ResourceId o tramite piping.</span><span class="sxs-lookup"><span data-stu-id="e3e50-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="e3e50-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3e50-119">PARAMETERS</span></span>

### <span data-ttu-id="e3e50-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3e50-120">-AsJob</span></span>
<span data-ttu-id="e3e50-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e3e50-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3e50-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e50-122">-DefaultProfile</span></span>
<span data-ttu-id="e3e50-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3e50-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3e50-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3e50-124">-InputObject</span></span>
<span data-ttu-id="e3e50-125">Oggetto Spazio dei nomi bus di servizio</span><span class="sxs-lookup"><span data-stu-id="e3e50-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e50-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e3e50-126">-Name</span></span>
<span data-ttu-id="e3e50-127">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e3e50-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e50-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3e50-128">-PassThru</span></span>
<span data-ttu-id="e3e50-129">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e3e50-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e3e50-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e50-130">-ResourceGroupName</span></span>
<span data-ttu-id="e3e50-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e3e50-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e50-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3e50-132">-ResourceId</span></span>
<span data-ttu-id="e3e50-133">ID risorsa spazio dei nomi bus di servizio</span><span class="sxs-lookup"><span data-stu-id="e3e50-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="e3e50-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3e50-134">-Confirm</span></span>
<span data-ttu-id="e3e50-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3e50-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3e50-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3e50-136">-WhatIf</span></span>
<span data-ttu-id="e3e50-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3e50-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3e50-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3e50-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3e50-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e50-139">CommonParameters</span></span>
<span data-ttu-id="e3e50-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3e50-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e50-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3e50-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e50-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3e50-142">INPUTS</span></span>

### <span data-ttu-id="e3e50-143">System.String</span><span class="sxs-lookup"><span data-stu-id="e3e50-143">System.String</span></span>

### <span data-ttu-id="e3e50-144">Microsoft.Azure.Commands.ServiceBus.Models.PSAttributes</span><span class="sxs-lookup"><span data-stu-id="e3e50-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e3e50-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3e50-145">OUTPUTS</span></span>

### <span data-ttu-id="e3e50-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3e50-146">System.Boolean</span></span>

## <span data-ttu-id="e3e50-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3e50-147">NOTES</span></span>

## <span data-ttu-id="e3e50-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3e50-148">RELATED LINKS</span></span>
