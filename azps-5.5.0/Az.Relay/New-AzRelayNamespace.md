---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208587"
---
# <span data-ttu-id="4bcc7-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="4bcc7-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="4bcc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bcc7-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcc7-103">Crea un nuovo spazio dei nomi inoltro.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="4bcc7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bcc7-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bcc7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4bcc7-105">DESCRIPTION</span></span>
<span data-ttu-id="4bcc7-106">Il cmdlet **New-AzRelayLé crea** un nuovo spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="4bcc7-107">Dopo la creazione, il manifesto della risorsa dello spazio dei nomi non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="4bcc7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bcc7-108">EXAMPLES</span></span>

### <span data-ttu-id="4bcc7-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4bcc7-109">Example 1</span></span>
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

<span data-ttu-id="4bcc7-110">Crea un nuovo spazio dei nomi Inoltro all'interno del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="4bcc7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bcc7-111">PARAMETERS</span></span>

### <span data-ttu-id="4bcc7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcc7-112">-DefaultProfile</span></span>
<span data-ttu-id="4bcc7-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bcc7-114">-Location</span><span class="sxs-lookup"><span data-stu-id="4bcc7-114">-Location</span></span>
<span data-ttu-id="4bcc7-115">Posizione dello spazio dei nomi di inoltro.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="4bcc7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4bcc7-116">-Name</span></span>
<span data-ttu-id="4bcc7-117">Relay Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="4bcc7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bcc7-118">-ResourceGroupName</span></span>
<span data-ttu-id="4bcc7-119">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="4bcc7-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="4bcc7-120">-Tag</span></span>
<span data-ttu-id="4bcc7-121">Hashtables che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="4bcc7-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bcc7-122">-Confirm</span></span>
<span data-ttu-id="4bcc7-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bcc7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bcc7-124">-WhatIf</span></span>
<span data-ttu-id="4bcc7-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bcc7-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bcc7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcc7-127">CommonParameters</span></span>
<span data-ttu-id="4bcc7-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bcc7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcc7-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bcc7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcc7-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="4bcc7-130">INPUTS</span></span>

### <span data-ttu-id="4bcc7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4bcc7-131">System.String</span></span>

### <span data-ttu-id="4bcc7-132">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4bcc7-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4bcc7-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bcc7-133">OUTPUTS</span></span>

### <span data-ttu-id="4bcc7-134">Microsoft.Azure.Commands.Relay.Models.PSRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="4bcc7-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="4bcc7-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="4bcc7-135">NOTES</span></span>

## <span data-ttu-id="4bcc7-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bcc7-136">RELATED LINKS</span></span>
