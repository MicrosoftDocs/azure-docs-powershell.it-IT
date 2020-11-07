---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: 04925f904861eea006c6480dbdb48794afc55c56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856470"
---
# <span data-ttu-id="061cb-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="061cb-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="061cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="061cb-102">SYNOPSIS</span></span>
<span data-ttu-id="061cb-103">Aggiorna la descrizione di un WcfRelay nello spazio dei nomi di inoltro specificato.</span><span class="sxs-lookup"><span data-stu-id="061cb-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="061cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="061cb-104">SYNTAX</span></span>

### <span data-ttu-id="061cb-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="061cb-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="061cb-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="061cb-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="061cb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="061cb-107">DESCRIPTION</span></span>
<span data-ttu-id="061cb-108">Il cmdlet Set-AzWcfRelay aggiorna la descrizione per WcfRelay nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="061cb-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="061cb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="061cb-109">EXAMPLES</span></span>

### <span data-ttu-id="061cb-110">Esempio 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="061cb-110">Example 1 - InputObject</span></span>
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

### <span data-ttu-id="061cb-111">Esempio 2-proprietà</span><span class="sxs-lookup"><span data-stu-id="061cb-111">Example 2 - Properties</span></span>
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

<span data-ttu-id="061cb-112">Aggiorna l'oggetto WcfRelay specificato con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="061cb-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="061cb-113">Questo esempio aggiorna la Proprietà UserMetadata con un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="061cb-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="061cb-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="061cb-114">PARAMETERS</span></span>

### <span data-ttu-id="061cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="061cb-115">-DefaultProfile</span></span>
<span data-ttu-id="061cb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="061cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="061cb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="061cb-117">-InputObject</span></span>
<span data-ttu-id="061cb-118">Oggetto WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="061cb-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="061cb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="061cb-119">-Name</span></span>
<span data-ttu-id="061cb-120">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="061cb-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="061cb-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="061cb-121">-Namespace</span></span>
<span data-ttu-id="061cb-122">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="061cb-122">Namespace Name.</span></span>

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

### <span data-ttu-id="061cb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="061cb-123">-ResourceGroupName</span></span>
<span data-ttu-id="061cb-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="061cb-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="061cb-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="061cb-125">-UserMetadata</span></span>
<span data-ttu-id="061cb-126">Ottiene o imposta UserMetadata è un segnaposto per archiviare i dati di stringa definiti dall'utente per l'endpoint WcfRelay. ad esempio. può essere usato per archiviare dati descrittivi, ad esempio un elenco di team e le relative informazioni di contatto anche le impostazioni di configurazione definite dall'utente possono essere archiviate.</span><span class="sxs-lookup"><span data-stu-id="061cb-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="061cb-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="061cb-127">-Confirm</span></span>
<span data-ttu-id="061cb-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="061cb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="061cb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="061cb-129">-WhatIf</span></span>
<span data-ttu-id="061cb-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="061cb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="061cb-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="061cb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="061cb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="061cb-132">CommonParameters</span></span>
<span data-ttu-id="061cb-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="061cb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="061cb-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="061cb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="061cb-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="061cb-135">INPUTS</span></span>

### <span data-ttu-id="061cb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="061cb-136">System.String</span></span>

### <span data-ttu-id="061cb-137">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="061cb-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="061cb-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="061cb-138">OUTPUTS</span></span>

### <span data-ttu-id="061cb-139">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="061cb-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="061cb-140">Note</span><span class="sxs-lookup"><span data-stu-id="061cb-140">NOTES</span></span>

## <span data-ttu-id="061cb-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="061cb-141">RELATED LINKS</span></span>
