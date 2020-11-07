---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 35e3889603dc7e86a7d10679864adfd34a880b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686077"
---
# <span data-ttu-id="9a51a-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9a51a-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="9a51a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a51a-102">SYNOPSIS</span></span>
<span data-ttu-id="9a51a-103">Rimuove la regola di autorizzazione dell'hub eventi specificata.</span><span class="sxs-lookup"><span data-stu-id="9a51a-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a51a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a51a-104">SYNTAX</span></span>

### <span data-ttu-id="9a51a-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9a51a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a51a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9a51a-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a51a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a51a-107">DESCRIPTION</span></span>
<span data-ttu-id="9a51a-108">Il cmdlet Remove-AzureRmEventHubAuthorizationRule rimuove ed elimina la regola di autorizzazione specificata dall'hub dell'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="9a51a-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="9a51a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a51a-109">EXAMPLES</span></span>

### <span data-ttu-id="9a51a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a51a-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="9a51a-111">Rimuove la regola \` di autorizzazione MyAuthRuleName \` dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="9a51a-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="9a51a-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9a51a-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="9a51a-113">Rimuove la regola \` di autorizzazione MyAuthRuleName \` dall'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="9a51a-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="9a51a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a51a-114">PARAMETERS</span></span>

### <span data-ttu-id="9a51a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a51a-115">-DefaultProfile</span></span>
<span data-ttu-id="9a51a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a51a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a51a-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="9a51a-117">-EventHub</span></span>
<span data-ttu-id="9a51a-118">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="9a51a-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a51a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9a51a-119">-Force</span></span>
<span data-ttu-id="9a51a-120">Non chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="9a51a-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="9a51a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a51a-121">-Name</span></span>
<span data-ttu-id="9a51a-122">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9a51a-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="9a51a-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9a51a-123">-Namespace</span></span>
<span data-ttu-id="9a51a-124">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9a51a-124">Namespace Name</span></span>

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

### <span data-ttu-id="9a51a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a51a-125">-PassThru</span></span>
<span data-ttu-id="9a51a-126">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="9a51a-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a51a-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9a51a-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a51a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a51a-128">-ResourceGroupName</span></span>
<span data-ttu-id="9a51a-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9a51a-129">Resource Group Name</span></span>

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

### <span data-ttu-id="9a51a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9a51a-130">-Confirm</span></span>
<span data-ttu-id="9a51a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a51a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a51a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a51a-132">-WhatIf</span></span>
<span data-ttu-id="9a51a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a51a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a51a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a51a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a51a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a51a-135">CommonParameters</span></span>
<span data-ttu-id="9a51a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a51a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a51a-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a51a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a51a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a51a-138">INPUTS</span></span>

### <span data-ttu-id="9a51a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9a51a-139">System.String</span></span>

## <span data-ttu-id="9a51a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a51a-140">OUTPUTS</span></span>

### <span data-ttu-id="9a51a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a51a-141">System.Boolean</span></span>

## <span data-ttu-id="9a51a-142">Note</span><span class="sxs-lookup"><span data-stu-id="9a51a-142">NOTES</span></span>

## <span data-ttu-id="9a51a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a51a-143">RELATED LINKS</span></span>
