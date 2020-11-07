---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: a7a8734395b08c906b84cc4465528434fcb31eb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687095"
---
# <span data-ttu-id="460fc-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="460fc-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="460fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="460fc-102">SYNOPSIS</span></span>
<span data-ttu-id="460fc-103">Crea un WcfRelay nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="460fc-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="460fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="460fc-104">SYNTAX</span></span>

### <span data-ttu-id="460fc-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="460fc-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="460fc-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="460fc-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="460fc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="460fc-107">DESCRIPTION</span></span>
<span data-ttu-id="460fc-108">Il cmdlet New-AzureRmWcfRelay crea un WcfRelay nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="460fc-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="460fc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="460fc-109">EXAMPLES</span></span>

### <span data-ttu-id="460fc-110">Esempio 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="460fc-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject
```

<span data-ttu-id="460fc-111">Crea un nuovo WcfRelay \` TestWCFRelay2 \` nello spazio dei nomi di inoltro specificato \` TestNameSpace-Relay \` .</span><span class="sxs-lookup"><span data-stu-id="460fc-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="460fc-112">Esempio 2-proprietà</span><span class="sxs-lookup"><span data-stu-id="460fc-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"
```

<span data-ttu-id="460fc-113">Crea un nuovo WcfRelay \` TestWCFRelay \` nello spazio dei nomi di inoltro specificato \` TestNameSpace-relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="460fc-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="460fc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="460fc-114">PARAMETERS</span></span>

### <span data-ttu-id="460fc-115">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="460fc-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="460fc-116">true se l'autorizzazione client è necessaria per questo inoltro; in caso contrario, false</span><span class="sxs-lookup"><span data-stu-id="460fc-116">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="460fc-117">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="460fc-117">-RequiresTransportSecurity</span></span>
<span data-ttu-id="460fc-118">true se è necessaria la sicurezza del trasporto per il relè; in caso contrario, false</span><span class="sxs-lookup"><span data-stu-id="460fc-118">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="460fc-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="460fc-119">-UserMetadata</span></span>
<span data-ttu-id="460fc-120">Ottiene o imposta UserMetadata è un segnaposto per archiviare i dati di stringa definiti dall'utente per l'endpoint HybridConnection. ad esempio. può essere usato per archiviare dati descrittivi, ad esempio un elenco di team e le relative informazioni di contatto anche le impostazioni di configurazione definite dall'utente possono essere archiviate.</span><span class="sxs-lookup"><span data-stu-id="460fc-120">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="460fc-121">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="460fc-121">-WcfRelayType</span></span>
<span data-ttu-id="460fc-122">Tipo WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="460fc-122">WcfRelay Type.</span></span>
<span data-ttu-id="460fc-123">I valori possibili includono:' NetTcp ' o ' http '</span><span class="sxs-lookup"><span data-stu-id="460fc-123">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="460fc-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="460fc-124">-Confirm</span></span>
<span data-ttu-id="460fc-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="460fc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="460fc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="460fc-126">-WhatIf</span></span>
<span data-ttu-id="460fc-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="460fc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="460fc-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="460fc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="460fc-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="460fc-129">-InputObject</span></span>
<span data-ttu-id="460fc-130">Oggetto WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="460fc-130">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="460fc-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="460fc-131">-Name</span></span>
<span data-ttu-id="460fc-132">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="460fc-132">WcfRelay Name.</span></span>

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

### <span data-ttu-id="460fc-133">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="460fc-133">-Namespace</span></span>
<span data-ttu-id="460fc-134">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="460fc-134">Namespace Name.</span></span>

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

### <span data-ttu-id="460fc-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="460fc-135">-ResourceGroupName</span></span>
<span data-ttu-id="460fc-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="460fc-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="460fc-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="460fc-137">-DefaultProfile</span></span>
<span data-ttu-id="460fc-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="460fc-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="460fc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460fc-139">CommonParameters</span></span>
<span data-ttu-id="460fc-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="460fc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460fc-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="460fc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="460fc-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="460fc-142">INPUTS</span></span>

### <span data-ttu-id="460fc-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="460fc-143">-ResourceGroupName</span></span>
<span data-ttu-id="460fc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="460fc-144">System.String</span></span>

### <span data-ttu-id="460fc-145">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="460fc-145">-NamespaceName</span></span>
<span data-ttu-id="460fc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="460fc-146">System.String</span></span>

### <span data-ttu-id="460fc-147">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="460fc-147">-WcfRelayName</span></span>
<span data-ttu-id="460fc-148">System. String</span><span class="sxs-lookup"><span data-stu-id="460fc-148">System.String</span></span>

### <span data-ttu-id="460fc-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="460fc-149">-InputObject</span></span>
<span data-ttu-id="460fc-150">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="460fc-150">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="460fc-151">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="460fc-151">-WcfRelayType</span></span>
<span data-ttu-id="460fc-152">System. String</span><span class="sxs-lookup"><span data-stu-id="460fc-152">System.String</span></span>

### <span data-ttu-id="460fc-153">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="460fc-153">-RequiresClientAuthorization</span></span>
<span data-ttu-id="460fc-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="460fc-154">System.Boolean</span></span>

### <span data-ttu-id="460fc-155">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="460fc-155">-RequiresTransportSecurity</span></span>
<span data-ttu-id="460fc-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="460fc-156">System.Boolean</span></span>

### <span data-ttu-id="460fc-157">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="460fc-157">-UserMetadata</span></span>
<span data-ttu-id="460fc-158">System. String</span><span class="sxs-lookup"><span data-stu-id="460fc-158">System.String</span></span>

## <span data-ttu-id="460fc-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="460fc-159">OUTPUTS</span></span>

### <span data-ttu-id="460fc-160">Esempio 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="460fc-160">Example 1 - InputObject</span></span>

### <span data-ttu-id="460fc-161">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="460fc-161">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="460fc-162">RelayType: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:14:46 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true dinamico: false UserMetadata: TestWCFRelay2 ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-relay1/WcfRelays/TestWCFRelay2 Name: TestWCFRelay2 Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="460fc-162">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:14:46 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : TestWCFRelay2 Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="460fc-163">Esempio 2-proprietà</span><span class="sxs-lookup"><span data-stu-id="460fc-163">Example 2 - Properties</span></span>

### <span data-ttu-id="460fc-164">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="460fc-164">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="460fc-165">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:20:08 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true dinamico: false UserMetadata: ID metadati dell'utente:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-relay1/WcfRelays/TestWCFRelay Name: TestWCFRelay Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="460fc-165">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:20:08 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="460fc-166">Note</span><span class="sxs-lookup"><span data-stu-id="460fc-166">NOTES</span></span>

## <span data-ttu-id="460fc-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="460fc-167">RELATED LINKS</span></span>

