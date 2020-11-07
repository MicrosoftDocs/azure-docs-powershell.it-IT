---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: e6dea50e3cb9933d9c6a8aa141f2df43be0b1a18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686196"
---
# <span data-ttu-id="dc8b9-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="dc8b9-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="dc8b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="dc8b9-103">Questa operazione Disabilita il ripristino di emergenza e smette di eseguire la replica delle modifiche dagli spazi dei nomi primari a quelli secondari</span><span class="sxs-lookup"><span data-stu-id="dc8b9-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc8b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc8b9-104">SYNTAX</span></span>

### <span data-ttu-id="dc8b9-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc8b9-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc8b9-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc8b9-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc8b9-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc8b9-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc8b9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc8b9-108">DESCRIPTION</span></span>
<span data-ttu-id="dc8b9-109">Il cmdlet **set-AzureRmEventHubGeoDRConfigurationBreakPair** Disabilita il ripristino di emergenza e smette di replicare le modifiche dagli spazi dei nomi secondari principali a</span><span class="sxs-lookup"><span data-stu-id="dc8b9-109">The **Set-AzureRmEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="dc8b9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc8b9-110">EXAMPLES</span></span>

### <span data-ttu-id="dc8b9-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="dc8b9-111">Example</span></span>
```
PS C:\> Set-AzureRmEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="dc8b9-112">Questa operazione Disabilita il ripristino di emergenza e smette di eseguire la replica delle modifiche dagli spazi dei nomi primari a quelli secondari</span><span class="sxs-lookup"><span data-stu-id="dc8b9-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="dc8b9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc8b9-113">PARAMETERS</span></span>

### <span data-ttu-id="dc8b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc8b9-114">-DefaultProfile</span></span>
<span data-ttu-id="dc8b9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc8b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc8b9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc8b9-116">-InputObject</span></span>
<span data-ttu-id="dc8b9-117">Oggetto di configurazione GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="dc8b9-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc8b9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc8b9-118">-Name</span></span>
<span data-ttu-id="dc8b9-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="dc8b9-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc8b9-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dc8b9-120">-Namespace</span></span>
<span data-ttu-id="dc8b9-121">Nome dello spazio dei nomi-spazio dei nomi principale</span><span class="sxs-lookup"><span data-stu-id="dc8b9-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc8b9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc8b9-122">-PassThru</span></span>
<span data-ttu-id="dc8b9-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="dc8b9-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dc8b9-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="dc8b9-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc8b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc8b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="dc8b9-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="dc8b9-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc8b9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc8b9-127">-ResourceId</span></span>
<span data-ttu-id="dc8b9-128">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc8b9-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc8b9-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dc8b9-129">-Confirm</span></span>
<span data-ttu-id="dc8b9-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc8b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc8b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc8b9-131">-WhatIf</span></span>
<span data-ttu-id="dc8b9-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc8b9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc8b9-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc8b9-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc8b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc8b9-134">CommonParameters</span></span>
<span data-ttu-id="dc8b9-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc8b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dc8b9-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc8b9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc8b9-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc8b9-137">INPUTS</span></span>

### <span data-ttu-id="dc8b9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dc8b9-138">System.String</span></span>
<span data-ttu-id="dc8b9-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="dc8b9-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="dc8b9-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc8b9-140">OUTPUTS</span></span>

### <span data-ttu-id="dc8b9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc8b9-141">System.Boolean</span></span>


## <span data-ttu-id="dc8b9-142">Note</span><span class="sxs-lookup"><span data-stu-id="dc8b9-142">NOTES</span></span>

## <span data-ttu-id="dc8b9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc8b9-143">RELATED LINKS</span></span>