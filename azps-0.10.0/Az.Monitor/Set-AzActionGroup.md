---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: aad8ebb5b78163319ca0c6f56780bd0e336853f7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861062"
---
# <span data-ttu-id="f7f85-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="f7f85-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="f7f85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7f85-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f85-103">Crea un nuovo o aggiorna un gruppo di azioni esistente.</span><span class="sxs-lookup"><span data-stu-id="f7f85-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="f7f85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7f85-104">SYNTAX</span></span>

### <span data-ttu-id="f7f85-105">ByPropertyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7f85-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f85-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f7f85-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f85-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f7f85-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7f85-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7f85-108">DESCRIPTION</span></span>
<span data-ttu-id="f7f85-109">Il cmdlet **set-AzActionGroup** crea un nuovo o aggiorna un gruppo di azioni esistente</span><span class="sxs-lookup"><span data-stu-id="f7f85-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="f7f85-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7f85-110">EXAMPLES</span></span>

### <span data-ttu-id="f7f85-111">Esempio 1: creare un gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="f7f85-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="f7f85-112">I primi due comandi creano due destinatari.</span><span class="sxs-lookup"><span data-stu-id="f7f85-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="f7f85-113">Il comando finale crea un gruppo di azioni, inclusi i due destinatari.</span><span class="sxs-lookup"><span data-stu-id="f7f85-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="f7f85-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7f85-114">PARAMETERS</span></span>

### <span data-ttu-id="f7f85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f85-115">-DefaultProfile</span></span>
<span data-ttu-id="f7f85-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f7f85-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7f85-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="f7f85-117">-DisableGroup</span></span>
<span data-ttu-id="f7f85-118">Disabilita il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="f7f85-118">Disables the action group.</span></span>

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

### <span data-ttu-id="f7f85-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7f85-119">-InputObject</span></span>
<span data-ttu-id="f7f85-120">Risorsa gruppo azioni</span><span class="sxs-lookup"><span data-stu-id="f7f85-120">The action group resource</span></span>

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

### <span data-ttu-id="f7f85-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7f85-121">-Name</span></span>
<span data-ttu-id="f7f85-122">Nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="f7f85-122">The name of the action group.</span></span>

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

### <span data-ttu-id="f7f85-123">-Ricevitore</span><span class="sxs-lookup"><span data-stu-id="f7f85-123">-Receiver</span></span>
<span data-ttu-id="f7f85-124">Elenco dei destinatari del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="f7f85-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="f7f85-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f85-125">-ResourceGroupName</span></span>
<span data-ttu-id="f7f85-126">Gruppo risorse Nam</span><span class="sxs-lookup"><span data-stu-id="f7f85-126">The resource group nam</span></span>

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

### <span data-ttu-id="f7f85-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7f85-127">-ResourceId</span></span>
<span data-ttu-id="f7f85-128">Risorsa i</span><span class="sxs-lookup"><span data-stu-id="f7f85-128">The resource i</span></span>

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

### <span data-ttu-id="f7f85-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="f7f85-129">-ShortName</span></span>
<span data-ttu-id="f7f85-130">Nome breve del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="f7f85-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="f7f85-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="f7f85-131">-Tag</span></span>
<span data-ttu-id="f7f85-132">Tag della risorsa del gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="f7f85-132">The tags of the action group resource</span></span>

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

### <span data-ttu-id="f7f85-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7f85-133">-Confirm</span></span>
<span data-ttu-id="f7f85-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7f85-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f85-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f85-135">-WhatIf</span></span>
<span data-ttu-id="f7f85-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7f85-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7f85-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7f85-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f85-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f85-138">CommonParameters</span></span>
<span data-ttu-id="f7f85-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f85-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f85-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7f85-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f85-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7f85-141">INPUTS</span></span>

### <span data-ttu-id="f7f85-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f7f85-142">System.String</span></span>

### <span data-ttu-id="f7f85-143">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. PowerShell. Cmdlets. monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f7f85-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f7f85-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f7f85-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f7f85-145">System. Collections. Generic. IDictionary ' 2 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f7f85-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f7f85-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="f7f85-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="f7f85-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7f85-147">OUTPUTS</span></span>

### <span data-ttu-id="f7f85-148">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="f7f85-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="f7f85-149">Note</span><span class="sxs-lookup"><span data-stu-id="f7f85-149">NOTES</span></span>

## <span data-ttu-id="f7f85-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7f85-150">RELATED LINKS</span></span>

<span data-ttu-id="f7f85-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="f7f85-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
