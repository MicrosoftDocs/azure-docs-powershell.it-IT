---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 287a0b82c9236841b613ac52a7a07ccf8adb4811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512952"
---
# <span data-ttu-id="79002-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="79002-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="79002-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79002-102">SYNOPSIS</span></span>
<span data-ttu-id="79002-103">Rimuove la regola speficied di un abbonamento specifico.</span><span class="sxs-lookup"><span data-stu-id="79002-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79002-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79002-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79002-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79002-105">DESCRIPTION</span></span>
<span data-ttu-id="79002-106">Il cmdlet **Remove-AzureRmServiceBusRule** rimuove la regola di una sottoscrizione di un argomento specifico.</span><span class="sxs-lookup"><span data-stu-id="79002-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="79002-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79002-107">EXAMPLES</span></span>

### <span data-ttu-id="79002-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79002-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="79002-109">Rimuove la regola `SBRule` di sottoscrizione `SBSubscription` dell'argomento specificato `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="79002-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="79002-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79002-110">PARAMETERS</span></span>

### <span data-ttu-id="79002-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79002-111">-Confirm</span></span>
<span data-ttu-id="79002-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79002-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79002-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="79002-113">-Name</span></span>
<span data-ttu-id="79002-114">Nome della regola.</span><span class="sxs-lookup"><span data-stu-id="79002-114">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79002-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="79002-115">-Namespace</span></span>
<span data-ttu-id="79002-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="79002-116">Namespace Name.</span></span>

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

### <span data-ttu-id="79002-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79002-117">-ResourceGroupName</span></span>
<span data-ttu-id="79002-118">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="79002-118">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79002-119">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="79002-119">-Subscription</span></span>
<span data-ttu-id="79002-120">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="79002-120">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79002-121">-Topic</span><span class="sxs-lookup"><span data-stu-id="79002-121">-Topic</span></span>
<span data-ttu-id="79002-122">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="79002-122">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79002-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79002-123">-WhatIf</span></span>
<span data-ttu-id="79002-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79002-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79002-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79002-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79002-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79002-126">-DefaultProfile</span></span>
<span data-ttu-id="79002-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79002-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79002-128">-Force</span><span class="sxs-lookup"><span data-stu-id="79002-128">-Force</span></span>
<span data-ttu-id="79002-129">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="79002-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="79002-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79002-130">-PassThru</span></span>
<span data-ttu-id="79002-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="79002-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="79002-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79002-132">CommonParameters</span></span>
<span data-ttu-id="79002-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79002-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79002-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79002-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79002-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79002-135">INPUTS</span></span>

### <span data-ttu-id="79002-136">System. String</span><span class="sxs-lookup"><span data-stu-id="79002-136">System.String</span></span>

## <span data-ttu-id="79002-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79002-137">OUTPUTS</span></span>

### <span data-ttu-id="79002-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79002-138">System.Boolean</span></span>

## <span data-ttu-id="79002-139">Note</span><span class="sxs-lookup"><span data-stu-id="79002-139">NOTES</span></span>

## <span data-ttu-id="79002-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79002-140">RELATED LINKS</span></span>

