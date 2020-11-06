---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 81463fc5202c9b5990e5d73d81c7bc2cbeadcca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516088"
---
# <span data-ttu-id="41443-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="41443-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="41443-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41443-102">SYNOPSIS</span></span>
<span data-ttu-id="41443-103">Restituisce una descrizione per l'oggetto WcfRelay specificato.</span><span class="sxs-lookup"><span data-stu-id="41443-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41443-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41443-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41443-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41443-105">DESCRIPTION</span></span>
<span data-ttu-id="41443-106">Il cmdlet **Get-AzureRmWcfRelay** restituisce una descrizione dell'oggetto WcfRelay specificato.</span><span class="sxs-lookup"><span data-stu-id="41443-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="41443-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41443-107">EXAMPLES</span></span>

### <span data-ttu-id="41443-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41443-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="41443-109">Restituisce la descrizione di WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="41443-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="41443-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41443-110">PARAMETERS</span></span>

### <span data-ttu-id="41443-111">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="41443-111">-Namespace</span></span>
<span data-ttu-id="41443-112">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="41443-112">Namespace Name.</span></span>

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

### <span data-ttu-id="41443-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41443-113">-ResourceGroupName</span></span>
<span data-ttu-id="41443-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41443-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="41443-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="41443-115">-Name</span></span>
<span data-ttu-id="41443-116">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="41443-116">WcfRelay Name.</span></span>

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

### <span data-ttu-id="41443-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41443-117">-DefaultProfile</span></span>
<span data-ttu-id="41443-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41443-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41443-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41443-119">CommonParameters</span></span>
<span data-ttu-id="41443-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41443-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41443-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41443-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41443-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41443-122">INPUTS</span></span>

### <span data-ttu-id="41443-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41443-123">-ResourceGroupName</span></span>
 <span data-ttu-id="41443-124">System. String</span><span class="sxs-lookup"><span data-stu-id="41443-124">System.String</span></span>
 

### <span data-ttu-id="41443-125">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="41443-125">-Namespace</span></span>
 <span data-ttu-id="41443-126">System. String</span><span class="sxs-lookup"><span data-stu-id="41443-126">System.String</span></span>
 

### <span data-ttu-id="41443-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="41443-127">-Name</span></span>
 <span data-ttu-id="41443-128">System. String</span><span class="sxs-lookup"><span data-stu-id="41443-128">System.String</span></span> 

## <span data-ttu-id="41443-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41443-129">OUTPUTS</span></span>

### <span data-ttu-id="41443-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="41443-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="41443-131">RelayType: NetTcp CreatedAt: 4/12/2017 2:23:08 AM UpdatedAt: 4/12/2017 2:23:08 AM ListenerCount: 0 RequiresClientAuthorization: true RequiresTransportSecurity: true dinamico: false UserMetadata: ID dati utente meta:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 nome: TestWCFRelay1 tipo: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="41443-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="41443-132">Note</span><span class="sxs-lookup"><span data-stu-id="41443-132">NOTES</span></span>

## <span data-ttu-id="41443-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41443-133">RELATED LINKS</span></span>

