---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: bae9d8814d5988d0d509f64cb1de10040bb1af00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521855"
---
# <span data-ttu-id="a5e30-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a5e30-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="a5e30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5e30-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e30-103">Crea un nuovo o aggiorna un gruppo di azioni esistente.</span><span class="sxs-lookup"><span data-stu-id="a5e30-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5e30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5e30-104">SYNTAX</span></span>

### <span data-ttu-id="a5e30-105">ByPropertyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5e30-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e30-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e30-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e30-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5e30-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5e30-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5e30-108">DESCRIPTION</span></span>
<span data-ttu-id="a5e30-109">Il cmdlet **set-AzureRmActionGroup** crea un nuovo o aggiorna un gruppo di azioni esistente</span><span class="sxs-lookup"><span data-stu-id="a5e30-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="a5e30-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5e30-110">EXAMPLES</span></span>

### <span data-ttu-id="a5e30-111">Esempio 1: creare un gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="a5e30-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="a5e30-112">I primi due comandi creano due destinatari.</span><span class="sxs-lookup"><span data-stu-id="a5e30-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="a5e30-113">Il comando finale crea un gruppo di azioni, inclusi i due destinatari.</span><span class="sxs-lookup"><span data-stu-id="a5e30-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="a5e30-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5e30-114">PARAMETERS</span></span>

### <span data-ttu-id="a5e30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e30-115">-DefaultProfile</span></span>
<span data-ttu-id="a5e30-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a5e30-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5e30-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="a5e30-117">-DisableGroup</span></span>
<span data-ttu-id="a5e30-118">Disabilita il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="a5e30-118">Disables the action group.</span></span>

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

### <span data-ttu-id="a5e30-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5e30-119">-InputObject</span></span>
<span data-ttu-id="a5e30-120">Gruppo di azioni resourc</span><span class="sxs-lookup"><span data-stu-id="a5e30-120">The action group resourc</span></span>

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

### <span data-ttu-id="a5e30-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a5e30-121">-Name</span></span>
<span data-ttu-id="a5e30-122">Nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="a5e30-122">The name of the action group.</span></span>

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

### <span data-ttu-id="a5e30-123">-Ricevitore</span><span class="sxs-lookup"><span data-stu-id="a5e30-123">-Receiver</span></span>
<span data-ttu-id="a5e30-124">Elenco dei destinatari del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="a5e30-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="a5e30-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e30-125">-ResourceGroupName</span></span>
<span data-ttu-id="a5e30-126">Gruppo risorse Nam</span><span class="sxs-lookup"><span data-stu-id="a5e30-126">The resource group nam</span></span>

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

### <span data-ttu-id="a5e30-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e30-127">-ResourceId</span></span>
<span data-ttu-id="a5e30-128">Risorsa i</span><span class="sxs-lookup"><span data-stu-id="a5e30-128">The resource i</span></span>

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

### <span data-ttu-id="a5e30-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="a5e30-129">-ShortName</span></span>
<span data-ttu-id="a5e30-130">Nome breve del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="a5e30-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="a5e30-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="a5e30-131">-Tag</span></span>
<span data-ttu-id="a5e30-132">Tag del gruppo di azioni resourc</span><span class="sxs-lookup"><span data-stu-id="a5e30-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="a5e30-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5e30-133">-Confirm</span></span>
<span data-ttu-id="a5e30-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5e30-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e30-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e30-135">-WhatIf</span></span>
<span data-ttu-id="a5e30-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5e30-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5e30-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5e30-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e30-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e30-138">CommonParameters</span></span>
<span data-ttu-id="a5e30-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e30-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e30-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e30-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e30-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5e30-141">INPUTS</span></span>

### <span data-ttu-id="a5e30-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e30-142">System.String</span></span>

### <span data-ttu-id="a5e30-143">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a5e30-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a5e30-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a5e30-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a5e30-145">System. Collections. Generic. IDictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a5e30-145">System.Collections.Generic.IDictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a5e30-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="a5e30-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="a5e30-147">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5e30-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a5e30-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5e30-148">OUTPUTS</span></span>

### <span data-ttu-id="a5e30-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="a5e30-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="a5e30-150">Note</span><span class="sxs-lookup"><span data-stu-id="a5e30-150">NOTES</span></span>

## <span data-ttu-id="a5e30-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5e30-151">RELATED LINKS</span></span>

<span data-ttu-id="a5e30-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="a5e30-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
