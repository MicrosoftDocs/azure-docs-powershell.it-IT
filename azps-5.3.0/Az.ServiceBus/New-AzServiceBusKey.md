---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: c0c413918a986da4eaea8d9ef5f0f6a091b8b2e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486068"
---
# <span data-ttu-id="b6a07-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="b6a07-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="b6a07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6a07-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a07-103">Rigenera le stringhe di connessione primarie o secondarie per lo spazio dei nomi Service Bus o la coda o l'argomento.</span><span class="sxs-lookup"><span data-stu-id="b6a07-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="b6a07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6a07-104">SYNTAX</span></span>

### <span data-ttu-id="b6a07-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6a07-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6a07-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6a07-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6a07-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b6a07-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6a07-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6a07-108">DESCRIPTION</span></span>
<span data-ttu-id="b6a07-109">Il cmdlet **New-AzServiceBusKey** genera nuove stringhe di connessione primarie o secondarie per lo spazio dei nomi o le code o gli argomenti e le regole di autorizzazione specificati.</span><span class="sxs-lookup"><span data-stu-id="b6a07-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="b6a07-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6a07-110">EXAMPLES</span></span>

### <span data-ttu-id="b6a07-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b6a07-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="b6a07-112">Rigenera le stringhe di connessione primarie o secondarie per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b6a07-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="b6a07-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b6a07-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="b6a07-114">Rigenera le stringhe di connessione primarie o secondarie con il valore di chiave specificato per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b6a07-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="b6a07-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b6a07-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="b6a07-116">Rigenera le stringhe di connessione primarie o secondarie per la coda.</span><span class="sxs-lookup"><span data-stu-id="b6a07-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="b6a07-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b6a07-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="b6a07-118">Rigenera le stringhe di connessione primarie o secondarie con il valore di chiave specificato per la coda.</span><span class="sxs-lookup"><span data-stu-id="b6a07-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="b6a07-119">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="b6a07-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="b6a07-120">Rigenera le stringhe di connessione primarie o secondarie per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="b6a07-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="b6a07-121">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="b6a07-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="b6a07-122">Rigenera le stringhe di connessione primarie o secondarie con il valore di chiave specificato per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="b6a07-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="b6a07-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6a07-123">PARAMETERS</span></span>

### <span data-ttu-id="b6a07-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a07-124">-DefaultProfile</span></span>
<span data-ttu-id="b6a07-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a07-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a07-126">-Valore della stessa</span><span class="sxs-lookup"><span data-stu-id="b6a07-126">-KeyValue</span></span>
<span data-ttu-id="b6a07-127">Una chiave a 256 bit con codifica Base64 per la firma e la convalida del token SAS.</span><span class="sxs-lookup"><span data-stu-id="b6a07-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="b6a07-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6a07-128">-Name</span></span>
<span data-ttu-id="b6a07-129">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="b6a07-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b6a07-130">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6a07-130">-Namespace</span></span>
<span data-ttu-id="b6a07-131">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6a07-131">Namespace Name</span></span>

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

### <span data-ttu-id="b6a07-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="b6a07-132">-Queue</span></span>
<span data-ttu-id="b6a07-133">Nome coda</span><span class="sxs-lookup"><span data-stu-id="b6a07-133">Queue Name</span></span>

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

### <span data-ttu-id="b6a07-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="b6a07-134">-RegenerateKey</span></span>
<span data-ttu-id="b6a07-135">Rigenera chiavi-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="b6a07-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="b6a07-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a07-136">-ResourceGroupName</span></span>
<span data-ttu-id="b6a07-137">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b6a07-137">Resource Group Name</span></span>

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

### <span data-ttu-id="b6a07-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="b6a07-138">-Topic</span></span>
<span data-ttu-id="b6a07-139">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="b6a07-139">Topic Name</span></span>

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

### <span data-ttu-id="b6a07-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b6a07-140">-Confirm</span></span>
<span data-ttu-id="b6a07-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6a07-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6a07-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a07-142">-WhatIf</span></span>
<span data-ttu-id="b6a07-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6a07-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6a07-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6a07-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6a07-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a07-145">CommonParameters</span></span>
<span data-ttu-id="b6a07-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a07-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a07-147">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a07-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a07-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6a07-148">INPUTS</span></span>

### <span data-ttu-id="b6a07-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a07-149">System.String</span></span>

## <span data-ttu-id="b6a07-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6a07-150">OUTPUTS</span></span>

### <span data-ttu-id="b6a07-151">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b6a07-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="b6a07-152">Note</span><span class="sxs-lookup"><span data-stu-id="b6a07-152">NOTES</span></span>

## <span data-ttu-id="b6a07-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6a07-153">RELATED LINKS</span></span>
