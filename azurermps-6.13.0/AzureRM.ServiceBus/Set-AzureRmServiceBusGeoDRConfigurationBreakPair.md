---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: a12f22260ce8ee5412cd17ddfa420a7d23f82008
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514804"
---
# <span data-ttu-id="288f6-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="288f6-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="288f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="288f6-102">SYNOPSIS</span></span>
<span data-ttu-id="288f6-103">Questa operazione Disabilita il ripristino di emergenza e smette di eseguire la replica delle modifiche dagli spazi dei nomi primari a quelli secondari</span><span class="sxs-lookup"><span data-stu-id="288f6-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="288f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="288f6-104">SYNTAX</span></span>

### <span data-ttu-id="288f6-105">GeoDRPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="288f6-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="288f6-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="288f6-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="288f6-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="288f6-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="288f6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="288f6-108">DESCRIPTION</span></span>
<span data-ttu-id="288f6-109">Il cmdlet **set-AzureRmServiceBusGeoDRConfigurationBreakPair** Disabilita il ripristino di emergenza e smette di replicare le modifiche dagli spazi dei nomi secondari principali a</span><span class="sxs-lookup"><span data-stu-id="288f6-109">The **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="288f6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="288f6-110">EXAMPLES</span></span>

### <span data-ttu-id="288f6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="288f6-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="288f6-112">Questa operazione Disabilita il ripristino di emergenza e smette di eseguire la replica delle modifiche dagli spazi dei nomi primari a quelli secondari</span><span class="sxs-lookup"><span data-stu-id="288f6-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="288f6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="288f6-113">PARAMETERS</span></span>

### <span data-ttu-id="288f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288f6-114">-DefaultProfile</span></span>
<span data-ttu-id="288f6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="288f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="288f6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="288f6-116">-InputObject</span></span>
<span data-ttu-id="288f6-117">Oggetto di configurazione di Service Bus GeoDR</span><span class="sxs-lookup"><span data-stu-id="288f6-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="288f6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="288f6-118">-Name</span></span>
<span data-ttu-id="288f6-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="288f6-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="288f6-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="288f6-120">-Namespace</span></span>
<span data-ttu-id="288f6-121">Nome dello spazio dei nomi-spazio dei nomi principale</span><span class="sxs-lookup"><span data-stu-id="288f6-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="288f6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="288f6-122">-PassThru</span></span>
<span data-ttu-id="288f6-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="288f6-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="288f6-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="288f6-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="288f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="288f6-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="288f6-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="288f6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="288f6-127">-ResourceId</span></span>
<span data-ttu-id="288f6-128">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="288f6-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="288f6-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="288f6-129">-Confirm</span></span>
<span data-ttu-id="288f6-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="288f6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="288f6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="288f6-131">-WhatIf</span></span>
<span data-ttu-id="288f6-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="288f6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="288f6-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="288f6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="288f6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288f6-134">CommonParameters</span></span>
<span data-ttu-id="288f6-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="288f6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288f6-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="288f6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288f6-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="288f6-137">INPUTS</span></span>

### <span data-ttu-id="288f6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="288f6-138">System.String</span></span>

### <span data-ttu-id="288f6-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="288f6-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="288f6-140">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="288f6-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="288f6-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="288f6-141">OUTPUTS</span></span>

### <span data-ttu-id="288f6-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="288f6-142">System.Boolean</span></span>

## <span data-ttu-id="288f6-143">Note</span><span class="sxs-lookup"><span data-stu-id="288f6-143">NOTES</span></span>

## <span data-ttu-id="288f6-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="288f6-144">RELATED LINKS</span></span>