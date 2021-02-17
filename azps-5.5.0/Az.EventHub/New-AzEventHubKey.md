---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: 477884e676118f461578be500715fd3698957003
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196326"
---
# <span data-ttu-id="4075e-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="4075e-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="4075e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4075e-102">SYNOPSIS</span></span>
<span data-ttu-id="4075e-103">Crea una nuova chiave primaria o secondaria per la regola di autorizzazione hub eventi specificata.</span><span class="sxs-lookup"><span data-stu-id="4075e-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="4075e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4075e-104">SYNTAX</span></span>

### <span data-ttu-id="4075e-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4075e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4075e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4075e-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4075e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4075e-107">DESCRIPTION</span></span>
<span data-ttu-id="4075e-108">Il cmdlet New-AzEventHubKey rigenera la chiave di firma di accesso condiviso primaria o secondaria per la regola di autorizzazione Hub eventi specificata.</span><span class="sxs-lookup"><span data-stu-id="4075e-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="4075e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4075e-109">EXAMPLES</span></span>

### <span data-ttu-id="4075e-110">Esempio 1: Spazio dei nomi - AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4075e-110">Example 1: Namespace - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="4075e-111">Rigenera la chiave primaria per la regola di autorizzazione \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="4075e-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="4075e-112">Esempio 2: EventHub - AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4075e-112">Example 2: EventHub - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="4075e-113">Rigenera la chiave primaria per la regola di autorizzazione \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="4075e-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="4075e-114">Esempio 3: - Spazio dei nomi - AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4075e-114">Example 3: - Namespace - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="4075e-115">Esempio 4: EventHub - AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4075e-115">Example 4: EventHub - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="4075e-116">Rigenera la chiave secondaria per la regola di autorizzazione \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="4075e-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="4075e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4075e-117">PARAMETERS</span></span>

### <span data-ttu-id="4075e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4075e-118">-DefaultProfile</span></span>
<span data-ttu-id="4075e-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4075e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4075e-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4075e-120">-EventHub</span></span>
<span data-ttu-id="4075e-121">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="4075e-121">EventHub Name</span></span>

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

### <span data-ttu-id="4075e-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="4075e-122">-KeyValue</span></span>
<span data-ttu-id="4075e-123">Chiave a 256 bit codificata in base64 per firmare e convalidare il token di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="4075e-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="4075e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4075e-124">-Name</span></span>
<span data-ttu-id="4075e-125">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="4075e-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="4075e-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4075e-126">-Namespace</span></span>
<span data-ttu-id="4075e-127">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4075e-127">Namespace Name</span></span>

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

### <span data-ttu-id="4075e-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="4075e-128">-RegenerateKey</span></span>
<span data-ttu-id="4075e-129">Rigenerare le chiavi - 'PrimaryKey'/'SecondaryKey'</span><span class="sxs-lookup"><span data-stu-id="4075e-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="4075e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4075e-130">-ResourceGroupName</span></span>
<span data-ttu-id="4075e-131">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4075e-131">Resource Group Name</span></span>

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

### <span data-ttu-id="4075e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4075e-132">-Confirm</span></span>
<span data-ttu-id="4075e-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4075e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4075e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4075e-134">-WhatIf</span></span>
<span data-ttu-id="4075e-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4075e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4075e-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4075e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4075e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4075e-137">CommonParameters</span></span>
<span data-ttu-id="4075e-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4075e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4075e-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4075e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4075e-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="4075e-140">INPUTS</span></span>

### <span data-ttu-id="4075e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4075e-141">System.String</span></span>

## <span data-ttu-id="4075e-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4075e-142">OUTPUTS</span></span>

### <span data-ttu-id="4075e-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="4075e-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="4075e-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="4075e-144">NOTES</span></span>

## <span data-ttu-id="4075e-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4075e-145">RELATED LINKS</span></span>
