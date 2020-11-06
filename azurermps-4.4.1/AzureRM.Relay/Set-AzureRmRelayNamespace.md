---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: c243f31ee549443ad959bde13abc9ff3b68c1560
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513023"
---
# <span data-ttu-id="4a951-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="4a951-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="4a951-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a951-102">SYNOPSIS</span></span>
<span data-ttu-id="4a951-103">Aggiorna la descrizione di uno spazio dei nomi di inoltro esistente.</span><span class="sxs-lookup"><span data-stu-id="4a951-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a951-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a951-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a951-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a951-105">DESCRIPTION</span></span>
<span data-ttu-id="4a951-106">Il cmdlet **set-AzureRmRelayNamespace** aggiorna la descrizione dello spazio dei nomi Relay specificato all'interno del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a951-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="4a951-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a951-107">EXAMPLES</span></span>

### <span data-ttu-id="4a951-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a951-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="4a951-109">Aggiorna lo spazio dei nomi Relay con una nuova descrizione.</span><span class="sxs-lookup"><span data-stu-id="4a951-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="4a951-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a951-110">PARAMETERS</span></span>

### <span data-ttu-id="4a951-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a951-111">-ResourceGroupName</span></span>
<span data-ttu-id="4a951-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a951-112">Resource Group Name.</span></span>

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

### <span data-ttu-id="4a951-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a951-113">-Tag</span></span>
<span data-ttu-id="4a951-114">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4a951-114">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4a951-115">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="4a951-115">For example:</span></span>

<span data-ttu-id="4a951-116">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4a951-116">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4a951-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a951-117">-Confirm</span></span>
<span data-ttu-id="4a951-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a951-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a951-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a951-119">-WhatIf</span></span>
<span data-ttu-id="4a951-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a951-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a951-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a951-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a951-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a951-122">-DefaultProfile</span></span>
<span data-ttu-id="4a951-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a951-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a951-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a951-124">-InputObject</span></span>
<span data-ttu-id="4a951-125">Oggetto dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="4a951-125">Relay Namespace object.</span></span>

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

### <span data-ttu-id="4a951-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a951-126">-Name</span></span>
<span data-ttu-id="4a951-127">Nome dello spazio dei nomi Relay.</span><span class="sxs-lookup"><span data-stu-id="4a951-127">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a951-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a951-128">CommonParameters</span></span>
<span data-ttu-id="4a951-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a951-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a951-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a951-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a951-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a951-131">INPUTS</span></span>

### <span data-ttu-id="4a951-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a951-132">-ResourceGroupName</span></span>
 <span data-ttu-id="4a951-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4a951-133">System.String</span></span>

### <span data-ttu-id="4a951-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4a951-134">-NamespaceName</span></span>
 <span data-ttu-id="4a951-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4a951-135">System.String</span></span>

### <span data-ttu-id="4a951-136">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4a951-136">-Location</span></span>
 <span data-ttu-id="4a951-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4a951-137">System.String</span></span>

### <span data-ttu-id="4a951-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a951-138">-Tag</span></span>
 <span data-ttu-id="4a951-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a951-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a951-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a951-140">OUTPUTS</span></span>

### <span data-ttu-id="4a951-141">Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4a951-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="4a951-142">Note</span><span class="sxs-lookup"><span data-stu-id="4a951-142">NOTES</span></span>

## <span data-ttu-id="4a951-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a951-143">RELATED LINKS</span></span>

