---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: 10fc65f492c76a3b240bd2287b080d56bb20836e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000413"
---
# <span data-ttu-id="ee1e5-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="ee1e5-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="ee1e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee1e5-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1e5-103">Aggiorna la descrizione di HybridConnection nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="ee1e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee1e5-104">SYNTAX</span></span>

### <span data-ttu-id="ee1e5-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ee1e5-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee1e5-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="ee1e5-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee1e5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ee1e5-107">DESCRIPTION</span></span>
<span data-ttu-id="ee1e5-108">Il Set-AzRelayHybridConnection cmdlet aggiorna la descrizione per HybridConnection nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="ee1e5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee1e5-109">EXAMPLES</span></span>

### <span data-ttu-id="ee1e5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee1e5-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="ee1e5-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ee1e5-111">Example 2</span></span>
```
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="ee1e5-112">Aggiorna l'oggetto HybridConnection specificato con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="ee1e5-113">Questo esempio aggiorna la proprietà UserMetadata con un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="ee1e5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee1e5-114">PARAMETERS</span></span>

### <span data-ttu-id="ee1e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1e5-115">-DefaultProfile</span></span>
<span data-ttu-id="ee1e5-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee1e5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee1e5-117">-InputObject</span></span>
<span data-ttu-id="ee1e5-118">Oggetto HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1e5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ee1e5-119">-Name</span></span>
<span data-ttu-id="ee1e5-120">Nome HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="ee1e5-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ee1e5-121">-Namespace</span></span>
<span data-ttu-id="ee1e5-122">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-122">Namespace Name.</span></span>

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

### <span data-ttu-id="ee1e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee1e5-124">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee1e5-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="ee1e5-125">-UserMetadata</span></span>
<span data-ttu-id="ee1e5-126">Ottiene o imposta usermetadata è un segnaposto per archiviare i dati delle stringhe definiti dall'utente per l'endpoint HybridConnection. può essere usato per archiviare dati descrittivi, come l'elenco dei team e le relative informazioni di contatto, e possono essere archiviate anche impostazioni di configurazione definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1e5-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee1e5-127">-Confirm</span></span>
<span data-ttu-id="ee1e5-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee1e5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee1e5-129">-WhatIf</span></span>
<span data-ttu-id="ee1e5-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee1e5-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee1e5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1e5-132">CommonParameters</span></span>
<span data-ttu-id="ee1e5-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee1e5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1e5-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee1e5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1e5-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ee1e5-135">INPUTS</span></span>

### <span data-ttu-id="ee1e5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ee1e5-136">System.String</span></span>

### <span data-ttu-id="ee1e5-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="ee1e5-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="ee1e5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee1e5-138">OUTPUTS</span></span>

### <span data-ttu-id="ee1e5-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="ee1e5-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="ee1e5-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="ee1e5-140">NOTES</span></span>

## <span data-ttu-id="ee1e5-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee1e5-141">RELATED LINKS</span></span>
