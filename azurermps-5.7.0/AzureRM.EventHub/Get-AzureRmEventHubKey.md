---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: f8a9f074398df5ce9d8464adf3c22a65d14784b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520453"
---
# <span data-ttu-id="02a97-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="02a97-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="02a97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02a97-102">SYNOPSIS</span></span>
<span data-ttu-id="02a97-103">Ottiene i dettagli della chiave primaria della regola di autorizzazione degli hub di eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="02a97-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02a97-104">SYNTAX</span></span>

### <span data-ttu-id="02a97-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="02a97-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02a97-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="02a97-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02a97-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="02a97-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02a97-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02a97-108">DESCRIPTION</span></span>
<span data-ttu-id="02a97-109">Il cmdlet Get-AzureRmEventHubKey restituisce le caratteristiche connectionStrings primarie e secondarie e i dettagli delle chiavi della regola di autorizzazione per lo spazio dei nomi/eventi/alias.</span><span class="sxs-lookup"><span data-stu-id="02a97-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="02a97-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02a97-110">EXAMPLES</span></span>

### <span data-ttu-id="02a97-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02a97-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="02a97-112">Ottiene i dettagli delle caratteristiche connectionStrings primarie e secondarie e delle chiavi per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="02a97-112">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="02a97-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02a97-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="02a97-114">Ottiene i dettagli delle caratteristiche connectionStrings primarie, secondarie, AliasPrimary e AliasSecondary e delle chiavi per la regola di autorizzazione \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="02a97-114">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="02a97-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02a97-115">PARAMETERS</span></span>

### <span data-ttu-id="02a97-116">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="02a97-116">-AliasName</span></span>
<span data-ttu-id="02a97-117">Nome alias</span><span class="sxs-lookup"><span data-stu-id="02a97-117">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a97-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a97-118">-DefaultProfile</span></span>
<span data-ttu-id="02a97-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="02a97-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02a97-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="02a97-120">-EventHub</span></span>
<span data-ttu-id="02a97-121">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="02a97-121">EventHub Name</span></span>

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

### <span data-ttu-id="02a97-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="02a97-122">-Name</span></span>
<span data-ttu-id="02a97-123">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="02a97-123">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="02a97-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="02a97-124">-Namespace</span></span>
<span data-ttu-id="02a97-125">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="02a97-125">Namespace Name</span></span>

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

### <span data-ttu-id="02a97-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a97-126">-ResourceGroupName</span></span>
<span data-ttu-id="02a97-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="02a97-127">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a97-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a97-128">CommonParameters</span></span>
<span data-ttu-id="02a97-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a97-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="02a97-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a97-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a97-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02a97-131">INPUTS</span></span>

### <span data-ttu-id="02a97-132">System. String</span><span class="sxs-lookup"><span data-stu-id="02a97-132">System.String</span></span>


## <span data-ttu-id="02a97-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02a97-133">OUTPUTS</span></span>

### <span data-ttu-id="02a97-134">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="02a97-134">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="02a97-135">Note</span><span class="sxs-lookup"><span data-stu-id="02a97-135">NOTES</span></span>

## <span data-ttu-id="02a97-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02a97-136">RELATED LINKS</span></span>
