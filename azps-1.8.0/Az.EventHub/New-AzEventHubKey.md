---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: bb66aacb406871731cb2f356c19a91e8bb27429c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678791"
---
# <span data-ttu-id="5a9c6-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="5a9c6-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="5a9c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a9c6-102">SYNOPSIS</span></span>
<span data-ttu-id="5a9c6-103">Crea una nuova chiave primaria o secondaria per la regola di autorizzazione Hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="5a9c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a9c6-104">SYNTAX</span></span>

### <span data-ttu-id="5a9c6-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a9c6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a9c6-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a9c6-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a9c6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a9c6-107">DESCRIPTION</span></span>
<span data-ttu-id="5a9c6-108">Il cmdlet New-AzEventHubKey rigenera la chiave SAS primaria o secondaria per la regola di autorizzazione Hub eventi specificata.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="5a9c6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a9c6-109">EXAMPLES</span></span>

### <span data-ttu-id="5a9c6-110">Esempio 1,1-spazio dei nomi-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="5a9c6-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="5a9c6-111">Rigenera la chiave primaria per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="5a9c6-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="5a9c6-112">Esempio 1,2-EventHub-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="5a9c6-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="5a9c6-113">Rigenera la chiave primaria per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="5a9c6-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="5a9c6-114">Esempio 2,1-spazio dei nomi-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="5a9c6-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="5a9c6-115">Esempio 2,2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="5a9c6-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="5a9c6-116">Rigenera la chiave secondaria per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="5a9c6-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="5a9c6-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a9c6-117">PARAMETERS</span></span>

### <span data-ttu-id="5a9c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a9c6-118">-DefaultProfile</span></span>
<span data-ttu-id="5a9c6-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a9c6-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5a9c6-120">-EventHub</span></span>
<span data-ttu-id="5a9c6-121">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="5a9c6-121">EventHub Name</span></span>

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

### <span data-ttu-id="5a9c6-122">-Valore della stessa</span><span class="sxs-lookup"><span data-stu-id="5a9c6-122">-KeyValue</span></span>
<span data-ttu-id="5a9c6-123">Una chiave a 256 bit con codifica Base64 per la firma e la convalida del token SAS.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a9c6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a9c6-124">-Name</span></span>
<span data-ttu-id="5a9c6-125">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5a9c6-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="5a9c6-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5a9c6-126">-Namespace</span></span>
<span data-ttu-id="5a9c6-127">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5a9c6-127">Namespace Name</span></span>

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

### <span data-ttu-id="5a9c6-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="5a9c6-128">-RegenerateKey</span></span>
<span data-ttu-id="5a9c6-129">Rigenera chiavi-' PrimaryKey '/' SecondaryKey '</span><span class="sxs-lookup"><span data-stu-id="5a9c6-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a9c6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a9c6-130">-ResourceGroupName</span></span>
<span data-ttu-id="5a9c6-131">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5a9c6-131">Resource Group Name</span></span>

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

### <span data-ttu-id="5a9c6-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a9c6-132">-Confirm</span></span>
<span data-ttu-id="5a9c6-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a9c6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a9c6-134">-WhatIf</span></span>
<span data-ttu-id="5a9c6-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a9c6-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a9c6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a9c6-137">CommonParameters</span></span>
<span data-ttu-id="5a9c6-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a9c6-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a9c6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a9c6-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a9c6-140">INPUTS</span></span>

### <span data-ttu-id="5a9c6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5a9c6-141">System.String</span></span>

## <span data-ttu-id="5a9c6-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a9c6-142">OUTPUTS</span></span>

### <span data-ttu-id="5a9c6-143">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="5a9c6-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="5a9c6-144">Note</span><span class="sxs-lookup"><span data-stu-id="5a9c6-144">NOTES</span></span>

## <span data-ttu-id="5a9c6-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a9c6-145">RELATED LINKS</span></span>
