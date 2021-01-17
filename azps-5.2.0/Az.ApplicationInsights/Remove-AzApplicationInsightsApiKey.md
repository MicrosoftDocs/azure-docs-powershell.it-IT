---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353503"
---
# <span data-ttu-id="c6cc5-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c6cc5-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="c6cc5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c6cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="c6cc5-103">Rimuovere una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="c6cc5-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="c6cc5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6cc5-104">SYNTAX</span></span>

### <span data-ttu-id="c6cc5-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6cc5-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6cc5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6cc5-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6cc5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6cc5-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6cc5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6cc5-108">DESCRIPTION</span></span>
<span data-ttu-id="c6cc5-109">Rimuovere una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="c6cc5-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="c6cc5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6cc5-110">EXAMPLES</span></span>

### <span data-ttu-id="c6cc5-111">Esempio 1 rimuovere una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="c6cc5-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="c6cc5-112">Rimuovere le informazioni chiave API specifiche dell'applicazione che ID è "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="c6cc5-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="c6cc5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c6cc5-113">PARAMETERS</span></span>

### <span data-ttu-id="c6cc5-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="c6cc5-114">-ApiKeyId</span></span>
<span data-ttu-id="c6cc5-115">ID chiave API dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="c6cc5-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c6cc5-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c6cc5-117">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c6cc5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6cc5-118">-DefaultProfile</span></span>
<span data-ttu-id="c6cc5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6cc5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6cc5-120">-Name</span></span>
<span data-ttu-id="c6cc5-121">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c6cc5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6cc5-122">-PassThru</span></span>
<span data-ttu-id="c6cc5-123">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="c6cc5-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-124">This parameter is optional.</span></span> <span data-ttu-id="c6cc5-125">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-125">Default value is false.</span></span>

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

### <span data-ttu-id="c6cc5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6cc5-126">-ResourceGroupName</span></span>
<span data-ttu-id="c6cc5-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c6cc5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6cc5-128">-ResourceId</span></span>
<span data-ttu-id="c6cc5-129">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c6cc5-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c6cc5-130">-Confirm</span></span>
<span data-ttu-id="c6cc5-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6cc5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6cc5-132">-WhatIf</span></span>
<span data-ttu-id="c6cc5-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6cc5-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6cc5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6cc5-135">CommonParameters</span></span>
<span data-ttu-id="c6cc5-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6cc5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6cc5-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6cc5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6cc5-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c6cc5-138">INPUTS</span></span>

### <span data-ttu-id="c6cc5-139">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c6cc5-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="c6cc5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c6cc5-140">System.String</span></span>

## <span data-ttu-id="c6cc5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6cc5-141">OUTPUTS</span></span>

### <span data-ttu-id="c6cc5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6cc5-142">System.Boolean</span></span>

## <span data-ttu-id="c6cc5-143">Note</span><span class="sxs-lookup"><span data-stu-id="c6cc5-143">NOTES</span></span>

## <span data-ttu-id="c6cc5-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6cc5-144">RELATED LINKS</span></span>
