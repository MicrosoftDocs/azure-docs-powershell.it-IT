---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: 16df81633d4265b7b52dd2678bb58c80d4a756e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512364"
---
# <span data-ttu-id="b32d2-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="b32d2-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="b32d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b32d2-102">SYNOPSIS</span></span>
<span data-ttu-id="b32d2-103">Aggiorna la descrizione di un WcfRelay nello spazio dei nomi di inoltro specificato.</span><span class="sxs-lookup"><span data-stu-id="b32d2-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b32d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b32d2-104">SYNTAX</span></span>

### <span data-ttu-id="b32d2-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b32d2-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b32d2-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b32d2-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b32d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b32d2-107">DESCRIPTION</span></span>
<span data-ttu-id="b32d2-108">Il cmdlet Set-AzureRmWcfRelay aggiorna la descrizione per WcfRelay nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="b32d2-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="b32d2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b32d2-109">EXAMPLES</span></span>

### <span data-ttu-id="b32d2-110">Esempio 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="b32d2-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="b32d2-111">Esempio 2-proprietà</span><span class="sxs-lookup"><span data-stu-id="b32d2-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="b32d2-112">Aggiorna l'oggetto WcfRelay specificato con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="b32d2-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="b32d2-113">Questo esempio aggiorna la Proprietà UserMetadata con un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="b32d2-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="b32d2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b32d2-114">PARAMETERS</span></span>

### <span data-ttu-id="b32d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32d2-115">-DefaultProfile</span></span>
<span data-ttu-id="b32d2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b32d2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b32d2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b32d2-117">-InputObject</span></span>
<span data-ttu-id="b32d2-118">Oggetto WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="b32d2-118">WcfRelay object.</span></span>

```yaml
Type: WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32d2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b32d2-119">-Name</span></span>
<span data-ttu-id="b32d2-120">Nome WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="b32d2-120">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32d2-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b32d2-121">-Namespace</span></span>
<span data-ttu-id="b32d2-122">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b32d2-122">Namespace Name.</span></span>

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

### <span data-ttu-id="b32d2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b32d2-123">-ResourceGroupName</span></span>
<span data-ttu-id="b32d2-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b32d2-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="b32d2-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b32d2-125">-UserMetadata</span></span>
<span data-ttu-id="b32d2-126">Ottiene o imposta UserMetadata è un segnaposto per archiviare i dati di stringa definiti dall'utente per l'endpoint HybridConnection. ad esempio. può essere usato per archiviare dati descrittivi, ad esempio un elenco di team e le relative informazioni di contatto anche le impostazioni di configurazione definite dall'utente possono essere archiviate.</span><span class="sxs-lookup"><span data-stu-id="b32d2-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32d2-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b32d2-127">-Confirm</span></span>
<span data-ttu-id="b32d2-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b32d2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b32d2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b32d2-129">-WhatIf</span></span>
<span data-ttu-id="b32d2-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b32d2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b32d2-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b32d2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b32d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32d2-132">CommonParameters</span></span>
<span data-ttu-id="b32d2-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b32d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32d2-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b32d2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32d2-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b32d2-135">INPUTS</span></span>

### <span data-ttu-id="b32d2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b32d2-136">-ResourceGroupName</span></span>
<span data-ttu-id="b32d2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b32d2-137">System.String</span></span>

### <span data-ttu-id="b32d2-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b32d2-138">-NamespaceName</span></span>
<span data-ttu-id="b32d2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b32d2-139">System.String</span></span>

### <span data-ttu-id="b32d2-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="b32d2-140">-WcfRelayName</span></span>
<span data-ttu-id="b32d2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b32d2-141">System.String</span></span>

### <span data-ttu-id="b32d2-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b32d2-142">-InputObject</span></span>
<span data-ttu-id="b32d2-143">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="b32d2-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="b32d2-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="b32d2-144">-WcfRelayType</span></span>
<span data-ttu-id="b32d2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b32d2-145">System.String</span></span>

### <span data-ttu-id="b32d2-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b32d2-146">-UserMetadata</span></span>
<span data-ttu-id="b32d2-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b32d2-147">System.String</span></span>

## <span data-ttu-id="b32d2-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b32d2-148">OUTPUTS</span></span>

### <span data-ttu-id="b32d2-149">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="b32d2-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="b32d2-150">Esempio 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="b32d2-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="b32d2-151">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="b32d2-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="b32d2-152">RelayType: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true dinamico: false UserMetadata: UserMetadata è un segnaposto per archiviare i dati di stringa definiti dall'utente per l'endpoint HybridConnection. ad esempio può essere usato per archiviare i dati di desc riptive, come l'elenco dei team e le relative informazioni di contatto anche le impostazioni di configurazione definite dall'utente possono essere archiviate.</span><span class="sxs-lookup"><span data-stu-id="b32d2-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="b32d2-153">ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-relay1/WcfRelays/TestWCFRelay2 nome: TestWCFRelay2 tipo: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="b32d2-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="b32d2-154">Esempio 2-proprietà</span><span class="sxs-lookup"><span data-stu-id="b32d2-154">Example 2 - Properties</span></span>

### <span data-ttu-id="b32d2-155">Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="b32d2-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="b32d2-156">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:26:09 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true dinamico: false UserMetadata: ID metadati dell'utente:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-relay1/WcfRelays/TestWCFRelay Name: TestWCFRelay Type: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="b32d2-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="b32d2-157">Note</span><span class="sxs-lookup"><span data-stu-id="b32d2-157">NOTES</span></span>

## <span data-ttu-id="b32d2-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b32d2-158">RELATED LINKS</span></span>

