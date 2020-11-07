---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0483c60a1624374dc3e5b750439d905f19ceb2fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687692"
---
# <span data-ttu-id="2021d-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="2021d-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="2021d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2021d-102">SYNOPSIS</span></span>
<span data-ttu-id="2021d-103">Rigenera le stringhe di connessione primarie o secondarie per lo spazio dei nomi Service Bus o la coda o l'argomento.</span><span class="sxs-lookup"><span data-stu-id="2021d-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2021d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2021d-104">SYNTAX</span></span>

### <span data-ttu-id="2021d-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2021d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2021d-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2021d-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2021d-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2021d-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2021d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2021d-108">DESCRIPTION</span></span>
<span data-ttu-id="2021d-109">Il cmdlet **New-AzureRmServiceBusKey** genera nuove stringhe di connessione primarie o secondarie per lo spazio dei nomi o le code o gli argomenti e le regole di autorizzazione specificati.</span><span class="sxs-lookup"><span data-stu-id="2021d-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="2021d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2021d-110">EXAMPLES</span></span>

### <span data-ttu-id="2021d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2021d-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="2021d-112">Rigenera le stringhe di connessione primarie o secondarie per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="2021d-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="2021d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2021d-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="2021d-114">Rigenera le stringhe di connessione primarie o secondarie per la coda.</span><span class="sxs-lookup"><span data-stu-id="2021d-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="2021d-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="2021d-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="2021d-116">Rigenera le stringhe di connessione primarie o secondarie per l'argomento.</span><span class="sxs-lookup"><span data-stu-id="2021d-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="2021d-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2021d-117">PARAMETERS</span></span>

### <span data-ttu-id="2021d-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2021d-118">-Confirm</span></span>
<span data-ttu-id="2021d-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2021d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2021d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2021d-120">-Name</span></span>
<span data-ttu-id="2021d-121">Nome AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="2021d-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2021d-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2021d-122">-Namespace</span></span>
<span data-ttu-id="2021d-123">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="2021d-123">Namespace Name.</span></span>

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

### <span data-ttu-id="2021d-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="2021d-124">-Queue</span></span>
<span data-ttu-id="2021d-125">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="2021d-125">Queue Name.</span></span>

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

### <span data-ttu-id="2021d-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="2021d-126">-RegenerateKey</span></span>
<span data-ttu-id="2021d-127">Rigenera chiavi-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="2021d-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2021d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2021d-128">-ResourceGroupName</span></span>
<span data-ttu-id="2021d-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2021d-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="2021d-130">-Topic</span><span class="sxs-lookup"><span data-stu-id="2021d-130">-Topic</span></span>
<span data-ttu-id="2021d-131">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="2021d-131">Topic Name.</span></span>

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

### <span data-ttu-id="2021d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2021d-132">-WhatIf</span></span>
<span data-ttu-id="2021d-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2021d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2021d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2021d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2021d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2021d-135">-DefaultProfile</span></span>
<span data-ttu-id="2021d-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2021d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2021d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2021d-137">CommonParameters</span></span>
<span data-ttu-id="2021d-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2021d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2021d-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2021d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2021d-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2021d-140">INPUTS</span></span>

### <span data-ttu-id="2021d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2021d-141">System.String</span></span>

## <span data-ttu-id="2021d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2021d-142">OUTPUTS</span></span>

### <span data-ttu-id="2021d-143">Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="2021d-143">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="2021d-144">Note</span><span class="sxs-lookup"><span data-stu-id="2021d-144">NOTES</span></span>

## <span data-ttu-id="2021d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2021d-145">RELATED LINKS</span></span>

