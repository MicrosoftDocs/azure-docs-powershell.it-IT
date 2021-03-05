---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: ef4d7ccf2f56d8a6d2a70fa4efb9468365cfcd32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993423"
---
# <span data-ttu-id="fa7e8-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="fa7e8-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="fa7e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa7e8-102">SYNOPSIS</span></span>
<span data-ttu-id="fa7e8-103">Ottiene una descrizione per lo spazio dei nomi del bus di servizio specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="fa7e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa7e8-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa7e8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fa7e8-105">DESCRIPTION</span></span>
<span data-ttu-id="fa7e8-106">Il cmdlet **Get-AzServiceBus Pull ottiene** una descrizione per lo spazio dei nomi del bus di servizio specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="fa7e8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa7e8-107">EXAMPLES</span></span>

### <span data-ttu-id="fa7e8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fa7e8-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="fa7e8-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa7e8-109">PARAMETERS</span></span>

### <span data-ttu-id="fa7e8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa7e8-110">-DefaultProfile</span></span>
<span data-ttu-id="fa7e8-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa7e8-112">-Name</span><span class="sxs-lookup"><span data-stu-id="fa7e8-112">-Name</span></span>
<span data-ttu-id="fa7e8-113">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-113">Namespace Name.</span></span>

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

### <span data-ttu-id="fa7e8-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa7e8-114">-ResourceGroupName</span></span>
<span data-ttu-id="fa7e8-115">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fa7e8-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa7e8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa7e8-116">CommonParameters</span></span>
<span data-ttu-id="fa7e8-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa7e8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa7e8-118">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa7e8-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa7e8-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="fa7e8-119">INPUTS</span></span>

### <span data-ttu-id="fa7e8-120">System.String</span><span class="sxs-lookup"><span data-stu-id="fa7e8-120">System.String</span></span>

## <span data-ttu-id="fa7e8-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa7e8-121">OUTPUTS</span></span>

### <span data-ttu-id="fa7e8-122">Microsoft.Azure.Commands.ServiceBus.Models.PSAttributes</span><span class="sxs-lookup"><span data-stu-id="fa7e8-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="fa7e8-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="fa7e8-123">NOTES</span></span>

## <span data-ttu-id="fa7e8-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa7e8-124">RELATED LINKS</span></span>
