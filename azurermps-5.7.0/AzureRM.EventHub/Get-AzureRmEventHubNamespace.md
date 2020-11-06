---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
ms.openlocfilehash: d65e19cb86a2ba850311fa937e64432ee8588d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520452"
---
# <span data-ttu-id="989f6-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="989f6-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="989f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="989f6-102">SYNOPSIS</span></span>
<span data-ttu-id="989f6-103">Ottiene i dettagli di uno spazio dei nomi Hub eventi o ottiene un elenco di tutti gli spazi dei nomi Hub eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="989f6-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="989f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="989f6-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="989f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="989f6-105">DESCRIPTION</span></span>
<span data-ttu-id="989f6-106">Il cmdlet Get-AzureRmEventHubNamespace ottiene i dettagli dello spazio dei nomi di un hub di eventi specificato o un elenco di tutti gli spazi dei nomi degli hub di eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="989f6-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="989f6-107">Se viene fornito il nome dello spazio dei nomi, vengono restituiti i dettagli di un singolo spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="989f6-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="989f6-108">Se il nome dello spazio dei nomi non è disponibile, viene restituito un elenco di spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="989f6-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="989f6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="989f6-109">EXAMPLES</span></span>

### <span data-ttu-id="989f6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="989f6-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="989f6-111">Ottiene i dettagli dello spazio dei nomi degli hub di eventi mynamespacename \` \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="989f6-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="989f6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="989f6-112">PARAMETERS</span></span>

### <span data-ttu-id="989f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989f6-113">-DefaultProfile</span></span>
<span data-ttu-id="989f6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="989f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="989f6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="989f6-115">-Name</span></span>
<span data-ttu-id="989f6-116">Nome dello spazio dei nomi EventHub</span><span class="sxs-lookup"><span data-stu-id="989f6-116">EventHub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="989f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="989f6-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="989f6-118">Resource Group Name</span></span>

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

### <span data-ttu-id="989f6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989f6-119">CommonParameters</span></span>
<span data-ttu-id="989f6-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="989f6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="989f6-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="989f6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989f6-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="989f6-122">INPUTS</span></span>

### <span data-ttu-id="989f6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="989f6-123">System.String</span></span>


## <span data-ttu-id="989f6-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="989f6-124">OUTPUTS</span></span>

### <span data-ttu-id="989f6-125">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="989f6-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="989f6-126">Note</span><span class="sxs-lookup"><span data-stu-id="989f6-126">NOTES</span></span>

## <span data-ttu-id="989f6-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="989f6-127">RELATED LINKS</span></span>
