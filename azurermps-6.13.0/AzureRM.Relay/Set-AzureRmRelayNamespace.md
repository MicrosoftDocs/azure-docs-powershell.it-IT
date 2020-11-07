---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 6bb333de426236099bed7402fc4756181415c4ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685754"
---
# <span data-ttu-id="bd064-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="bd064-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="bd064-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd064-102">SYNOPSIS</span></span>
<span data-ttu-id="bd064-103">Aggiorna la descrizione di uno spazio dei nomi di inoltro esistente.</span><span class="sxs-lookup"><span data-stu-id="bd064-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd064-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd064-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd064-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd064-105">DESCRIPTION</span></span>
<span data-ttu-id="bd064-106">Il cmdlet **set-AzureRmRelayNamespace** aggiorna la descrizione dello spazio dei nomi Relay specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bd064-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="bd064-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd064-107">EXAMPLES</span></span>

### <span data-ttu-id="bd064-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bd064-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="bd064-109">Aggiorna lo spazio dei nomi Relay con una nuova descrizione.</span><span class="sxs-lookup"><span data-stu-id="bd064-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="bd064-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd064-110">PARAMETERS</span></span>

### <span data-ttu-id="bd064-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd064-111">-DefaultProfile</span></span>
<span data-ttu-id="bd064-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd064-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd064-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd064-113">-InputObject</span></span>
<span data-ttu-id="bd064-114">Oggetto dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="bd064-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="bd064-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd064-115">-Name</span></span>
<span data-ttu-id="bd064-116">Nome dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="bd064-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="bd064-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd064-117">-ResourceGroupName</span></span>
<span data-ttu-id="bd064-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bd064-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="bd064-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd064-119">-Tag</span></span>
<span data-ttu-id="bd064-120">Hashtable che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="bd064-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="bd064-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bd064-121">-Confirm</span></span>
<span data-ttu-id="bd064-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd064-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd064-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd064-123">-WhatIf</span></span>
<span data-ttu-id="bd064-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd064-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd064-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bd064-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd064-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd064-126">CommonParameters</span></span>
<span data-ttu-id="bd064-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd064-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bd064-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd064-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd064-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd064-129">INPUTS</span></span>

### <span data-ttu-id="bd064-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bd064-130">System.String</span></span>
<span data-ttu-id="bd064-131">System. Collections. Hashtable Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="bd064-131">System.Collections.Hashtable Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>


## <span data-ttu-id="bd064-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd064-132">OUTPUTS</span></span>

### <span data-ttu-id="bd064-133">Microsoft. Azure. Commands. Relay. Models. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="bd064-133">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>


## <span data-ttu-id="bd064-134">Note</span><span class="sxs-lookup"><span data-stu-id="bd064-134">NOTES</span></span>

## <span data-ttu-id="bd064-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd064-135">RELATED LINKS</span></span>
