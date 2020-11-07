---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 08a20958975d78a945e3e73729d5841f6dda6811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519379"
---
# <span data-ttu-id="f831d-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="f831d-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="f831d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f831d-102">SYNOPSIS</span></span>
<span data-ttu-id="f831d-103">Ottiene una descrizione per l'oggetto HybridConnection specificato all'interno dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="f831d-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f831d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f831d-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f831d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f831d-105">DESCRIPTION</span></span>
<span data-ttu-id="f831d-106">Il cmdlet **Get-AzureRmRelayHybridConnection** ottiene una descrizione per la HybridConnection specificata nello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="f831d-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="f831d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f831d-107">EXAMPLES</span></span>

### <span data-ttu-id="f831d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f831d-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="f831d-109">Restituisce la descrizione di HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="f831d-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="f831d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f831d-110">PARAMETERS</span></span>

### <span data-ttu-id="f831d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f831d-111">-DefaultProfile</span></span>
<span data-ttu-id="f831d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f831d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f831d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f831d-113">-Name</span></span>
<span data-ttu-id="f831d-114">Nome HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="f831d-114">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f831d-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f831d-115">-Namespace</span></span>
<span data-ttu-id="f831d-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f831d-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f831d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f831d-117">-ResourceGroupName</span></span>
<span data-ttu-id="f831d-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f831d-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f831d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f831d-119">CommonParameters</span></span>
<span data-ttu-id="f831d-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f831d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f831d-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f831d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f831d-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f831d-122">INPUTS</span></span>

### <span data-ttu-id="f831d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f831d-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="f831d-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f831d-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="f831d-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f831d-125">-Name</span></span>
    System.String

## <span data-ttu-id="f831d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f831d-126">OUTPUTS</span></span>

### <span data-ttu-id="f831d-127">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f831d-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f831d-128">CreatedAt: 4/12/2017 3:17:02 AM UpdatedAt: 4/12/2017 3:17:02 AM ListenerCount: 0 RequiresClientAuthorization: true UserMetadata: User Meta Data ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection nome: TestHybridConnection tipo: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="f831d-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="f831d-129">Note</span><span class="sxs-lookup"><span data-stu-id="f831d-129">NOTES</span></span>

## <span data-ttu-id="f831d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f831d-130">RELATED LINKS</span></span>
