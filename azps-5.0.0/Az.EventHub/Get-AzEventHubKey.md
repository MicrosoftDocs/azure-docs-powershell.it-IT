---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 0b77c4e4329577443e37054ce9861e246720e706
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202149"
---
# <span data-ttu-id="9d130-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="9d130-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="9d130-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d130-102">SYNOPSIS</span></span>
<span data-ttu-id="9d130-103">Ottiene i dettagli della chiave primaria della regola di autorizzazione degli hub di eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="9d130-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="9d130-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d130-104">SYNTAX</span></span>

### <span data-ttu-id="9d130-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d130-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d130-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9d130-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d130-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="9d130-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d130-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d130-108">DESCRIPTION</span></span>
<span data-ttu-id="9d130-109">Il cmdlet Get-AzEventHubKey restituisce le caratteristiche connectionStrings primarie e secondarie e i dettagli delle chiavi della regola di autorizzazione per lo spazio dei nomi/eventi/alias.</span><span class="sxs-lookup"><span data-stu-id="9d130-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="9d130-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d130-110">EXAMPLES</span></span>

### <span data-ttu-id="9d130-111">Esempio 1: spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d130-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="9d130-112">Esempio 2: EventHub</span><span class="sxs-lookup"><span data-stu-id="9d130-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="9d130-113">Ottiene i dettagli delle caratteristiche connectionStrings primarie e secondarie e delle chiavi per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="9d130-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="9d130-114">Esempio 3: alias (configurazione georecovery)</span><span class="sxs-lookup"><span data-stu-id="9d130-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="9d130-115">Ottiene i dettagli delle caratteristiche connectionStrings primarie, secondarie, AliasPrimary e AliasSecondary e delle chiavi per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="9d130-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="9d130-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d130-116">PARAMETERS</span></span>

### <span data-ttu-id="9d130-117">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="9d130-117">-AliasName</span></span>
<span data-ttu-id="9d130-118">Nome alias</span><span class="sxs-lookup"><span data-stu-id="9d130-118">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d130-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d130-119">-DefaultProfile</span></span>
<span data-ttu-id="9d130-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d130-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d130-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="9d130-121">-EventHub</span></span>
<span data-ttu-id="9d130-122">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="9d130-122">EventHub Name</span></span>

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

### <span data-ttu-id="9d130-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d130-123">-Name</span></span>
<span data-ttu-id="9d130-124">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9d130-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="9d130-125">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d130-125">-Namespace</span></span>
<span data-ttu-id="9d130-126">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d130-126">Namespace Name</span></span>

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

### <span data-ttu-id="9d130-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d130-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d130-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9d130-128">Resource Group Name</span></span>

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

### <span data-ttu-id="9d130-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d130-129">CommonParameters</span></span>
<span data-ttu-id="9d130-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d130-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d130-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d130-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d130-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d130-132">INPUTS</span></span>

### <span data-ttu-id="9d130-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9d130-133">System.String</span></span>

## <span data-ttu-id="9d130-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d130-134">OUTPUTS</span></span>

### <span data-ttu-id="9d130-135">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="9d130-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="9d130-136">Note</span><span class="sxs-lookup"><span data-stu-id="9d130-136">NOTES</span></span>

## <span data-ttu-id="9d130-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d130-137">RELATED LINKS</span></span>
