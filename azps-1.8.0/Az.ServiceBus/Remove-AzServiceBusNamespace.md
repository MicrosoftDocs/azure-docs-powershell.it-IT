---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: b17fa7309274f261c329eaf896519f8bb70d06fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677126"
---
# <span data-ttu-id="006be-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="006be-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="006be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="006be-102">SYNOPSIS</span></span>
<span data-ttu-id="006be-103">Rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="006be-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="006be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="006be-104">SYNTAX</span></span>

### <span data-ttu-id="006be-105">NamespacePropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="006be-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="006be-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="006be-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="006be-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="006be-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="006be-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="006be-108">DESCRIPTION</span></span>
<span data-ttu-id="006be-109">Il cmdlet **Remove-AzServiceBusNamespace** rimuove lo spazio dei nomi dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="006be-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="006be-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="006be-110">EXAMPLES</span></span>

### <span data-ttu-id="006be-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="006be-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="006be-112">Rimuove lo spazio dei nomi Service Bus `SB-Example1` dal gruppo di risorse specificato `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="006be-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="006be-113">Esempio 2,1-InputObject-using Variable:</span><span class="sxs-lookup"><span data-stu-id="006be-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="006be-114">Rimuove lo spazio dei nomi Service Bus fornito tramite la $inputobject.</span><span class="sxs-lookup"><span data-stu-id="006be-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="006be-115">Esempio 2,2-InputObject-using piping:</span><span class="sxs-lookup"><span data-stu-id="006be-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="006be-116">Rimuove lo spazio dei nomi Service Bus tramite piping.</span><span class="sxs-lookup"><span data-stu-id="006be-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="006be-117">Esempio 3-ResourceId</span><span class="sxs-lookup"><span data-stu-id="006be-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="006be-118">Rimuove lo spazio dei nomi Service Bus fornito tramite ID ARM in $resourceid parametro for-ResourceId o tramite piping.</span><span class="sxs-lookup"><span data-stu-id="006be-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="006be-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="006be-119">PARAMETERS</span></span>

### <span data-ttu-id="006be-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="006be-120">-AsJob</span></span>
<span data-ttu-id="006be-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="006be-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="006be-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="006be-122">-DefaultProfile</span></span>
<span data-ttu-id="006be-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="006be-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="006be-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="006be-124">-InputObject</span></span>
<span data-ttu-id="006be-125">Oggetto spazio dei nomi Service Bus</span><span class="sxs-lookup"><span data-stu-id="006be-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="006be-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="006be-126">-Name</span></span>
<span data-ttu-id="006be-127">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="006be-127">Namespace Name.</span></span>

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

### <span data-ttu-id="006be-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="006be-128">-PassThru</span></span>
<span data-ttu-id="006be-129">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="006be-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="006be-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="006be-130">-ResourceGroupName</span></span>
<span data-ttu-id="006be-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="006be-131">The name of the resource group</span></span>

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

### <span data-ttu-id="006be-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="006be-132">-ResourceId</span></span>
<span data-ttu-id="006be-133">ID risorsa dello spazio dei nomi Service Bus</span><span class="sxs-lookup"><span data-stu-id="006be-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="006be-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="006be-134">-Confirm</span></span>
<span data-ttu-id="006be-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="006be-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="006be-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="006be-136">-WhatIf</span></span>
<span data-ttu-id="006be-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="006be-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="006be-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="006be-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="006be-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="006be-139">CommonParameters</span></span>
<span data-ttu-id="006be-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="006be-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="006be-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="006be-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="006be-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="006be-142">INPUTS</span></span>

### <span data-ttu-id="006be-143">System. String</span><span class="sxs-lookup"><span data-stu-id="006be-143">System.String</span></span>

### <span data-ttu-id="006be-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="006be-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="006be-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="006be-145">OUTPUTS</span></span>

### <span data-ttu-id="006be-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="006be-146">System.Boolean</span></span>

## <span data-ttu-id="006be-147">Note</span><span class="sxs-lookup"><span data-stu-id="006be-147">NOTES</span></span>

## <span data-ttu-id="006be-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="006be-148">RELATED LINKS</span></span>
