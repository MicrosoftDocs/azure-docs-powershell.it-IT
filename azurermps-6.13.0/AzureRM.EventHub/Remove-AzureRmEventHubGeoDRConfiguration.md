---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 85f6373cad3c6c42bbefa0aba9aac14d3699b6a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686076"
---
# <span data-ttu-id="bf13f-101">Remove-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf13f-101">Remove-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="bf13f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf13f-102">SYNOPSIS</span></span>
<span data-ttu-id="bf13f-103">Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="bf13f-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf13f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf13f-104">SYNTAX</span></span>

### <span data-ttu-id="bf13f-105">GeoDRParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bf13f-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf13f-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bf13f-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf13f-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf13f-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf13f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf13f-108">DESCRIPTION</span></span>
<span data-ttu-id="bf13f-109">Il cmdlet **Remove-AzureRmEventHubGeoDRConfiguration** Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="bf13f-109">The **Remove-AzureRmEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="bf13f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf13f-110">EXAMPLES</span></span>

### <span data-ttu-id="bf13f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bf13f-111">Example 1</span></span>
```
PS C:\>Remove-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="bf13f-112">Elimina un alias (configurazione del ripristino di emergenza)</span><span class="sxs-lookup"><span data-stu-id="bf13f-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="bf13f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf13f-113">PARAMETERS</span></span>

### <span data-ttu-id="bf13f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf13f-114">-AsJob</span></span>
<span data-ttu-id="bf13f-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bf13f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf13f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf13f-116">-DefaultProfile</span></span>
<span data-ttu-id="bf13f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf13f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf13f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf13f-118">-InputObject</span></span>
<span data-ttu-id="bf13f-119">Oggetto di configurazione GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="bf13f-119">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf13f-120">-Name</span></span>
<span data-ttu-id="bf13f-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="bf13f-121">Alias (GeoDR)</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13f-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bf13f-122">-Namespace</span></span>
<span data-ttu-id="bf13f-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bf13f-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf13f-124">-PassThru</span></span>
<span data-ttu-id="bf13f-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="bf13f-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bf13f-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="bf13f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf13f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf13f-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf13f-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="bf13f-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf13f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf13f-129">-ResourceId</span></span>
<span data-ttu-id="bf13f-130">ID risorsa GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="bf13f-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="bf13f-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bf13f-131">-Confirm</span></span>
<span data-ttu-id="bf13f-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf13f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf13f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf13f-133">-WhatIf</span></span>
<span data-ttu-id="bf13f-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf13f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf13f-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bf13f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf13f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf13f-136">CommonParameters</span></span>
<span data-ttu-id="bf13f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf13f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf13f-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf13f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf13f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf13f-139">INPUTS</span></span>

### <span data-ttu-id="bf13f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bf13f-140">System.String</span></span>

### <span data-ttu-id="bf13f-141">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="bf13f-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="bf13f-142">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf13f-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bf13f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf13f-143">OUTPUTS</span></span>

### <span data-ttu-id="bf13f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf13f-144">System.Boolean</span></span>

## <span data-ttu-id="bf13f-145">Note</span><span class="sxs-lookup"><span data-stu-id="bf13f-145">NOTES</span></span>

## <span data-ttu-id="bf13f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf13f-146">RELATED LINKS</span></span>
