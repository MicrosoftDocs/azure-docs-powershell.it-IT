---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: ccccfe4ba17fe9d5fc9f35f6604f5f7bb9263d14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519942"
---
# <span data-ttu-id="9cf81-101">Remove-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="9cf81-101">Remove-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="9cf81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9cf81-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf81-103">Rimuovere una configurazione di esportazione cotinuous in una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="9cf81-103">Remove a cotinuous export configuration in an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cf81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cf81-104">SYNTAX</span></span>

### <span data-ttu-id="9cf81-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9cf81-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cf81-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cf81-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport
 [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cf81-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cf81-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cf81-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cf81-108">DESCRIPTION</span></span>
<span data-ttu-id="9cf81-109">Rimuovere una configurazione di esportazione cotinuous in una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="9cf81-109">Remove a cotinuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="9cf81-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cf81-110">EXAMPLES</span></span>

### <span data-ttu-id="9cf81-111">Esempio 1 rimuovere una configurazione di esportazione cotinuous in una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="9cf81-111">Example 1 Remove a cotinuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="9cf81-112">Rimuovere le informazioni approfondite dell'applicazione configurazione di esportazione continua con l'ID esportazione "uGOoki0jQsyEs3IdQ83Q4QsNr4 =" per la risorsa denominata "test" nel gruppo risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="9cf81-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="9cf81-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9cf81-113">PARAMETERS</span></span>

### <span data-ttu-id="9cf81-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9cf81-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="9cf81-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="9cf81-115">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf81-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9cf81-116">-Confirm</span></span>
<span data-ttu-id="9cf81-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cf81-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cf81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf81-118">-DefaultProfile</span></span>
<span data-ttu-id="9cf81-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf81-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cf81-120">-ExportId</span><span class="sxs-lookup"><span data-stu-id="9cf81-120">-ExportId</span></span>
<span data-ttu-id="9cf81-121">ID dell'esportazione continuo dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="9cf81-121">Application Insights Continuous Export ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf81-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9cf81-122">-Name</span></span>
<span data-ttu-id="9cf81-123">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="9cf81-123">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf81-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cf81-124">-PassThru</span></span>
<span data-ttu-id="9cf81-125">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="9cf81-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="9cf81-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9cf81-126">This parameter is optional.</span></span> <span data-ttu-id="9cf81-127">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="9cf81-127">Default value is false.</span></span>

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

### <span data-ttu-id="9cf81-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cf81-128">-ResourceGroupName</span></span>
<span data-ttu-id="9cf81-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9cf81-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cf81-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cf81-130">-ResourceId</span></span>
<span data-ttu-id="9cf81-131">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="9cf81-131">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cf81-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf81-132">-WhatIf</span></span>
<span data-ttu-id="9cf81-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cf81-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cf81-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cf81-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cf81-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf81-135">CommonParameters</span></span>
<span data-ttu-id="9cf81-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cf81-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf81-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf81-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf81-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9cf81-138">INPUTS</span></span>

### <span data-ttu-id="9cf81-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9cf81-139">System.String</span></span>

## <span data-ttu-id="9cf81-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cf81-140">OUTPUTS</span></span>

### <span data-ttu-id="9cf81-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="9cf81-141">System.Object</span></span>

## <span data-ttu-id="9cf81-142">Note</span><span class="sxs-lookup"><span data-stu-id="9cf81-142">NOTES</span></span>

## <span data-ttu-id="9cf81-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cf81-143">RELATED LINKS</span></span>

