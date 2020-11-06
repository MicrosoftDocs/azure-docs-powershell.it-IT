---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 88d2c8f7b0bcab3faad6368070606b8a36948343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520412"
---
# <span data-ttu-id="fab9b-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="fab9b-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="fab9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fab9b-102">SYNOPSIS</span></span>
<span data-ttu-id="fab9b-103">Restituisce una descrizione per l'oggetto WcfRelay specificato.</span><span class="sxs-lookup"><span data-stu-id="fab9b-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fab9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fab9b-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fab9b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fab9b-105">DESCRIPTION</span></span>
<span data-ttu-id="fab9b-106">Il cmdlet **Get-AzureRmWcfRelay** restituisce una descrizione dell'oggetto WcfRelay specificato.</span><span class="sxs-lookup"><span data-stu-id="fab9b-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="fab9b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fab9b-107">EXAMPLES</span></span>

### <span data-ttu-id="fab9b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fab9b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="fab9b-109">Restituisce la descrizione di WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="fab9b-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="fab9b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fab9b-110">PARAMETERS</span></span>

### <span data-ttu-id="fab9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab9b-111">-DefaultProfile</span></span>
<span data-ttu-id="fab9b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fab9b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fab9b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fab9b-113">-Name</span></span>
<span data-ttu-id="fab9b-114">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="fab9b-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fab9b-115">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fab9b-115">-Namespace</span></span>
<span data-ttu-id="fab9b-116">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fab9b-116">Namespace Name.</span></span>

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

### <span data-ttu-id="fab9b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab9b-117">-ResourceGroupName</span></span>
<span data-ttu-id="fab9b-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fab9b-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="fab9b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab9b-119">CommonParameters</span></span>
<span data-ttu-id="fab9b-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab9b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab9b-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab9b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab9b-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fab9b-122">INPUTS</span></span>

### <span data-ttu-id="fab9b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab9b-123">-ResourceGroupName</span></span>
 <span data-ttu-id="fab9b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fab9b-124">System.String</span></span>
 

### <span data-ttu-id="fab9b-125">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fab9b-125">-Namespace</span></span>
 <span data-ttu-id="fab9b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fab9b-126">System.String</span></span>
 

### <span data-ttu-id="fab9b-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="fab9b-127">-Name</span></span>
 <span data-ttu-id="fab9b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fab9b-128">System.String</span></span> 

## <span data-ttu-id="fab9b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fab9b-129">OUTPUTS</span></span>

### <span data-ttu-id="fab9b-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fab9b-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="fab9b-131">RelayType: NetTcp CreatedAt: 4/12/2017 2:23:08 AM UpdatedAt: 4/12/2017 2:23:08 AM ListenerCount: 0 RequiresClientAuthorization: true RequiresTransportSecurity: true dinamico: false UserMetadata: ID dati utente meta:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 nome: TestWCFRelay1 tipo: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="fab9b-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="fab9b-132">Note</span><span class="sxs-lookup"><span data-stu-id="fab9b-132">NOTES</span></span>

## <span data-ttu-id="fab9b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fab9b-133">RELATED LINKS</span></span>

