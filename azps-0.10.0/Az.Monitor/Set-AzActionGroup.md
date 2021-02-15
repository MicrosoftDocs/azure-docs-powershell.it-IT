---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: ede2a8566f7305b4f56a5fc392090b426c148547
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399006"
---
# <span data-ttu-id="db3ec-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="db3ec-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="db3ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db3ec-102">SYNOPSIS</span></span>
<span data-ttu-id="db3ec-103">Crea un nuovo gruppo di azioni o aggiorna un gruppo di azioni esistente.</span><span class="sxs-lookup"><span data-stu-id="db3ec-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="db3ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db3ec-104">SYNTAX</span></span>

### <span data-ttu-id="db3ec-105">ByPropertyName (Default)</span><span class="sxs-lookup"><span data-stu-id="db3ec-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db3ec-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="db3ec-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db3ec-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="db3ec-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db3ec-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db3ec-108">DESCRIPTION</span></span>
<span data-ttu-id="db3ec-109">Il cmdlet **Set-AzActionGroup** crea una nuova azione o aggiorna un gruppo di azioni esistente</span><span class="sxs-lookup"><span data-stu-id="db3ec-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="db3ec-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db3ec-110">EXAMPLES</span></span>

### <span data-ttu-id="db3ec-111">Esempio 1: Creare un gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="db3ec-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="db3ec-112">I primi due comandi creano due ricevitori.</span><span class="sxs-lookup"><span data-stu-id="db3ec-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="db3ec-113">Il comando finale crea un gruppo di azioni che include i due ricevitori.</span><span class="sxs-lookup"><span data-stu-id="db3ec-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="db3ec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db3ec-114">PARAMETERS</span></span>

### <span data-ttu-id="db3ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db3ec-115">-DefaultProfile</span></span>
<span data-ttu-id="db3ec-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="db3ec-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db3ec-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="db3ec-117">-DisableGroup</span></span>
<span data-ttu-id="db3ec-118">Disabilita il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="db3ec-118">Disables the action group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db3ec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db3ec-119">-InputObject</span></span>
<span data-ttu-id="db3ec-120">Risorsa gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="db3ec-120">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db3ec-121">-Name</span><span class="sxs-lookup"><span data-stu-id="db3ec-121">-Name</span></span>
<span data-ttu-id="db3ec-122">Nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="db3ec-122">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db3ec-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="db3ec-123">-Receiver</span></span>
<span data-ttu-id="db3ec-124">L'elenco dei ricevitori del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="db3ec-124">The list of receivers of the action group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db3ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db3ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="db3ec-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="db3ec-126">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db3ec-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db3ec-127">-ResourceId</span></span>
<span data-ttu-id="db3ec-128">La risorsa i</span><span class="sxs-lookup"><span data-stu-id="db3ec-128">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db3ec-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="db3ec-129">-ShortName</span></span>
<span data-ttu-id="db3ec-130">Nome breve del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="db3ec-130">The short name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db3ec-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="db3ec-131">-Tag</span></span>
<span data-ttu-id="db3ec-132">Tag della risorsa del gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="db3ec-132">The tags of the action group resource</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db3ec-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db3ec-133">-Confirm</span></span>
<span data-ttu-id="db3ec-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db3ec-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db3ec-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db3ec-135">-WhatIf</span></span>
<span data-ttu-id="db3ec-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db3ec-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db3ec-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db3ec-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db3ec-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db3ec-138">CommonParameters</span></span>
<span data-ttu-id="db3ec-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db3ec-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db3ec-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db3ec-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db3ec-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="db3ec-141">INPUTS</span></span>

### <span data-ttu-id="db3ec-142">System.String</span><span class="sxs-lookup"><span data-stu-id="db3ec-142">System.String</span></span>

### <span data-ttu-id="db3ec-143">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="db3ec-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="db3ec-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db3ec-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="db3ec-145">System.Collections.Generic.IDictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="db3ec-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="db3ec-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="db3ec-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="db3ec-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db3ec-147">OUTPUTS</span></span>

### <span data-ttu-id="db3ec-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="db3ec-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="db3ec-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="db3ec-149">NOTES</span></span>

## <span data-ttu-id="db3ec-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db3ec-150">RELATED LINKS</span></span>

<span data-ttu-id="db3ec-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="db3ec-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>

