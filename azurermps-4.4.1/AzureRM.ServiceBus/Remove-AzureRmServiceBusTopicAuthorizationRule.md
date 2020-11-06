---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 5694d46e44931d59f79a5ac7b86ceabf7632f945
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521139"
---
# <span data-ttu-id="bb4cc-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bb4cc-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="bb4cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb4cc-102">SYNOPSIS</span></span>
<span data-ttu-id="bb4cc-103">Rimuove la regola di autorizzazione di un argomento dallo spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="bb4cc-103">Removes the authorization rule of a topic from the specified Service Bus Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb4cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb4cc-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb4cc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb4cc-105">DESCRIPTION</span></span>
<span data-ttu-id="bb4cc-106">Il cmdlet **Remove-AzureRmServiceBusTopicAuthorizationRule** rimuove la regola di autorizzazione di un argomento dallo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="bb4cc-106">The **Remove-AzureRmServiceBusTopicAuthorizationRule** cmdlet removes the authorization rule of a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bb4cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb4cc-107">EXAMPLES</span></span>

### <span data-ttu-id="bb4cc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bb4cc-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="bb4cc-109">Rimuove la regola `SBTopicAuthoRule1` di autorizzazione dell'argomento `SB-Topic_exampl1` dallo spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="bb4cc-109">Removes the authorization rule `SBTopicAuthoRule1` of the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="bb4cc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb4cc-110">PARAMETERS</span></span>

### <span data-ttu-id="bb4cc-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bb4cc-111">-ResourceGroup</span></span>
<span data-ttu-id="bb4cc-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bb4cc-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="bb4cc-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bb4cc-113">-Confirm</span></span>
<span data-ttu-id="bb4cc-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb4cc-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb4cc-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb4cc-115">-WhatIf</span></span>
<span data-ttu-id="bb4cc-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb4cc-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb4cc-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb4cc-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb4cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb4cc-118">-DefaultProfile</span></span>
<span data-ttu-id="bb4cc-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb4cc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb4cc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb4cc-120">-Name</span></span>
<span data-ttu-id="bb4cc-121">Argomento AuthorizationRule nome.</span><span class="sxs-lookup"><span data-stu-id="bb4cc-121">Topic AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb4cc-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bb4cc-122">-Namespace</span></span>
<span data-ttu-id="bb4cc-123">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="bb4cc-123">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb4cc-124">-Topic</span><span class="sxs-lookup"><span data-stu-id="bb4cc-124">-Topic</span></span>
<span data-ttu-id="bb4cc-125">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="bb4cc-125">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb4cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb4cc-126">CommonParameters</span></span>
<span data-ttu-id="bb4cc-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb4cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb4cc-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb4cc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb4cc-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb4cc-129">INPUTS</span></span>

### <span data-ttu-id="bb4cc-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bb4cc-130">-ResourceGroup</span></span>
 <span data-ttu-id="bb4cc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bb4cc-131">System.String</span></span>

### <span data-ttu-id="bb4cc-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="bb4cc-132">-NamespaceName</span></span>
 <span data-ttu-id="bb4cc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bb4cc-133">System.String</span></span>

### <span data-ttu-id="bb4cc-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="bb4cc-134">-TopicName</span></span>
 <span data-ttu-id="bb4cc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bb4cc-135">System.String</span></span>

### <span data-ttu-id="bb4cc-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="bb4cc-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="bb4cc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bb4cc-137">System.String</span></span>

## <span data-ttu-id="bb4cc-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb4cc-138">OUTPUTS</span></span>

### <span data-ttu-id="bb4cc-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="bb4cc-139">System.Object</span></span>

## <span data-ttu-id="bb4cc-140">Note</span><span class="sxs-lookup"><span data-stu-id="bb4cc-140">NOTES</span></span>

## <span data-ttu-id="bb4cc-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb4cc-141">RELATED LINKS</span></span>

