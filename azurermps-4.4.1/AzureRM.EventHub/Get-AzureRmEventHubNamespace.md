---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520525"
---
# <span data-ttu-id="e94f2-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e94f2-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="e94f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e94f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e94f2-103">Ottiene i dettagli di uno spazio dei nomi Hub eventi o ottiene un elenco di tutti gli spazi dei nomi Hub eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="e94f2-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e94f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e94f2-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## <span data-ttu-id="e94f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e94f2-105">DESCRIPTION</span></span>
<span data-ttu-id="e94f2-106">Il cmdlet Get-AzureRmEventHubNamespace ottiene i dettagli dello spazio dei nomi di un hub di eventi specificato o un elenco di tutti gli spazi dei nomi degli hub di eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="e94f2-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="e94f2-107">Se viene fornito il nome dello spazio dei nomi, vengono restituiti i dettagli di un singolo spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="e94f2-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="e94f2-108">Se il nome dello spazio dei nomi non è disponibile, viene restituito un elenco di spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e94f2-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="e94f2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e94f2-109">EXAMPLES</span></span>

### <span data-ttu-id="e94f2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e94f2-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="e94f2-111">Ottiene i dettagli dello spazio dei nomi degli hub di eventi mynamespacename \` \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e94f2-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e94f2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e94f2-112">PARAMETERS</span></span>

### <span data-ttu-id="e94f2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e94f2-113">-ResourceGroupName</span></span>
<span data-ttu-id="e94f2-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e94f2-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94f2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e94f2-115">-Name</span></span>
<span data-ttu-id="e94f2-116">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="e94f2-116">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="e94f2-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e94f2-117">INPUTS</span></span>

### <span data-ttu-id="e94f2-118">System. String</span><span class="sxs-lookup"><span data-stu-id="e94f2-118">System.String</span></span>

## <span data-ttu-id="e94f2-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e94f2-119">OUTPUTS</span></span>

### <span data-ttu-id="e94f2-120">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventHub. Models. NamespaceAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e94f2-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e94f2-121">Note</span><span class="sxs-lookup"><span data-stu-id="e94f2-121">NOTES</span></span>

## <span data-ttu-id="e94f2-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e94f2-122">RELATED LINKS</span></span>

