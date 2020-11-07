---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7c766d3a112b880eaaa697e1f09d0d458dee5505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686798"
---
# <span data-ttu-id="7ee6b-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="7ee6b-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="7ee6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ee6b-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee6b-103">Aggiorna la descrizione di un HybridConnection nello spazio dei nomi di inoltro specificato.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ee6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ee6b-104">SYNTAX</span></span>

### <span data-ttu-id="7ee6b-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7ee6b-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ee6b-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="7ee6b-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ee6b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ee6b-107">DESCRIPTION</span></span>
<span data-ttu-id="7ee6b-108">Il cmdlet Set-AzureRmRelayHybridConnection aggiorna la descrizione per HybridConnection nello spazio dei nomi Relay specificato.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="7ee6b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ee6b-109">EXAMPLES</span></span>

### <span data-ttu-id="7ee6b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7ee6b-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid
```

### <span data-ttu-id="7ee6b-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7ee6b-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"
```

<span data-ttu-id="7ee6b-112">Aggiorna l'oggetto HybridConnection specificato con una nuova descrizione nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="7ee6b-113">Questo esempio aggiorna la Proprietà UserMetadata con un nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="7ee6b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ee6b-114">PARAMETERS</span></span>

### <span data-ttu-id="7ee6b-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="7ee6b-115">-UserMetadata</span></span>
<span data-ttu-id="7ee6b-116">Ottiene o imposta UserMetadata è un segnaposto per archiviare i dati di stringa definiti dall'utente per l'endpoint HybridConnection. ad esempio. può essere usato per archiviare dati descrittivi, ad esempio un elenco di team e le relative informazioni di contatto anche le impostazioni di configurazione definite dall'utente possono essere archiviate.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="7ee6b-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7ee6b-117">-Confirm</span></span>
<span data-ttu-id="7ee6b-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ee6b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ee6b-119">-WhatIf</span></span>
<span data-ttu-id="7ee6b-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ee6b-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ee6b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ee6b-122">-InputObject</span></span>
<span data-ttu-id="7ee6b-123">Oggetto HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-123">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee6b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ee6b-124">-Name</span></span>
<span data-ttu-id="7ee6b-125">Nome HybridConnections.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-125">HybridConnections Name.</span></span>

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

### <span data-ttu-id="7ee6b-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7ee6b-126">-Namespace</span></span>
<span data-ttu-id="7ee6b-127">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-127">Namespace Name.</span></span>

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

### <span data-ttu-id="7ee6b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee6b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7ee6b-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="7ee6b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee6b-130">-DefaultProfile</span></span>
<span data-ttu-id="7ee6b-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ee6b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee6b-132">CommonParameters</span></span>
<span data-ttu-id="7ee6b-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ee6b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee6b-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ee6b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee6b-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ee6b-135">INPUTS</span></span>

### <span data-ttu-id="7ee6b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee6b-136">-ResourceGroupName</span></span>
<span data-ttu-id="7ee6b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7ee6b-137">System.String</span></span>

### <span data-ttu-id="7ee6b-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7ee6b-138">-NamespaceName</span></span>
<span data-ttu-id="7ee6b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7ee6b-139">System.String</span></span>

### <span data-ttu-id="7ee6b-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="7ee6b-140">-WcfRelayName</span></span>
<span data-ttu-id="7ee6b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7ee6b-141">System.String</span></span>

### <span data-ttu-id="7ee6b-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ee6b-142">-InputObject</span></span>
<span data-ttu-id="7ee6b-143">Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="7ee6b-143">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="7ee6b-144">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="7ee6b-144">-UserMetadata</span></span>
<span data-ttu-id="7ee6b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7ee6b-145">System.String</span></span>

## <span data-ttu-id="7ee6b-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ee6b-146">OUTPUTS</span></span>

### <span data-ttu-id="7ee6b-147">Esempi-1: InputObject</span><span class="sxs-lookup"><span data-stu-id="7ee6b-147">Examples - 1 : InputObject</span></span>
<span data-ttu-id="7ee6b-148">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:08:11 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: test UserMetadata ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2 nome: TestHybirdConnection2 tipo: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="7ee6b-148">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:08:11 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="7ee6b-149">Esempi-2: Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ee6b-149">Examples - 2 : Properties</span></span>
<span data-ttu-id="7ee6b-150">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:10:25 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: test UserMetadata ID aggiornamento:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1 nome: TestHybirdConnection1 tipo: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="7ee6b-150">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:10:25 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata updated Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="7ee6b-151">Note</span><span class="sxs-lookup"><span data-stu-id="7ee6b-151">NOTES</span></span>

## <span data-ttu-id="7ee6b-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ee6b-152">RELATED LINKS</span></span>

