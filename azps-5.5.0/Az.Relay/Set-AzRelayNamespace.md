---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192807"
---
# <span data-ttu-id="c7411-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="c7411-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="c7411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7411-102">SYNOPSIS</span></span>
<span data-ttu-id="c7411-103">Aggiorna la descrizione di uno spazio dei nomi Inoltro esistente.</span><span class="sxs-lookup"><span data-stu-id="c7411-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="c7411-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7411-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7411-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c7411-105">DESCRIPTION</span></span>
<span data-ttu-id="c7411-106">Il cmdlet **Set-AzRelayLé** aggiorna la descrizione dello spazio dei nomi Relay specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7411-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="c7411-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7411-107">EXAMPLES</span></span>

### <span data-ttu-id="c7411-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c7411-108">Example 1</span></span>
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

<span data-ttu-id="c7411-109">Aggiorna lo spazio dei nomi Inoltro con una nuova descrizione.</span><span class="sxs-lookup"><span data-stu-id="c7411-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="c7411-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7411-110">PARAMETERS</span></span>

### <span data-ttu-id="c7411-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7411-111">-DefaultProfile</span></span>
<span data-ttu-id="c7411-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7411-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7411-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7411-113">-InputObject</span></span>
<span data-ttu-id="c7411-114">Oggetto Spazio dei nomi di inoltro.</span><span class="sxs-lookup"><span data-stu-id="c7411-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="c7411-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c7411-115">-Name</span></span>
<span data-ttu-id="c7411-116">Relay Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="c7411-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="c7411-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7411-117">-ResourceGroupName</span></span>
<span data-ttu-id="c7411-118">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7411-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7411-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7411-119">-Tag</span></span>
<span data-ttu-id="c7411-120">Hashtables che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c7411-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="c7411-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7411-121">-Confirm</span></span>
<span data-ttu-id="c7411-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7411-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7411-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7411-123">-WhatIf</span></span>
<span data-ttu-id="c7411-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7411-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7411-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7411-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7411-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7411-126">CommonParameters</span></span>
<span data-ttu-id="c7411-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7411-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7411-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7411-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7411-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="c7411-129">INPUTS</span></span>

### <span data-ttu-id="c7411-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c7411-130">System.String</span></span>

### <span data-ttu-id="c7411-131">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c7411-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c7411-132">Microsoft.Azure.Commands.Relay.Models.RelayRbAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="c7411-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="c7411-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7411-133">OUTPUTS</span></span>

### <span data-ttu-id="c7411-134">Microsoft.Azure.Commands.Relay.Models.PSRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="c7411-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="c7411-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="c7411-135">NOTES</span></span>

## <span data-ttu-id="c7411-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7411-136">RELATED LINKS</span></span>
