---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325816"
---
# <span data-ttu-id="dc2d3-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="dc2d3-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="dc2d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="dc2d3-103">Aggiorna la descrizione di uno spazio dei nomi di inoltro esistente.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="dc2d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc2d3-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc2d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc2d3-105">DESCRIPTION</span></span>
<span data-ttu-id="dc2d3-106">Il cmdlet **set-AzRelayNamespace** aggiorna la descrizione dello spazio dei nomi Relay specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="dc2d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc2d3-107">EXAMPLES</span></span>

### <span data-ttu-id="dc2d3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dc2d3-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="dc2d3-109">Aggiorna lo spazio dei nomi Relay con una nuova descrizione.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="dc2d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc2d3-110">PARAMETERS</span></span>

### <span data-ttu-id="dc2d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc2d3-111">-DefaultProfile</span></span>
<span data-ttu-id="dc2d3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc2d3-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc2d3-113">-InputObject</span></span>
<span data-ttu-id="dc2d3-114">Oggetto dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-114">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc2d3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc2d3-115">-Name</span></span>
<span data-ttu-id="dc2d3-116">Nome dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="dc2d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc2d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc2d3-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc2d3-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="dc2d3-119">-Tag</span></span>
<span data-ttu-id="dc2d3-120">Hashtable che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="dc2d3-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dc2d3-121">-Confirm</span></span>
<span data-ttu-id="dc2d3-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc2d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc2d3-123">-WhatIf</span></span>
<span data-ttu-id="dc2d3-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc2d3-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc2d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc2d3-126">CommonParameters</span></span>
<span data-ttu-id="dc2d3-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc2d3-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc2d3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc2d3-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc2d3-129">INPUTS</span></span>

### <span data-ttu-id="dc2d3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dc2d3-130">System.String</span></span>

### <span data-ttu-id="dc2d3-131">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dc2d3-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dc2d3-132">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="dc2d3-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="dc2d3-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc2d3-133">OUTPUTS</span></span>

### <span data-ttu-id="dc2d3-134">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="dc2d3-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="dc2d3-135">Note</span><span class="sxs-lookup"><span data-stu-id="dc2d3-135">NOTES</span></span>

## <span data-ttu-id="dc2d3-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc2d3-136">RELATED LINKS</span></span>
