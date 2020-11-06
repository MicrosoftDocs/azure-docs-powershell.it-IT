---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521672"
---
# <span data-ttu-id="9d5ff-101">Get-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="9d5ff-101">Get-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="9d5ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5ff-103">Ottiene i dettagli delle chiavi connectionStrings primarie e secondarie per la regola di autorizzazione della regola di autorizzazione dello spazio dei nomi Hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="9d5ff-103">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule of the specified Event Hubs namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d5ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d5ff-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## <span data-ttu-id="9d5ff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d5ff-105">DESCRIPTION</span></span>
<span data-ttu-id="9d5ff-106">Il cmdlet Get-AzureRmEventHubNamespaceKey restituisce i dati connectionStrings principali e secondari e i dettagli delle chiavi della regola di autorizzazione specificata nello spazio dei nomi dell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="9d5ff-106">The Get-AzureRmEventHubNamespaceKey cmdlet returns the Primary and Secondary connectionstrings and keys details of the specified authorization rule in the given Event Hubs namespace.</span></span>

## <span data-ttu-id="9d5ff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d5ff-107">EXAMPLES</span></span>

### <span data-ttu-id="9d5ff-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d5ff-108">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="9d5ff-109">Ottiene i dettagli delle caratteristiche connectionStrings primarie e secondarie e delle chiavi per la regola di autorizzazione \` MyAuthRuleName nello \` spazio dei nomi Hub eventi mynamespacename \` \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9d5ff-109">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\` on the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="9d5ff-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d5ff-110">PARAMETERS</span></span>

### <span data-ttu-id="9d5ff-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="9d5ff-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="9d5ff-112">Nome della regola di autorizzazione nello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="9d5ff-112">The name of the authorization rule on the Event Hubs namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d5ff-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9d5ff-113">-NamespaceName</span></span>
<span data-ttu-id="9d5ff-114">Nome dello spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="9d5ff-114">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d5ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d5ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="9d5ff-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9d5ff-116">Resource group name.</span></span>

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

## <span data-ttu-id="9d5ff-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d5ff-117">INPUTS</span></span>

### <span data-ttu-id="9d5ff-118">System. String</span><span class="sxs-lookup"><span data-stu-id="9d5ff-118">System.String</span></span>

## <span data-ttu-id="9d5ff-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d5ff-119">OUTPUTS</span></span>

### <span data-ttu-id="9d5ff-120">Microsoft. Azure. Commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="9d5ff-120">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="9d5ff-121">Note</span><span class="sxs-lookup"><span data-stu-id="9d5ff-121">NOTES</span></span>

## <span data-ttu-id="9d5ff-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d5ff-122">RELATED LINKS</span></span>

