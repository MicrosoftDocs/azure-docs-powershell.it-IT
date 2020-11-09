---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: 260cb8b605415137e9a9e667634ff02b8d4b3de7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310032"
---
# <span data-ttu-id="89285-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="89285-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="89285-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89285-102">SYNOPSIS</span></span>
<span data-ttu-id="89285-103">Restituisce una descrizione per l'oggetto WcfRelay specificato.</span><span class="sxs-lookup"><span data-stu-id="89285-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="89285-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89285-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89285-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89285-105">DESCRIPTION</span></span>
<span data-ttu-id="89285-106">Il cmdlet **Get-AzWcfRelay** restituisce una descrizione dell'oggetto WcfRelay specificato.</span><span class="sxs-lookup"><span data-stu-id="89285-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="89285-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89285-107">EXAMPLES</span></span>

### <span data-ttu-id="89285-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="89285-108">Example 1</span></span>
```
PS C:\> Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

RelayType                   : NetTcp
CreatedAt                   : 4/12/2017 2:23:08 AM
UpdatedAt                   : 4/12/2017 2:23:08 AM
ListenerCount               : 0
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W
                              cfRelays/TestWCFRelay1
Name                        : TestWCFRelay1
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="89285-109">Restituisce la descrizione di WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="89285-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="89285-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89285-110">PARAMETERS</span></span>

### <span data-ttu-id="89285-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89285-111">-DefaultProfile</span></span>
<span data-ttu-id="89285-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89285-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89285-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="89285-113">-Name</span></span>
<span data-ttu-id="89285-114">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="89285-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89285-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89285-115">-Namespace</span></span>
<span data-ttu-id="89285-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="89285-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89285-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89285-117">-ResourceGroupName</span></span>
<span data-ttu-id="89285-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89285-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89285-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89285-119">CommonParameters</span></span>
<span data-ttu-id="89285-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89285-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89285-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89285-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89285-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89285-122">INPUTS</span></span>

### <span data-ttu-id="89285-123">System. String</span><span class="sxs-lookup"><span data-stu-id="89285-123">System.String</span></span>

## <span data-ttu-id="89285-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89285-124">OUTPUTS</span></span>

### <span data-ttu-id="89285-125">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="89285-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="89285-126">Note</span><span class="sxs-lookup"><span data-stu-id="89285-126">NOTES</span></span>

## <span data-ttu-id="89285-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89285-127">RELATED LINKS</span></span>
