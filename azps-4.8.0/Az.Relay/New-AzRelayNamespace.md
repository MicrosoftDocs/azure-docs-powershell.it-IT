---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192651"
---
# <span data-ttu-id="a6408-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="a6408-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="a6408-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6408-102">SYNOPSIS</span></span>
<span data-ttu-id="a6408-103">Crea un nuovo spazio dei nomi di inoltro.</span><span class="sxs-lookup"><span data-stu-id="a6408-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="a6408-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6408-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6408-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6408-105">DESCRIPTION</span></span>
<span data-ttu-id="a6408-106">Il cmdlet **New-AzRelayNamespace** crea un nuovo spazio dei nomi di inoltro.</span><span class="sxs-lookup"><span data-stu-id="a6408-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="a6408-107">Una volta creato, il manifesto delle risorse dello spazio dei nomi non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="a6408-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="a6408-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6408-108">EXAMPLES</span></span>

### <span data-ttu-id="a6408-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a6408-109">Example 1</span></span>
```
PS C:\> New-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="a6408-110">Crea un nuovo spazio dei nomi di inoltro all'interno del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="a6408-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="a6408-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6408-111">PARAMETERS</span></span>

### <span data-ttu-id="a6408-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6408-112">-DefaultProfile</span></span>
<span data-ttu-id="a6408-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6408-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6408-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a6408-114">-Location</span></span>
<span data-ttu-id="a6408-115">Posizione dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="a6408-115">Relay Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6408-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6408-116">-Name</span></span>
<span data-ttu-id="a6408-117">Nome dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="a6408-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="a6408-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6408-118">-ResourceGroupName</span></span>
<span data-ttu-id="a6408-119">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6408-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="a6408-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6408-120">-Tag</span></span>
<span data-ttu-id="a6408-121">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a6408-121">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6408-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a6408-122">-Confirm</span></span>
<span data-ttu-id="a6408-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6408-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6408-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6408-124">-WhatIf</span></span>
<span data-ttu-id="a6408-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6408-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6408-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6408-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6408-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6408-127">CommonParameters</span></span>
<span data-ttu-id="a6408-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6408-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6408-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6408-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6408-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6408-130">INPUTS</span></span>

### <span data-ttu-id="a6408-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a6408-131">System.String</span></span>

### <span data-ttu-id="a6408-132">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a6408-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a6408-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6408-133">OUTPUTS</span></span>

### <span data-ttu-id="a6408-134">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a6408-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="a6408-135">Note</span><span class="sxs-lookup"><span data-stu-id="a6408-135">NOTES</span></span>

## <span data-ttu-id="a6408-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6408-136">RELATED LINKS</span></span>
