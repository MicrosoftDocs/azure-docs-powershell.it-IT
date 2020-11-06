---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 6efd58497adc1e59f1bf6d2c2151386ee773f66a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519693"
---
# <span data-ttu-id="9120c-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="9120c-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="9120c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9120c-102">SYNOPSIS</span></span>
<span data-ttu-id="9120c-103">Rigenera le stringhe di connessione primarie o secondarie per lo spazio dei nomi Service Bus o la coda o l'argomento.</span><span class="sxs-lookup"><span data-stu-id="9120c-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9120c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9120c-104">SYNTAX</span></span>

### <span data-ttu-id="9120c-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9120c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9120c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9120c-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9120c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9120c-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9120c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9120c-108">DESCRIPTION</span></span>
<span data-ttu-id="9120c-109">Il cmdlet **New-AzureRmServiceBusKey** genera nuove stringhe di connessione primarie o secondarie per lo spazio dei nomi o le code o gli argomenti e le regole di autorizzazione specificati.</span><span class="sxs-lookup"><span data-stu-id="9120c-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="9120c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9120c-110">EXAMPLES</span></span>

### <span data-ttu-id="9120c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9120c-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="9120c-112">Rigenera le stringhe di connessione primarie o secondarie per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9120c-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="9120c-113">Esempio 1,1</span><span class="sxs-lookup"><span data-stu-id="9120c-113">Example 1.1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="9120c-114">Rigenera le stringhe di connessione primarie o secondarie con il valore di chiave specificato per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9120c-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="9120c-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9120c-115">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="9120c-116">Rigenera le stringhe di connessione primarie o secondarie per la coda.</span><span class="sxs-lookup"><span data-stu-id="9120c-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="9120c-117">Esempio 2,2</span><span class="sxs-lookup"><span data-stu-id="9120c-117">Example 2.2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="9120c-118">Rigenera le stringhe di connessione primarie o secondarie con il valore di chiave specificato per la coda.</span><span class="sxs-lookup"><span data-stu-id="9120c-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="9120c-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9120c-119">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="9120c-120">Rigenera le stringhe di connessione primarie o secondarie per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="9120c-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="9120c-121">Esempio 3,1</span><span class="sxs-lookup"><span data-stu-id="9120c-121">Example 3.1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="9120c-122">Rigenera le stringhe di connessione primarie o secondarie con il valore di chiave specificato per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="9120c-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="9120c-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9120c-123">PARAMETERS</span></span>

### <span data-ttu-id="9120c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9120c-124">-DefaultProfile</span></span>
<span data-ttu-id="9120c-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9120c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9120c-126">-Valore della stessa</span><span class="sxs-lookup"><span data-stu-id="9120c-126">-KeyValue</span></span>
<span data-ttu-id="9120c-127">Una chiave a 256 bit con codifica Base64 per la firma e la convalida del token SAS.</span><span class="sxs-lookup"><span data-stu-id="9120c-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="9120c-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9120c-128">-Name</span></span>
<span data-ttu-id="9120c-129">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="9120c-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="9120c-130">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9120c-130">-Namespace</span></span>
<span data-ttu-id="9120c-131">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9120c-131">Namespace Name</span></span>

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

### <span data-ttu-id="9120c-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="9120c-132">-Queue</span></span>
<span data-ttu-id="9120c-133">Nome coda</span><span class="sxs-lookup"><span data-stu-id="9120c-133">Queue Name</span></span>

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

### <span data-ttu-id="9120c-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="9120c-134">-RegenerateKey</span></span>
<span data-ttu-id="9120c-135">Rigenera chiavi-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="9120c-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="9120c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9120c-136">-ResourceGroupName</span></span>
<span data-ttu-id="9120c-137">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9120c-137">Resource Group Name</span></span>

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

### <span data-ttu-id="9120c-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="9120c-138">-Topic</span></span>
<span data-ttu-id="9120c-139">Nome argomento</span><span class="sxs-lookup"><span data-stu-id="9120c-139">Topic Name</span></span>

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

### <span data-ttu-id="9120c-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9120c-140">-Confirm</span></span>
<span data-ttu-id="9120c-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9120c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9120c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9120c-142">-WhatIf</span></span>
<span data-ttu-id="9120c-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9120c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9120c-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9120c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9120c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9120c-145">CommonParameters</span></span>
<span data-ttu-id="9120c-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9120c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9120c-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9120c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9120c-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9120c-148">INPUTS</span></span>

### <span data-ttu-id="9120c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="9120c-149">System.String</span></span>

## <span data-ttu-id="9120c-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9120c-150">OUTPUTS</span></span>

### <span data-ttu-id="9120c-151">Microsoft. Azure. Commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="9120c-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="9120c-152">Note</span><span class="sxs-lookup"><span data-stu-id="9120c-152">NOTES</span></span>

## <span data-ttu-id="9120c-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9120c-153">RELATED LINKS</span></span>
