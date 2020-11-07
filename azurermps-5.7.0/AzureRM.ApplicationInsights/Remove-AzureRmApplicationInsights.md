---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/remove-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Remove-AzureRmApplicationInsights.md
ms.openlocfilehash: a440dd37d26bf65f4deb8c7e4c4535f6460f76be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687054"
---
# <span data-ttu-id="f6ac4-101">Remove-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="f6ac4-101">Remove-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="f6ac4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ac4-103">Rimuovere una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="f6ac4-103">Remove an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6ac4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6ac4-104">SYNTAX</span></span>

### <span data-ttu-id="f6ac4-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6ac4-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6ac4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6ac4-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6ac4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6ac4-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6ac4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6ac4-108">DESCRIPTION</span></span>
<span data-ttu-id="f6ac4-109">Rimuovere una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="f6ac4-109">Remove an application insights resource</span></span>

## <span data-ttu-id="f6ac4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6ac4-110">EXAMPLES</span></span>

### <span data-ttu-id="f6ac4-111">Esempio 1 rimuovere una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="f6ac4-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzureRmApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="f6ac4-112">Rimuovere una risorsa applciation Insights denominata "test" nel gruppo di risorse "testgroup"</span><span class="sxs-lookup"><span data-stu-id="f6ac4-112">Remove an applciation insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="f6ac4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6ac4-113">PARAMETERS</span></span>

### <span data-ttu-id="f6ac4-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f6ac4-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="f6ac4-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="f6ac4-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f6ac4-116">-Confirm</span></span>
<span data-ttu-id="f6ac4-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6ac4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ac4-118">-DefaultProfile</span></span>
<span data-ttu-id="f6ac4-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6ac4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6ac4-120">-Name</span></span>
<span data-ttu-id="f6ac4-121">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="f6ac4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6ac4-122">-PassThru</span></span>
<span data-ttu-id="f6ac4-123">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="f6ac4-124">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-124">This parameter is optional.</span></span> <span data-ttu-id="f6ac4-125">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-125">Default value is false.</span></span>

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

### <span data-ttu-id="f6ac4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ac4-126">-ResourceGroupName</span></span>
<span data-ttu-id="f6ac4-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f6ac4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6ac4-128">-ResourceId</span></span>
<span data-ttu-id="f6ac4-129">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="f6ac4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6ac4-130">-WhatIf</span></span>
<span data-ttu-id="f6ac4-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6ac4-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6ac4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ac4-133">CommonParameters</span></span>
<span data-ttu-id="f6ac4-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6ac4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ac4-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6ac4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ac4-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6ac4-136">INPUTS</span></span>

### <span data-ttu-id="f6ac4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f6ac4-137">System.String</span></span>

## <span data-ttu-id="f6ac4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6ac4-138">OUTPUTS</span></span>

### <span data-ttu-id="f6ac4-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="f6ac4-139">System.Object</span></span>

## <span data-ttu-id="f6ac4-140">Note</span><span class="sxs-lookup"><span data-stu-id="f6ac4-140">NOTES</span></span>

## <span data-ttu-id="f6ac4-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6ac4-141">RELATED LINKS</span></span>

