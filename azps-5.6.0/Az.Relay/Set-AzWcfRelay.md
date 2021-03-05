---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: 85c8d65f8a690f9cc977ff069fe6972f5537a114
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000365"
---
# <span data-ttu-id="dd4e7-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="dd4e7-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="dd4e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4e7-103">Aggiorna la descrizione di un elemento WcfRelay nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="dd4e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd4e7-104">SYNTAX</span></span>

### <span data-ttu-id="dd4e7-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd4e7-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd4e7-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="dd4e7-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd4e7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dd4e7-107">DESCRIPTION</span></span>
<span data-ttu-id="dd4e7-108">Il Set-AzWcfRelay cmdlet aggiorna la descrizione per WcfRelay nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="dd4e7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd4e7-109">EXAMPLES</span></span>

### <span data-ttu-id="dd4e7-110">Esempio 1 - InputObject</span><span class="sxs-lookup"><span data-stu-id="dd4e7-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:16:50 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

### <span data-ttu-id="dd4e7-111">Esempio 2 - Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd4e7-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:26:09 PM
ListenerCount               :
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
Name                        : TestWCFRelay
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="dd4e7-112">Aggiorna il valore WcfRelay specificato con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="dd4e7-113">Questo esempio aggiorna la proprietà UserMetadata con un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="dd4e7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd4e7-114">PARAMETERS</span></span>

### <span data-ttu-id="dd4e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4e7-115">-DefaultProfile</span></span>
<span data-ttu-id="dd4e7-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd4e7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd4e7-117">-InputObject</span></span>
<span data-ttu-id="dd4e7-118">Oggetto WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-118">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4e7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dd4e7-119">-Name</span></span>
<span data-ttu-id="dd4e7-120">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="dd4e7-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dd4e7-121">-Namespace</span></span>
<span data-ttu-id="dd4e7-122">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-122">Namespace Name.</span></span>

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

### <span data-ttu-id="dd4e7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd4e7-123">-ResourceGroupName</span></span>
<span data-ttu-id="dd4e7-124">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="dd4e7-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="dd4e7-125">-UserMetadata</span></span>
<span data-ttu-id="dd4e7-126">Ottiene o imposta usermetadata è un segnaposto per archiviare i dati di stringa definiti dall'utente per l'endpoint WcfRelay, ad esempio può essere usato per archiviare dati descrittivi, come l'elenco dei team e le relative informazioni di contatto, e possono essere archiviate anche impostazioni di configurazione definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd4e7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd4e7-127">-Confirm</span></span>
<span data-ttu-id="dd4e7-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd4e7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd4e7-129">-WhatIf</span></span>
<span data-ttu-id="dd4e7-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd4e7-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd4e7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4e7-132">CommonParameters</span></span>
<span data-ttu-id="dd4e7-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd4e7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4e7-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd4e7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4e7-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="dd4e7-135">INPUTS</span></span>

### <span data-ttu-id="dd4e7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="dd4e7-136">System.String</span></span>

### <span data-ttu-id="dd4e7-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="dd4e7-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="dd4e7-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd4e7-138">OUTPUTS</span></span>

### <span data-ttu-id="dd4e7-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="dd4e7-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="dd4e7-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="dd4e7-140">NOTES</span></span>

## <span data-ttu-id="dd4e7-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd4e7-141">RELATED LINKS</span></span>
