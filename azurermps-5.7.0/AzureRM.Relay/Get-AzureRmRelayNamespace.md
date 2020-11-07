---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: fe0991296ad5f2dc8be89c92117e74c4231b495c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687473"
---
# <span data-ttu-id="0c3bd-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="0c3bd-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="0c3bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c3bd-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3bd-103">Ottiene una descrizione per lo spazio dei nomi Relay specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c3bd-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c3bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c3bd-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c3bd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c3bd-105">DESCRIPTION</span></span>
<span data-ttu-id="0c3bd-106">Il cmdlet **Get-AzureRmRelayNamespace** ottiene una descrizione per lo spazio dei nomi Relay specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c3bd-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="0c3bd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c3bd-107">EXAMPLES</span></span>

### <span data-ttu-id="0c3bd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c3bd-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="0c3bd-109">Restituisce una descrizione dello spazio dei nomi di inoltro specificato.</span><span class="sxs-lookup"><span data-stu-id="0c3bd-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="0c3bd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c3bd-110">PARAMETERS</span></span>

### <span data-ttu-id="0c3bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3bd-111">-DefaultProfile</span></span>
<span data-ttu-id="0c3bd-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c3bd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c3bd-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c3bd-113">-Name</span></span>
<span data-ttu-id="0c3bd-114">Nome dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="0c3bd-114">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3bd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3bd-115">-ResourceGroupName</span></span>
<span data-ttu-id="0c3bd-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0c3bd-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="0c3bd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3bd-117">CommonParameters</span></span>
<span data-ttu-id="0c3bd-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3bd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3bd-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3bd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3bd-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c3bd-120">INPUTS</span></span>

### <span data-ttu-id="0c3bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c3bd-122">System. String</span><span class="sxs-lookup"><span data-stu-id="0c3bd-122">System.String</span></span>

### <span data-ttu-id="0c3bd-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c3bd-123">-Name</span></span>
 <span data-ttu-id="0c3bd-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0c3bd-124">System.String</span></span>

## <span data-ttu-id="0c3bd-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c3bd-125">OUTPUTS</span></span>

### <span data-ttu-id="0c3bd-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0c3bd-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0c3bd-127">ProvisioningState: succeeded CreatedAt: 4/12/2017 12:38:47 AM UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ metricID: 854d368f-1828-428F-8F3C-f2affa9b2f7d: TestNamespace-relay1 location: West US Tags: {[tag1, Tag1Value]} ID:/subscriptions/854d368f-1828-428F-8F3C-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-relay1 Name: TestNameSpace-Relay1 Type: Microsoft. Relay/Namespaces</span><span class="sxs-lookup"><span data-stu-id="0c3bd-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="0c3bd-128">Note</span><span class="sxs-lookup"><span data-stu-id="0c3bd-128">NOTES</span></span>

## <span data-ttu-id="0c3bd-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c3bd-129">RELATED LINKS</span></span>

