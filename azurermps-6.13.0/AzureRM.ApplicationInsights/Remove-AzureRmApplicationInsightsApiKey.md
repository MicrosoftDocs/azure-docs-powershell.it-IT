---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: f850877da71e68f14ec720acb7428e192882efd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507715"
---
# <span data-ttu-id="903ea-101">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="903ea-101">Remove-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="903ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="903ea-102">SYNOPSIS</span></span>
<span data-ttu-id="903ea-103">Rimuovere una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="903ea-103">Remove an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="903ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="903ea-104">SYNTAX</span></span>

### <span data-ttu-id="903ea-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="903ea-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="903ea-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="903ea-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="903ea-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="903ea-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="903ea-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="903ea-108">DESCRIPTION</span></span>
<span data-ttu-id="903ea-109">Rimuovere una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="903ea-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="903ea-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="903ea-110">EXAMPLES</span></span>

### <span data-ttu-id="903ea-111">Esempio 1 rimuovere una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="903ea-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="903ea-112">Rimuovere le informazioni chiave API specifiche dell'applicazione che ID è "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="903ea-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="903ea-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="903ea-113">PARAMETERS</span></span>

### <span data-ttu-id="903ea-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="903ea-114">-ApiKeyId</span></span>
<span data-ttu-id="903ea-115">ID chiave API dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="903ea-115">Application Insights API Key ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903ea-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="903ea-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="903ea-117">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="903ea-117">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="903ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903ea-118">-DefaultProfile</span></span>
<span data-ttu-id="903ea-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="903ea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="903ea-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="903ea-120">-Name</span></span>
<span data-ttu-id="903ea-121">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="903ea-121">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903ea-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="903ea-122">-PassThru</span></span>
<span data-ttu-id="903ea-123">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="903ea-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="903ea-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="903ea-124">This parameter is optional.</span></span> <span data-ttu-id="903ea-125">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="903ea-125">Default value is false.</span></span>

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

### <span data-ttu-id="903ea-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="903ea-126">-ResourceGroupName</span></span>
<span data-ttu-id="903ea-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="903ea-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903ea-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="903ea-128">-ResourceId</span></span>
<span data-ttu-id="903ea-129">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="903ea-129">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="903ea-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="903ea-130">-Confirm</span></span>
<span data-ttu-id="903ea-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="903ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="903ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="903ea-132">-WhatIf</span></span>
<span data-ttu-id="903ea-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="903ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="903ea-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="903ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="903ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903ea-135">CommonParameters</span></span>
<span data-ttu-id="903ea-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="903ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903ea-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="903ea-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903ea-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="903ea-138">INPUTS</span></span>

### <span data-ttu-id="903ea-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="903ea-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="903ea-140">Parametri: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="903ea-140">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="903ea-141">System. String</span><span class="sxs-lookup"><span data-stu-id="903ea-141">System.String</span></span>

## <span data-ttu-id="903ea-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="903ea-142">OUTPUTS</span></span>

### <span data-ttu-id="903ea-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="903ea-143">System.Boolean</span></span>

## <span data-ttu-id="903ea-144">Note</span><span class="sxs-lookup"><span data-stu-id="903ea-144">NOTES</span></span>

## <span data-ttu-id="903ea-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="903ea-145">RELATED LINKS</span></span>
