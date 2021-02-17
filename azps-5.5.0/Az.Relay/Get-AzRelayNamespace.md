---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: ddbc0631b6ba6a3cb55d6e91ab951d44d644e85d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206082"
---
# <span data-ttu-id="df581-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="df581-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="df581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df581-102">SYNOPSIS</span></span>
<span data-ttu-id="df581-103">Ottiene una descrizione per lo spazio dei nomi Inoltro specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="df581-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="df581-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df581-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df581-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="df581-105">DESCRIPTION</span></span>
<span data-ttu-id="df581-106">Il cmdlet **Get-AzRelayLé ottiene** una descrizione per lo spazio dei nomi Relay specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="df581-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="df581-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df581-107">EXAMPLES</span></span>

### <span data-ttu-id="df581-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="df581-108">Example 1</span></span>
```
PS C:\> Get-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="df581-109">Restituisce una descrizione dello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="df581-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="df581-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df581-110">PARAMETERS</span></span>

### <span data-ttu-id="df581-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df581-111">-DefaultProfile</span></span>
<span data-ttu-id="df581-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df581-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df581-113">-Name</span><span class="sxs-lookup"><span data-stu-id="df581-113">-Name</span></span>
<span data-ttu-id="df581-114">Relay Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="df581-114">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df581-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df581-115">-ResourceGroupName</span></span>
<span data-ttu-id="df581-116">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="df581-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="df581-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df581-117">CommonParameters</span></span>
<span data-ttu-id="df581-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df581-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df581-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df581-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df581-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="df581-120">INPUTS</span></span>

### <span data-ttu-id="df581-121">System.String</span><span class="sxs-lookup"><span data-stu-id="df581-121">System.String</span></span>

## <span data-ttu-id="df581-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df581-122">OUTPUTS</span></span>

### <span data-ttu-id="df581-123">Microsoft.Azure.Commands.Relay.Models.PSRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="df581-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="df581-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="df581-124">NOTES</span></span>

## <span data-ttu-id="df581-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df581-125">RELATED LINKS</span></span>
