---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 31ced8988574aed139830b5cdd8a26ac74ffcc5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357195"
---
# <span data-ttu-id="7e42c-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="7e42c-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="7e42c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e42c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e42c-103">Ottiene una descrizione per l'oggetto HybridConnection specificato all'interno dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="7e42c-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="7e42c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e42c-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e42c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e42c-105">DESCRIPTION</span></span>
<span data-ttu-id="7e42c-106">Il cmdlet **Get-AzRelayHybridConnection** ottiene una descrizione per la HybridConnection specificata nello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="7e42c-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="7e42c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e42c-107">EXAMPLES</span></span>

### <span data-ttu-id="7e42c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e42c-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="7e42c-109">Restituisce la descrizione di HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="7e42c-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="7e42c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e42c-110">PARAMETERS</span></span>

### <span data-ttu-id="7e42c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e42c-111">-DefaultProfile</span></span>
<span data-ttu-id="7e42c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e42c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e42c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e42c-113">-Name</span></span>
<span data-ttu-id="7e42c-114">Nome HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="7e42c-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e42c-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7e42c-115">-Namespace</span></span>
<span data-ttu-id="7e42c-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7e42c-116">Namespace Name.</span></span>

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

### <span data-ttu-id="7e42c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e42c-117">-ResourceGroupName</span></span>
<span data-ttu-id="7e42c-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7e42c-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="7e42c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e42c-119">CommonParameters</span></span>
<span data-ttu-id="7e42c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e42c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e42c-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e42c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e42c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e42c-122">INPUTS</span></span>

### <span data-ttu-id="7e42c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7e42c-123">System.String</span></span>

## <span data-ttu-id="7e42c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e42c-124">OUTPUTS</span></span>

### <span data-ttu-id="7e42c-125">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="7e42c-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="7e42c-126">Note</span><span class="sxs-lookup"><span data-stu-id="7e42c-126">NOTES</span></span>

## <span data-ttu-id="7e42c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e42c-127">RELATED LINKS</span></span>
