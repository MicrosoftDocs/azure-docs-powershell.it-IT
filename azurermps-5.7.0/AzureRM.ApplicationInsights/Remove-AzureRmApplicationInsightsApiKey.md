---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 7fbf269b43868724b015bd087536c49ccce71f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519947"
---
# <span data-ttu-id="0f471-101">Remove-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="0f471-101">Remove-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="0f471-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f471-102">SYNOPSIS</span></span>
<span data-ttu-id="0f471-103">Rimuovere una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="0f471-103">Remove an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f471-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f471-104">SYNTAX</span></span>

### <span data-ttu-id="0f471-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f471-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f471-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f471-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f471-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f471-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f471-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f471-108">DESCRIPTION</span></span>
<span data-ttu-id="0f471-109">Rimuovere una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="0f471-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="0f471-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f471-110">EXAMPLES</span></span>

### <span data-ttu-id="0f471-111">Esempio 1 rimuovere una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="0f471-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="0f471-112">Rimuovere le informazioni chiave API specifiche dell'applicazione che ID è "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="0f471-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="0f471-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f471-113">PARAMETERS</span></span>

### <span data-ttu-id="0f471-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="0f471-114">-ApiKeyId</span></span>
<span data-ttu-id="0f471-115">ID chiave API dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="0f471-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="0f471-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0f471-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0f471-117">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="0f471-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="0f471-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0f471-118">-Confirm</span></span>
<span data-ttu-id="0f471-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f471-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f471-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f471-120">-DefaultProfile</span></span>
<span data-ttu-id="0f471-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f471-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f471-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f471-122">-Name</span></span>
<span data-ttu-id="0f471-123">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="0f471-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="0f471-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f471-124">-PassThru</span></span>
<span data-ttu-id="0f471-125">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="0f471-125">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="0f471-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0f471-126">This parameter is optional.</span></span> <span data-ttu-id="0f471-127">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="0f471-127">Default value is false.</span></span>

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

### <span data-ttu-id="0f471-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f471-128">-ResourceGroupName</span></span>
<span data-ttu-id="0f471-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f471-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="0f471-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f471-130">-ResourceId</span></span>
<span data-ttu-id="0f471-131">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="0f471-131">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0f471-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f471-132">-WhatIf</span></span>
<span data-ttu-id="0f471-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f471-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f471-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f471-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f471-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f471-135">CommonParameters</span></span>
<span data-ttu-id="0f471-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f471-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f471-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f471-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f471-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f471-138">INPUTS</span></span>

### <span data-ttu-id="0f471-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0f471-139">System.String</span></span>

## <span data-ttu-id="0f471-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f471-140">OUTPUTS</span></span>

### <span data-ttu-id="0f471-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="0f471-141">System.Object</span></span>

## <span data-ttu-id="0f471-142">Note</span><span class="sxs-lookup"><span data-stu-id="0f471-142">NOTES</span></span>

## <span data-ttu-id="0f471-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f471-143">RELATED LINKS</span></span>

