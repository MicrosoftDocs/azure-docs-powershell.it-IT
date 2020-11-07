---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: c39a85fe148461d5daa680a62b5cfd09b4a3e4e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678804"
---
# <span data-ttu-id="ee4b2-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ee4b2-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="ee4b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee4b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4b2-103">Ottiene i dettagli di uno spazio dei nomi Hub eventi o ottiene un elenco di tutti gli spazi dei nomi Hub eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="ee4b2-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="ee4b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee4b2-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee4b2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee4b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ee4b2-106">Il cmdlet Get-AzEventHubNamespace ottiene i dettagli dello spazio dei nomi di un hub di eventi specificato o un elenco di tutti gli spazi dei nomi degli hub di eventi nell'abbonamento Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="ee4b2-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="ee4b2-107">Se viene fornito il nome dello spazio dei nomi, vengono restituiti i dettagli di un singolo spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="ee4b2-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="ee4b2-108">Se il nome dello spazio dei nomi non è disponibile, viene restituito un elenco di spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ee4b2-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="ee4b2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee4b2-109">EXAMPLES</span></span>

### <span data-ttu-id="ee4b2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee4b2-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="ee4b2-111">Ottiene i dettagli dello spazio dei nomi MyNamespace \` \` nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ee4b2-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ee4b2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee4b2-112">PARAMETERS</span></span>

### <span data-ttu-id="ee4b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee4b2-113">-DefaultProfile</span></span>
<span data-ttu-id="ee4b2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee4b2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee4b2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee4b2-115">-Name</span></span>
<span data-ttu-id="ee4b2-116">Nome dello spazio dei nomi EventHub</span><span class="sxs-lookup"><span data-stu-id="ee4b2-116">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee4b2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee4b2-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee4b2-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ee4b2-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee4b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4b2-119">CommonParameters</span></span>
<span data-ttu-id="ee4b2-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee4b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4b2-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee4b2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4b2-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee4b2-122">INPUTS</span></span>

### <span data-ttu-id="ee4b2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ee4b2-123">System.String</span></span>

## <span data-ttu-id="ee4b2-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee4b2-124">OUTPUTS</span></span>

### <span data-ttu-id="ee4b2-125">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ee4b2-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ee4b2-126">Note</span><span class="sxs-lookup"><span data-stu-id="ee4b2-126">NOTES</span></span>

## <span data-ttu-id="ee4b2-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee4b2-127">RELATED LINKS</span></span>