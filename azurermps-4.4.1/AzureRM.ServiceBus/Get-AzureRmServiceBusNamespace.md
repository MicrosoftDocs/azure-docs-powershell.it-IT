---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685656"
---
# <span data-ttu-id="178aa-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="178aa-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="178aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="178aa-102">SYNOPSIS</span></span>
<span data-ttu-id="178aa-103">Ottiene una descrizione per lo spazio dei nomi Service Bus specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="178aa-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="178aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="178aa-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="178aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="178aa-105">DESCRIPTION</span></span>
<span data-ttu-id="178aa-106">Il cmdlet **Get-AzureRmServiceBusNamespace** ottiene una descrizione per lo spazio dei nomi Service Bus specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="178aa-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="178aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="178aa-107">EXAMPLES</span></span>

### <span data-ttu-id="178aa-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="178aa-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="178aa-109">Restituisce una descrizione dello spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="178aa-109">Returns a description of the specified Service Bus namespace.</span></span>

## <span data-ttu-id="178aa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="178aa-110">PARAMETERS</span></span>

### <span data-ttu-id="178aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178aa-111">-DefaultProfile</span></span>
<span data-ttu-id="178aa-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="178aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178aa-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="178aa-113">-Name</span></span>
<span data-ttu-id="178aa-114">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="178aa-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178aa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="178aa-115">-ResourceGroupName</span></span>
<span data-ttu-id="178aa-116">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="178aa-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="178aa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178aa-117">CommonParameters</span></span>
<span data-ttu-id="178aa-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="178aa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178aa-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178aa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178aa-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="178aa-120">INPUTS</span></span>

### <span data-ttu-id="178aa-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="178aa-121">-ResourceGroup</span></span>
<span data-ttu-id="178aa-122">System. String</span><span class="sxs-lookup"><span data-stu-id="178aa-122">System.String</span></span>

### <span data-ttu-id="178aa-123">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="178aa-123">-NamespaceName</span></span>
 <span data-ttu-id="178aa-124">System. String</span><span class="sxs-lookup"><span data-stu-id="178aa-124">System.String</span></span>

## <span data-ttu-id="178aa-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="178aa-125">OUTPUTS</span></span>

### <span data-ttu-id="178aa-126">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. NamespaceAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="178aa-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="178aa-127">Nome: SB-Example1 ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 location: West US SKU: Name: standard, Capacity: 1, Tier: standard ProvisioningState: succeeded status: Active CreatedAt: 1/20/2017 1:40:01 AM UpdatedAt: 1/20/2017 1:40:24 AM ServiceBusEndpoint: https://SB-Example1.servicebus.windows.net:443/ Enabled: true</span><span class="sxs-lookup"><span data-stu-id="178aa-127">Name               : SB-Example1 Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 Location           : West US Sku                : Name : Standard , Capacity : 1 , Tier : Standard ProvisioningState  : Succeeded Status             : Active CreatedAt          : 1/20/2017 1:40:01 AM UpdatedAt          : 1/20/2017 1:40:24 AM ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/ Enabled            : True</span></span>

## <span data-ttu-id="178aa-128">Note</span><span class="sxs-lookup"><span data-stu-id="178aa-128">NOTES</span></span>
## <span data-ttu-id="178aa-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="178aa-129">RELATED LINKS</span></span>

## <span data-ttu-id="178aa-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="178aa-130">RELATED LINKS</span></span>

