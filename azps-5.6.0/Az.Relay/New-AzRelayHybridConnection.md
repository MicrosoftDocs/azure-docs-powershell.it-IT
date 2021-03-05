---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 6eaffc8f15249366c6e951e78aaf6bb2dc702768
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000526"
---
# <span data-ttu-id="f2591-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="f2591-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="f2591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2591-102">SYNOPSIS</span></span>
<span data-ttu-id="f2591-103">Crea una connessione HybridConnection nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="f2591-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="f2591-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2591-104">SYNTAX</span></span>

### <span data-ttu-id="f2591-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f2591-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2591-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f2591-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2591-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f2591-107">DESCRIPTION</span></span>
<span data-ttu-id="f2591-108">Il cmdlet New-AzRelayHybridConnection crea una connessione HybridConnection nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="f2591-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="f2591-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2591-109">EXAMPLES</span></span>

### <span data-ttu-id="f2591-110">Esempio 1 - InputObject</span><span class="sxs-lookup"><span data-stu-id="f2591-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="f2591-111">Crea una nuova connessione HybirdConnection TestHybirdConnection2 nello spazio dei nomi \` \` Relay specificato \` TestNameSpace-HybirdConnection. \`</span><span class="sxs-lookup"><span data-stu-id="f2591-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="f2591-112">Esempio 2 - Proprietà</span><span class="sxs-lookup"><span data-stu-id="f2591-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="f2591-113">Crea una nuova connessione HybirdConnection TestHybirdConnection1 nello spazio dei nomi \` \` Relay specificato \` TestNameSpace-HybirdConnection. \`</span><span class="sxs-lookup"><span data-stu-id="f2591-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="f2591-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2591-114">PARAMETERS</span></span>

### <span data-ttu-id="f2591-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2591-115">-DefaultProfile</span></span>
<span data-ttu-id="f2591-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2591-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2591-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2591-117">-InputObject</span></span>
<span data-ttu-id="f2591-118">Oggetto HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="f2591-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2591-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f2591-119">-Name</span></span>
<span data-ttu-id="f2591-120">Nome HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="f2591-120">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2591-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f2591-121">-Namespace</span></span>
<span data-ttu-id="f2591-122">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f2591-122">Namespace Name.</span></span>

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

### <span data-ttu-id="f2591-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="f2591-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="f2591-124">true se è necessaria l'autorizzazione client per hybridConnections; in caso contrario false</span><span class="sxs-lookup"><span data-stu-id="f2591-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2591-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2591-125">-ResourceGroupName</span></span>
<span data-ttu-id="f2591-126">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f2591-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="f2591-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="f2591-127">-UserMetadata</span></span>
<span data-ttu-id="f2591-128">Ottiene o imposta usermetadata è un segnaposto per archiviare i dati delle stringhe definiti dall'utente per l'endpoint HybridConnection. può essere usato per archiviare dati descrittivi, ad esempio un elenco di team e le relative informazioni di contatto, è anche possibile archiviare impostazioni di configurazione definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f2591-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="f2591-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2591-129">-Confirm</span></span>
<span data-ttu-id="f2591-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2591-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2591-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2591-131">-WhatIf</span></span>
<span data-ttu-id="f2591-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2591-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2591-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2591-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2591-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2591-134">CommonParameters</span></span>
<span data-ttu-id="f2591-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2591-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2591-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2591-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2591-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="f2591-137">INPUTS</span></span>

### <span data-ttu-id="f2591-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f2591-138">System.String</span></span>

### <span data-ttu-id="f2591-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="f2591-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="f2591-140">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f2591-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f2591-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2591-141">OUTPUTS</span></span>

### <span data-ttu-id="f2591-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="f2591-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="f2591-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="f2591-143">NOTES</span></span>

## <span data-ttu-id="f2591-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2591-144">RELATED LINKS</span></span>
