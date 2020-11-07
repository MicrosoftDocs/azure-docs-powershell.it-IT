---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: af4927631b126f068495b3b130dfc560874834cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685661"
---
# <span data-ttu-id="6e4af-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="6e4af-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="6e4af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e4af-102">SYNOPSIS</span></span>
<span data-ttu-id="6e4af-103">Aggiorna la descrizione di un WcfRelay nello spazio dei nomi di inoltro specificato.</span><span class="sxs-lookup"><span data-stu-id="6e4af-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e4af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e4af-104">SYNTAX</span></span>

### <span data-ttu-id="6e4af-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6e4af-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e4af-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="6e4af-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e4af-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e4af-107">DESCRIPTION</span></span>
<span data-ttu-id="6e4af-108">Il cmdlet Set-AzureRmWcfRelay aggiorna la descrizione per WcfRelay nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="6e4af-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="6e4af-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e4af-109">EXAMPLES</span></span>

### <span data-ttu-id="6e4af-110">Esempio 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e4af-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="6e4af-111">Esempio 2-proprietà</span><span class="sxs-lookup"><span data-stu-id="6e4af-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="6e4af-112">Aggiorna l'oggetto WcfRelay specificato con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="6e4af-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="6e4af-113">Questo esempio aggiorna la Proprietà UserMetadata con un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="6e4af-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="6e4af-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e4af-114">PARAMETERS</span></span>

### <span data-ttu-id="6e4af-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="6e4af-115">-UserMetadata</span></span>
<span data-ttu-id="6e4af-116">Ottiene o imposta UserMetadata è un segnaposto per archiviare i dati di stringa definiti dall'utente per l'endpoint HybridConnection. ad esempio. può essere usato per archiviare dati descrittivi, ad esempio un elenco di team e le relative informazioni di contatto anche le impostazioni di configurazione definite dall'utente possono essere archiviate.</span><span class="sxs-lookup"><span data-stu-id="6e4af-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="6e4af-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6e4af-117">-Confirm</span></span>
<span data-ttu-id="6e4af-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e4af-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e4af-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e4af-119">-WhatIf</span></span>
<span data-ttu-id="6e4af-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e4af-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e4af-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e4af-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e4af-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e4af-122">-InputObject</span></span>
<span data-ttu-id="6e4af-123">Oggetto WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6e4af-123">WcfRelay object.</span></span>

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

### <span data-ttu-id="6e4af-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e4af-124">-Name</span></span>
<span data-ttu-id="6e4af-125">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6e4af-125">WcfRelay Name.</span></span>

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

### <span data-ttu-id="6e4af-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6e4af-126">-Namespace</span></span>
<span data-ttu-id="6e4af-127">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6e4af-127">Namespace Name.</span></span>

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

### <span data-ttu-id="6e4af-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e4af-128">-ResourceGroupName</span></span>
<span data-ttu-id="6e4af-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e4af-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="6e4af-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e4af-130">-DefaultProfile</span></span>
<span data-ttu-id="6e4af-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e4af-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e4af-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e4af-132">CommonParameters</span></span>
<span data-ttu-id="6e4af-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e4af-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e4af-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e4af-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e4af-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e4af-135">INPUTS</span></span>

### <span data-ttu-id="6e4af-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e4af-136">-ResourceGroupName</span></span>
<span data-ttu-id="6e4af-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6e4af-137">System.String</span></span>

### <span data-ttu-id="6e4af-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6e4af-138">-NamespaceName</span></span>
<span data-ttu-id="6e4af-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6e4af-139">System.String</span></span>

### <span data-ttu-id="6e4af-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="6e4af-140">-WcfRelayName</span></span>
<span data-ttu-id="6e4af-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6e4af-141">System.String</span></span>

### <span data-ttu-id="6e4af-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e4af-142">-InputObject</span></span>
<span data-ttu-id="6e4af-143">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="6e4af-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="6e4af-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="6e4af-144">-WcfRelayType</span></span>
<span data-ttu-id="6e4af-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6e4af-145">System.String</span></span>

### <span data-ttu-id="6e4af-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="6e4af-146">-UserMetadata</span></span>
<span data-ttu-id="6e4af-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6e4af-147">System.String</span></span>

## <span data-ttu-id="6e4af-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e4af-148">OUTPUTS</span></span>

### <span data-ttu-id="6e4af-149">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="6e4af-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="6e4af-150">Esempio 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e4af-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="6e4af-151">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="6e4af-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="6e4af-152">RelayType: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true dinamico: false UserMetadata: UserMetadata è un segnaposto per archiviare i dati di stringa definiti dall'utente per l'endpoint HybridConnection. ad esempio può essere usato per archiviare i dati di desc riptive, come l'elenco dei team e le relative informazioni di contatto anche le impostazioni di configurazione definite dall'utente possono essere archiviate.</span><span class="sxs-lookup"><span data-stu-id="6e4af-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="6e4af-153">ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-relay1/WcfRelays/TestWCFRelay2 nome: TestWCFRelay2 tipo: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="6e4af-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="6e4af-154">Esempio 2-proprietà</span><span class="sxs-lookup"><span data-stu-id="6e4af-154">Example 2 - Properties</span></span>

### <span data-ttu-id="6e4af-155">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="6e4af-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="6e4af-156">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:26:09 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true dinamico: false UserMetadata: ID metadati dell'utente:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-relay1/WcfRelays/TestWCFRelay Name: TestWCFRelay Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="6e4af-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="6e4af-157">Note</span><span class="sxs-lookup"><span data-stu-id="6e4af-157">NOTES</span></span>

## <span data-ttu-id="6e4af-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e4af-158">RELATED LINKS</span></span>

