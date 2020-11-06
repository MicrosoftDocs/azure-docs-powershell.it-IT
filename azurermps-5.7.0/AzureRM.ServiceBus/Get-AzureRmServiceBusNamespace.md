---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2584630c8c1d0981f354ffc920af4f8ed9ff979f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512283"
---
# <span data-ttu-id="4ee45-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="4ee45-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="4ee45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ee45-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee45-103">Ottiene una descrizione per lo spazio dei nomi Service Bus specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ee45-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ee45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ee45-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ee45-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ee45-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee45-106">Il cmdlet **Get-AzureRmServiceBusNamespace** ottiene una descrizione per lo spazio dei nomi Service Bus specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ee45-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="4ee45-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ee45-107">EXAMPLES</span></span>

### <span data-ttu-id="4ee45-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ee45-108">Example 1</span></span>

```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/

```

## <span data-ttu-id="4ee45-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ee45-109">PARAMETERS</span></span>

### <span data-ttu-id="4ee45-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee45-110">-DefaultProfile</span></span>
<span data-ttu-id="4ee45-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee45-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ee45-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ee45-112">-Name</span></span>
<span data-ttu-id="4ee45-113">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4ee45-113">Namespace Name.</span></span>

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

### <span data-ttu-id="4ee45-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee45-114">-ResourceGroupName</span></span>
<span data-ttu-id="4ee45-115">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4ee45-115">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee45-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee45-116">CommonParameters</span></span>
<span data-ttu-id="4ee45-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee45-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee45-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee45-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee45-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ee45-119">INPUTS</span></span>

### <span data-ttu-id="4ee45-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4ee45-120">-ResourceGroup</span></span>
<span data-ttu-id="4ee45-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4ee45-121">System.String</span></span>

### <span data-ttu-id="4ee45-122">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4ee45-122">-NamespaceName</span></span>
 <span data-ttu-id="4ee45-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4ee45-123">System.String</span></span>

## <span data-ttu-id="4ee45-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ee45-124">OUTPUTS</span></span>

### <span data-ttu-id="4ee45-125">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4ee45-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4ee45-126">Note</span><span class="sxs-lookup"><span data-stu-id="4ee45-126">NOTES</span></span>

## <span data-ttu-id="4ee45-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ee45-127">RELATED LINKS</span></span>

