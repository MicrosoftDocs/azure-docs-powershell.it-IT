---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 8be39cb4b4b173d3b87efbf0b7ecea72ae233061
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686518"
---
# <span data-ttu-id="6c33a-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="6c33a-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="6c33a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c33a-102">SYNOPSIS</span></span>
<span data-ttu-id="6c33a-103">Crea una nuova chiave primaria o secondaria per la regola di autorizzazione Hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="6c33a-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c33a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c33a-104">SYNTAX</span></span>

### <span data-ttu-id="6c33a-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c33a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c33a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6c33a-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c33a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c33a-107">DESCRIPTION</span></span>
<span data-ttu-id="6c33a-108">Il cmdlet New-AzureRmEventHubKey rigenera la chiave SAS primaria o secondaria per la regola di autorizzazione Hub eventi specificata.</span><span class="sxs-lookup"><span data-stu-id="6c33a-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="6c33a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c33a-109">EXAMPLES</span></span>

### <span data-ttu-id="6c33a-110">Esempio 1,1</span><span class="sxs-lookup"><span data-stu-id="6c33a-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="6c33a-111">Rigenera la chiave primaria per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="6c33a-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="6c33a-112">Esempio 1,2</span><span class="sxs-lookup"><span data-stu-id="6c33a-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="6c33a-113">Rigenera la chiave primaria per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="6c33a-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="6c33a-114">Esempio 2,1</span><span class="sxs-lookup"><span data-stu-id="6c33a-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="6c33a-115">Esempio 2,2</span><span class="sxs-lookup"><span data-stu-id="6c33a-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="6c33a-116">Rigenera la chiave secondaria per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="6c33a-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="6c33a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c33a-117">PARAMETERS</span></span>

### <span data-ttu-id="6c33a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c33a-118">-DefaultProfile</span></span>
<span data-ttu-id="6c33a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c33a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c33a-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6c33a-120">-EventHub</span></span>
<span data-ttu-id="6c33a-121">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="6c33a-121">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c33a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c33a-122">-Name</span></span>
<span data-ttu-id="6c33a-123">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6c33a-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c33a-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6c33a-124">-Namespace</span></span>
<span data-ttu-id="6c33a-125">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6c33a-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c33a-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="6c33a-126">-RegenerateKey</span></span>
<span data-ttu-id="6c33a-127">Rigenera chiavi-' PrimaryKey '/' SecondaryKey '</span><span class="sxs-lookup"><span data-stu-id="6c33a-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c33a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c33a-128">-ResourceGroupName</span></span>
<span data-ttu-id="6c33a-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="6c33a-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c33a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c33a-130">-Confirm</span></span>
<span data-ttu-id="6c33a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c33a-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c33a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c33a-132">-WhatIf</span></span>
<span data-ttu-id="6c33a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c33a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c33a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c33a-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c33a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c33a-135">CommonParameters</span></span>
<span data-ttu-id="6c33a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c33a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6c33a-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c33a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c33a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c33a-138">INPUTS</span></span>

### <span data-ttu-id="6c33a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6c33a-139">System.String</span></span>


## <span data-ttu-id="6c33a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c33a-140">OUTPUTS</span></span>

### <span data-ttu-id="6c33a-141">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="6c33a-141">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="6c33a-142">Note</span><span class="sxs-lookup"><span data-stu-id="6c33a-142">NOTES</span></span>

## <span data-ttu-id="6c33a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c33a-143">RELATED LINKS</span></span>
