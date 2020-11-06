---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: 29ef822e61c13d3ea976002c465a7c114296da9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519582"
---
# <span data-ttu-id="1c4bd-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="1c4bd-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="1c4bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4bd-103">Crea un nuovo o aggiorna un gruppo di azioni esistente.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c4bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c4bd-104">SYNTAX</span></span>

### <span data-ttu-id="1c4bd-105">ByPropertyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c4bd-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c4bd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c4bd-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c4bd-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1c4bd-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c4bd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c4bd-108">DESCRIPTION</span></span>
<span data-ttu-id="1c4bd-109">Il cmdlet **set-AzureRmActionGroup** crea un nuovo o aggiorna un gruppo di azioni esistente</span><span class="sxs-lookup"><span data-stu-id="1c4bd-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="1c4bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c4bd-110">EXAMPLES</span></span>

### <span data-ttu-id="1c4bd-111">Esempio 1: creare un gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="1c4bd-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="1c4bd-112">I primi due comandi creano due destinatari.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="1c4bd-113">Il comando finale crea un gruppo di azioni, inclusi i due destinatari.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="1c4bd-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c4bd-114">PARAMETERS</span></span>

### <span data-ttu-id="1c4bd-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c4bd-115">-Name</span></span>
<span data-ttu-id="1c4bd-116">Nome del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-116">The name of the action group.</span></span>

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

### <span data-ttu-id="1c4bd-117">-ShortName</span><span class="sxs-lookup"><span data-stu-id="1c4bd-117">-ShortName</span></span>
<span data-ttu-id="1c4bd-118">Nome breve del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-118">The short name of the action group.</span></span>

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

### <span data-ttu-id="1c4bd-119">-Ricevitore</span><span class="sxs-lookup"><span data-stu-id="1c4bd-119">-Receiver</span></span>
<span data-ttu-id="1c4bd-120">Elenco dei destinatari del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-120">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="1c4bd-121">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="1c4bd-121">-DisableGroup</span></span>
<span data-ttu-id="1c4bd-122">Disabilita il gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-122">Disables the action group.</span></span>

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

### <span data-ttu-id="1c4bd-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1c4bd-123">-Confirm</span></span>
<span data-ttu-id="1c4bd-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c4bd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4bd-125">-DefaultProfile</span></span>
<span data-ttu-id="1c4bd-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c4bd-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c4bd-127">-InputObject</span></span>
<span data-ttu-id="1c4bd-128">Risorsa gruppo azioni</span><span class="sxs-lookup"><span data-stu-id="1c4bd-128">The action group resource</span></span>

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

### <span data-ttu-id="1c4bd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c4bd-129">-ResourceGroupName</span></span>
<span data-ttu-id="1c4bd-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1c4bd-130">The resource group name</span></span>

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

### <span data-ttu-id="1c4bd-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c4bd-131">-ResourceId</span></span>
<span data-ttu-id="1c4bd-132">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="1c4bd-132">The resource id</span></span>

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

### <span data-ttu-id="1c4bd-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c4bd-133">-Tag</span></span>
<span data-ttu-id="1c4bd-134">Tag della risorsa del gruppo di azioni</span><span class="sxs-lookup"><span data-stu-id="1c4bd-134">The tags of the action group resource</span></span>

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

### <span data-ttu-id="1c4bd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c4bd-135">-WhatIf</span></span>
<span data-ttu-id="1c4bd-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c4bd-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c4bd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4bd-138">CommonParameters</span></span>
<span data-ttu-id="1c4bd-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c4bd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4bd-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c4bd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4bd-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c4bd-141">INPUTS</span></span>

## <span data-ttu-id="1c4bd-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c4bd-142">OUTPUTS</span></span>

### <span data-ttu-id="1c4bd-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="1c4bd-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="1c4bd-144">Note</span><span class="sxs-lookup"><span data-stu-id="1c4bd-144">NOTES</span></span>

## <span data-ttu-id="1c4bd-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c4bd-145">RELATED LINKS</span></span>

<span data-ttu-id="1c4bd-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="1c4bd-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
