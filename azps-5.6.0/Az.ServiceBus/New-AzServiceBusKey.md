---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: ac3b98089a3bbb710680269692685a32ef7adc03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950957"
---
# <span data-ttu-id="a7cf3-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="a7cf3-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="a7cf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="a7cf3-103">Rigenera le stringhe di connessione primaria o secondaria per lo spazio dei nomi o la coda o l'argomento del bus di servizio.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="a7cf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7cf3-104">SYNTAX</span></span>

### <span data-ttu-id="a7cf3-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a7cf3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7cf3-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7cf3-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7cf3-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7cf3-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7cf3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a7cf3-108">DESCRIPTION</span></span>
<span data-ttu-id="a7cf3-109">Il cmdlet **New-AzServiceBusKey** genera nuove stringhe di connessione primaria o secondaria per lo spazio dei nomi o la coda o l'argomento specificato e la regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="a7cf3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7cf3-110">EXAMPLES</span></span>

### <span data-ttu-id="a7cf3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a7cf3-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="a7cf3-112">Rigenera le stringhe di connessione primaria o secondaria per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="a7cf3-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a7cf3-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="a7cf3-114">Rigenera le stringhe di connessione primaria o secondaria con il valore chiave fornito per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="a7cf3-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a7cf3-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="a7cf3-116">Rigenera le stringhe di connessione primaria o secondaria per la coda.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="a7cf3-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="a7cf3-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="a7cf3-118">Rigenera le stringhe di connessione primaria o secondaria con il valore chiave fornito per la coda.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="a7cf3-119">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="a7cf3-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="a7cf3-120">Rigenera le stringhe di connessione primaria o secondaria per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="a7cf3-121">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="a7cf3-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="a7cf3-122">Rigenera le stringhe di connessione primaria o secondaria con il valore chiave fornito per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="a7cf3-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7cf3-123">PARAMETERS</span></span>

### <span data-ttu-id="a7cf3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7cf3-124">-DefaultProfile</span></span>
<span data-ttu-id="a7cf3-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7cf3-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="a7cf3-126">-KeyValue</span></span>
<span data-ttu-id="a7cf3-127">Chiave a 256 bit codificata in base64 per firmare e convalidare il token di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7cf3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a7cf3-128">-Name</span></span>
<span data-ttu-id="a7cf3-129">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-129">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7cf3-130">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7cf3-130">-Namespace</span></span>
<span data-ttu-id="a7cf3-131">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7cf3-131">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7cf3-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="a7cf3-132">-Queue</span></span>
<span data-ttu-id="a7cf3-133">Nome coda</span><span class="sxs-lookup"><span data-stu-id="a7cf3-133">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7cf3-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="a7cf3-134">-RegenerateKey</span></span>
<span data-ttu-id="a7cf3-135">Rigenerare le chiavi - 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7cf3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7cf3-136">-ResourceGroupName</span></span>
<span data-ttu-id="a7cf3-137">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a7cf3-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7cf3-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="a7cf3-138">-Topic</span></span>
<span data-ttu-id="a7cf3-139">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="a7cf3-139">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7cf3-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7cf3-140">-Confirm</span></span>
<span data-ttu-id="a7cf3-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7cf3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7cf3-142">-WhatIf</span></span>
<span data-ttu-id="a7cf3-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7cf3-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7cf3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7cf3-145">CommonParameters</span></span>
<span data-ttu-id="a7cf3-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7cf3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7cf3-147">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7cf3-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7cf3-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="a7cf3-148">INPUTS</span></span>

### <span data-ttu-id="a7cf3-149">System.String</span><span class="sxs-lookup"><span data-stu-id="a7cf3-149">System.String</span></span>

## <span data-ttu-id="a7cf3-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7cf3-150">OUTPUTS</span></span>

### <span data-ttu-id="a7cf3-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="a7cf3-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="a7cf3-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="a7cf3-152">NOTES</span></span>

## <span data-ttu-id="a7cf3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7cf3-153">RELATED LINKS</span></span>
