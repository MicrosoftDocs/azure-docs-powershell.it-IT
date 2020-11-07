---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 9398c2229b31e432e55e5c4b11e72d3360b52fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686307"
---
# <span data-ttu-id="8bd12-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="8bd12-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="8bd12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8bd12-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd12-103">Crea un HybridConnection nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="8bd12-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bd12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bd12-104">SYNTAX</span></span>

### <span data-ttu-id="8bd12-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8bd12-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bd12-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="8bd12-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bd12-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bd12-107">DESCRIPTION</span></span>
<span data-ttu-id="8bd12-108">Il cmdlet New-AzureRmRelayHybridConnection crea un HybridConnection nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="8bd12-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="8bd12-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bd12-109">EXAMPLES</span></span>

### <span data-ttu-id="8bd12-110">Esempio 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bd12-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

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

<span data-ttu-id="8bd12-111">Crea un nuovo HybirdConnection \` TestHybirdConnection2 \` nello spazio dei nomi di inoltro specificato \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="8bd12-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="8bd12-112">Esempio 2-proprietà</span><span class="sxs-lookup"><span data-stu-id="8bd12-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

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

<span data-ttu-id="8bd12-113">Crea un nuovo HybirdConnection \` TestHybirdConnection1 \` nello spazio dei nomi di inoltro specificato \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="8bd12-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="8bd12-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bd12-114">PARAMETERS</span></span>

### <span data-ttu-id="8bd12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd12-115">-DefaultProfile</span></span>
<span data-ttu-id="8bd12-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd12-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd12-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bd12-117">-InputObject</span></span>
<span data-ttu-id="8bd12-118">Oggetto HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="8bd12-118">HybridConnections object.</span></span>

```yaml
Type: HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd12-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bd12-119">-Name</span></span>
<span data-ttu-id="8bd12-120">Nome HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="8bd12-120">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd12-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8bd12-121">-Namespace</span></span>
<span data-ttu-id="8bd12-122">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8bd12-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd12-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="8bd12-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="8bd12-124">true se è necessaria l'autorizzazione client per questo HybridConnections; in caso contrario, false</span><span class="sxs-lookup"><span data-stu-id="8bd12-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: Boolean
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd12-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bd12-125">-ResourceGroupName</span></span>
<span data-ttu-id="8bd12-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8bd12-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd12-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="8bd12-127">-UserMetadata</span></span>
<span data-ttu-id="8bd12-128">Ottiene o imposta UserMetadata è un segnaposto per archiviare i dati di stringa definiti dall'utente per l'endpoint HybridConnection. ad esempio. può essere usato per archiviare dati descrittivi, ad esempio un elenco di team e le relative informazioni di contatto anche le impostazioni di configurazione definite dall'utente possono essere archiviate.</span><span class="sxs-lookup"><span data-stu-id="8bd12-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd12-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8bd12-129">-Confirm</span></span>
<span data-ttu-id="8bd12-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bd12-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd12-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bd12-131">-WhatIf</span></span>
<span data-ttu-id="8bd12-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bd12-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bd12-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bd12-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd12-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd12-134">CommonParameters</span></span>
<span data-ttu-id="8bd12-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd12-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd12-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bd12-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd12-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8bd12-137">INPUTS</span></span>

### <span data-ttu-id="8bd12-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bd12-138">-ResourceGroupName</span></span>
<span data-ttu-id="8bd12-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8bd12-139">System.String</span></span>

### <span data-ttu-id="8bd12-140">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8bd12-140">-NamespaceName</span></span>
<span data-ttu-id="8bd12-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8bd12-141">System.String</span></span>

### <span data-ttu-id="8bd12-142">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="8bd12-142">-HybridConnectionsName</span></span>
<span data-ttu-id="8bd12-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8bd12-143">System.String</span></span>

### <span data-ttu-id="8bd12-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bd12-144">-InputObject</span></span>
<span data-ttu-id="8bd12-145">Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="8bd12-145">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="8bd12-146">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="8bd12-146">-RequiresClientAuthorization</span></span>
<span data-ttu-id="8bd12-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8bd12-147">System.Boolean</span></span>

### <span data-ttu-id="8bd12-148">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="8bd12-148">-UserMetadata</span></span>
<span data-ttu-id="8bd12-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8bd12-149">System.String</span></span>

## <span data-ttu-id="8bd12-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bd12-150">OUTPUTS</span></span>

### <span data-ttu-id="8bd12-151">Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="8bd12-151">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

## <span data-ttu-id="8bd12-152">Note</span><span class="sxs-lookup"><span data-stu-id="8bd12-152">NOTES</span></span>

## <span data-ttu-id="8bd12-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bd12-153">RELATED LINKS</span></span>

