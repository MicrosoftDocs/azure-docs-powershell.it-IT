---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: 3aa57c1ec70d560a0fee395b27d79372bdf4fd61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509108"
---
# <span data-ttu-id="50bd9-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="50bd9-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="50bd9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="50bd9-103">Crea un WcfRelay nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="50bd9-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50bd9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50bd9-104">SYNTAX</span></span>

### <span data-ttu-id="50bd9-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="50bd9-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50bd9-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="50bd9-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-WcfRelayType <String>] [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>]
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50bd9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50bd9-107">DESCRIPTION</span></span>
<span data-ttu-id="50bd9-108">Il cmdlet New-AzureRmWcfRelay crea un WcfRelay nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="50bd9-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="50bd9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50bd9-109">EXAMPLES</span></span>

### <span data-ttu-id="50bd9-110">Esempio 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="50bd9-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:14:46 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : TestWCFRelay2
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="50bd9-111">Crea un nuovo WcfRelay \` TestWCFRelay2 \` nello spazio dei nomi di inoltro specificato \` TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="50bd9-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="50bd9-112">Esempio 2-proprietà</span><span class="sxs-lookup"><span data-stu-id="50bd9-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:20:08 PM
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

<span data-ttu-id="50bd9-113">Crea un nuovo WcfRelay \` TestWCFRelay \` nello spazio dei nomi di inoltro specificato \` TestNameSpace-relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="50bd9-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="50bd9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50bd9-114">PARAMETERS</span></span>

### <span data-ttu-id="50bd9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50bd9-115">-DefaultProfile</span></span>
<span data-ttu-id="50bd9-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50bd9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50bd9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50bd9-117">-InputObject</span></span>
<span data-ttu-id="50bd9-118">Oggetto WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="50bd9-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="50bd9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="50bd9-119">-Name</span></span>
<span data-ttu-id="50bd9-120">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="50bd9-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="50bd9-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="50bd9-121">-Namespace</span></span>
<span data-ttu-id="50bd9-122">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="50bd9-122">Namespace Name.</span></span>

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

### <span data-ttu-id="50bd9-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="50bd9-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="50bd9-124">true se l'autorizzazione client è necessaria per questo inoltro; in caso contrario, false</span><span class="sxs-lookup"><span data-stu-id="50bd9-124">true if client authorization is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bd9-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="50bd9-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="50bd9-126">true se è necessaria la sicurezza del trasporto per il relè; in caso contrario, false</span><span class="sxs-lookup"><span data-stu-id="50bd9-126">true if transport security is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bd9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50bd9-127">-ResourceGroupName</span></span>
<span data-ttu-id="50bd9-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50bd9-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="50bd9-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="50bd9-129">-UserMetadata</span></span>
<span data-ttu-id="50bd9-130">Ottiene o imposta UserMetadata è un segnaposto per archiviare i dati di stringa definiti dall'utente per l'endpoint HybridConnection. ad esempio. può essere usato per archiviare dati descrittivi, ad esempio un elenco di team e le relative informazioni di contatto anche le impostazioni di configurazione definite dall'utente possono essere archiviate.</span><span class="sxs-lookup"><span data-stu-id="50bd9-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="50bd9-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="50bd9-131">-WcfRelayType</span></span>
<span data-ttu-id="50bd9-132">Tipo WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="50bd9-132">WcfRelay Type.</span></span>
<span data-ttu-id="50bd9-133">I valori possibili includono:' NetTcp ' o ' http '</span><span class="sxs-lookup"><span data-stu-id="50bd9-133">Possible values include: 'NetTcp' or 'Http'</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50bd9-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50bd9-134">-Confirm</span></span>
<span data-ttu-id="50bd9-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50bd9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50bd9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50bd9-136">-WhatIf</span></span>
<span data-ttu-id="50bd9-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50bd9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50bd9-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50bd9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50bd9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50bd9-139">CommonParameters</span></span>
<span data-ttu-id="50bd9-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50bd9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="50bd9-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50bd9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50bd9-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50bd9-142">INPUTS</span></span>

### <span data-ttu-id="50bd9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="50bd9-143">System.String</span></span>
<span data-ttu-id="50bd9-144">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="50bd9-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="50bd9-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50bd9-145">OUTPUTS</span></span>

### <span data-ttu-id="50bd9-146">Microsoft. Azure. Commands. Relay. Models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="50bd9-146">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>


## <span data-ttu-id="50bd9-147">Note</span><span class="sxs-lookup"><span data-stu-id="50bd9-147">NOTES</span></span>

## <span data-ttu-id="50bd9-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50bd9-148">RELATED LINKS</span></span>