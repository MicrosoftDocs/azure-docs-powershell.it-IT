---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 0da9ecf9fabaa1cbb21a5fe8f82bb172b84850e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685994"
---
# <span data-ttu-id="fafee-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="fafee-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="fafee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fafee-102">SYNOPSIS</span></span>
<span data-ttu-id="fafee-103">Richiama il failover GEO DR e riconfigura l'alias per puntare allo spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="fafee-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fafee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fafee-104">SYNTAX</span></span>

### <span data-ttu-id="fafee-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fafee-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fafee-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fafee-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fafee-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fafee-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fafee-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fafee-108">DESCRIPTION</span></span>
<span data-ttu-id="fafee-109">Il cmdlet **set-AzureRmEventHubGeoDRConfigurationFailOver** envokes il failover Geo Dr e riconfigura l'alias in punti allo spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="fafee-109">The **Set-AzureRmEventHubGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="fafee-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fafee-110">EXAMPLES</span></span>

### <span data-ttu-id="fafee-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fafee-111">Example 1</span></span>
```
PS C:\>Set-AzureRmEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="fafee-112">Richiama il failover su alias "SampleDRCongifName", riconfigura e punta allo spazio dei nomi secondario "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="fafee-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="fafee-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fafee-113">PARAMETERS</span></span>

### <span data-ttu-id="fafee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fafee-114">-DefaultProfile</span></span>
<span data-ttu-id="fafee-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fafee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fafee-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fafee-116">-InputObject</span></span>
<span data-ttu-id="fafee-117">Oggetto di configurazione GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="fafee-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="fafee-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fafee-118">-Name</span></span>
<span data-ttu-id="fafee-119">Nome configurazione DR</span><span class="sxs-lookup"><span data-stu-id="fafee-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="fafee-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fafee-120">-Namespace</span></span>
<span data-ttu-id="fafee-121">Nome dello spazio dei nomi-spazio dei nomi secondario</span><span class="sxs-lookup"><span data-stu-id="fafee-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="fafee-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fafee-122">-PassThru</span></span>
<span data-ttu-id="fafee-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="fafee-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fafee-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="fafee-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fafee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fafee-125">-ResourceGroupName</span></span>
<span data-ttu-id="fafee-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="fafee-126">Resource Group Name</span></span>

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

### <span data-ttu-id="fafee-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fafee-127">-ResourceId</span></span>
<span data-ttu-id="fafee-128">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="fafee-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="fafee-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fafee-129">-Confirm</span></span>
<span data-ttu-id="fafee-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fafee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fafee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fafee-131">-WhatIf</span></span>
<span data-ttu-id="fafee-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fafee-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fafee-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fafee-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fafee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fafee-134">CommonParameters</span></span>
<span data-ttu-id="fafee-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fafee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fafee-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fafee-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fafee-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fafee-137">INPUTS</span></span>

### <span data-ttu-id="fafee-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fafee-138">System.String</span></span>
<span data-ttu-id="fafee-139">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="fafee-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="fafee-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fafee-140">OUTPUTS</span></span>

### <span data-ttu-id="fafee-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fafee-141">System.Boolean</span></span>


## <span data-ttu-id="fafee-142">Note</span><span class="sxs-lookup"><span data-stu-id="fafee-142">NOTES</span></span>

## <span data-ttu-id="fafee-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fafee-143">RELATED LINKS</span></span>
