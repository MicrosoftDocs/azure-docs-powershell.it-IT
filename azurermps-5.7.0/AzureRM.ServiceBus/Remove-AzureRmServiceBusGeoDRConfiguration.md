---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusgeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusGeoDRConfiguration.md
ms.openlocfilehash: 9c5fe091e5e218c4e70ef1486f1211bc0be7894b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517968"
---
# <span data-ttu-id="b1658-101">Remove-AzureRmServiceBusGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1658-101">Remove-AzureRmServiceBusGeoDRConfiguration</span></span>

## <span data-ttu-id="b1658-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1658-102">SYNOPSIS</span></span>
<span data-ttu-id="b1658-103">Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="b1658-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1658-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1658-104">SYNTAX</span></span>

### <span data-ttu-id="b1658-105">GeoDRBreakPairFailOverPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1658-105">GeoDRBreakPairFailOverPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1658-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b1658-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1658-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1658-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1658-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1658-108">DESCRIPTION</span></span>
<span data-ttu-id="b1658-109">Il cmdlet **Remove-AzureRmServiceBusGeoDRConfiguration** Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="b1658-109">The **Remove-AzureRmServiceBusGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="b1658-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1658-110">EXAMPLES</span></span>

### <span data-ttu-id="b1658-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1658-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="b1658-112">Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="b1658-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="b1658-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1658-113">PARAMETERS</span></span>

### <span data-ttu-id="b1658-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1658-114">-AsJob</span></span>
<span data-ttu-id="b1658-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b1658-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1658-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1658-116">-DefaultProfile</span></span>
<span data-ttu-id="b1658-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1658-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1658-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1658-118">-InputObject</span></span>
<span data-ttu-id="b1658-119">Oggetto di configurazione di Service Bus GeoDR</span><span class="sxs-lookup"><span data-stu-id="b1658-119">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1658-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1658-120">-Name</span></span>
<span data-ttu-id="b1658-121">Nome alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="b1658-121">Alias (GeoDR) Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1658-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1658-122">-Namespace</span></span>
<span data-ttu-id="b1658-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1658-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1658-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1658-124">-PassThru</span></span>
<span data-ttu-id="b1658-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b1658-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b1658-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b1658-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b1658-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1658-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1658-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b1658-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRBreakPairFailOverPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1658-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1658-129">-ResourceId</span></span>
<span data-ttu-id="b1658-130">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1658-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="b1658-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1658-131">-Confirm</span></span>
<span data-ttu-id="b1658-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1658-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1658-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1658-133">-WhatIf</span></span>
<span data-ttu-id="b1658-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1658-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1658-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1658-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1658-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1658-136">CommonParameters</span></span>
<span data-ttu-id="b1658-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1658-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b1658-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1658-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1658-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1658-139">INPUTS</span></span>

### <span data-ttu-id="b1658-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b1658-140">System.String</span></span>
<span data-ttu-id="b1658-141">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b1658-141">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>


## <span data-ttu-id="b1658-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1658-142">OUTPUTS</span></span>

### <span data-ttu-id="b1658-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1658-143">System.Boolean</span></span>


## <span data-ttu-id="b1658-144">Note</span><span class="sxs-lookup"><span data-stu-id="b1658-144">NOTES</span></span>

## <span data-ttu-id="b1658-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1658-145">RELATED LINKS</span></span>
