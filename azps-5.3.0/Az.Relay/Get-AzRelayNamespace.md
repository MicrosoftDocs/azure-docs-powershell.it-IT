---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: ddbc0631b6ba6a3cb55d6e91ab951d44d644e85d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474341"
---
# <span data-ttu-id="97d26-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="97d26-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="97d26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97d26-102">SYNOPSIS</span></span>
<span data-ttu-id="97d26-103">Ottiene una descrizione per lo spazio dei nomi Relay specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="97d26-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="97d26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97d26-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97d26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97d26-105">DESCRIPTION</span></span>
<span data-ttu-id="97d26-106">Il cmdlet **Get-AzRelayNamespace** ottiene una descrizione per lo spazio dei nomi Relay specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="97d26-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="97d26-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97d26-107">EXAMPLES</span></span>

### <span data-ttu-id="97d26-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97d26-108">Example 1</span></span>
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

<span data-ttu-id="97d26-109">Restituisce una descrizione dello spazio dei nomi di inoltro specificato.</span><span class="sxs-lookup"><span data-stu-id="97d26-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="97d26-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97d26-110">PARAMETERS</span></span>

### <span data-ttu-id="97d26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97d26-111">-DefaultProfile</span></span>
<span data-ttu-id="97d26-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97d26-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97d26-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="97d26-113">-Name</span></span>
<span data-ttu-id="97d26-114">Nome dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="97d26-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="97d26-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97d26-115">-ResourceGroupName</span></span>
<span data-ttu-id="97d26-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="97d26-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="97d26-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97d26-117">CommonParameters</span></span>
<span data-ttu-id="97d26-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97d26-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97d26-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97d26-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97d26-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97d26-120">INPUTS</span></span>

### <span data-ttu-id="97d26-121">System. String</span><span class="sxs-lookup"><span data-stu-id="97d26-121">System.String</span></span>

## <span data-ttu-id="97d26-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97d26-122">OUTPUTS</span></span>

### <span data-ttu-id="97d26-123">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="97d26-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="97d26-124">Note</span><span class="sxs-lookup"><span data-stu-id="97d26-124">NOTES</span></span>

## <span data-ttu-id="97d26-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97d26-125">RELATED LINKS</span></span>
