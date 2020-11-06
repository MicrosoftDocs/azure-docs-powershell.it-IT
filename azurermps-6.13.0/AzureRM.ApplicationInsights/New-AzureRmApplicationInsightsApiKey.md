---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: c60caa54f11fb2466631cf956cdc374b72265443
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512023"
---
# <span data-ttu-id="b2147-101">New-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="b2147-101">New-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="b2147-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b2147-102">SYNOPSIS</span></span>
<span data-ttu-id="b2147-103">Creare una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="b2147-103">Create an application insights api key for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2147-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b2147-104">SYNTAX</span></span>

### <span data-ttu-id="b2147-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b2147-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2147-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2147-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2147-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2147-107">ResourceIdParameterSet</span></span>
```
New-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2147-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2147-108">DESCRIPTION</span></span>
<span data-ttu-id="b2147-109">Creare un App Insights Keys API per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="b2147-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="b2147-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b2147-110">EXAMPLES</span></span>

### <span data-ttu-id="b2147-111">Esempio 1 creare una nuova chiave API per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="b2147-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="b2147-112">Creare una descrizione della chiave API per l'applicazione Insights come "testapiKey" con le autorizzazioni "ReadTelemetry", "WriteAnnotations" per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="b2147-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="b2147-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b2147-113">PARAMETERS</span></span>

### <span data-ttu-id="b2147-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b2147-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="b2147-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2147-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="b2147-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2147-116">-DefaultProfile</span></span>
<span data-ttu-id="b2147-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b2147-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2147-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2147-118">-Description</span></span>
<span data-ttu-id="b2147-119">Descrizione che consente di identificare questa chiave API.</span><span class="sxs-lookup"><span data-stu-id="b2147-119">Description to help identify this API key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2147-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2147-120">-Name</span></span>
<span data-ttu-id="b2147-121">Nome del componente.</span><span class="sxs-lookup"><span data-stu-id="b2147-121">Component Name.</span></span>

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

### <span data-ttu-id="b2147-122">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="b2147-122">-Permissions</span></span>
<span data-ttu-id="b2147-123">Autorizzazioni che la chiave API consente alle app di eseguire.</span><span class="sxs-lookup"><span data-stu-id="b2147-123">Permissions that API key allow apps to do.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2147-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2147-124">-ResourceGroupName</span></span>
<span data-ttu-id="b2147-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b2147-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b2147-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2147-126">-ResourceId</span></span>
<span data-ttu-id="b2147-127">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="b2147-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="b2147-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b2147-128">-Confirm</span></span>
<span data-ttu-id="b2147-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2147-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2147-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2147-130">-WhatIf</span></span>
<span data-ttu-id="b2147-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2147-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2147-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b2147-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2147-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2147-133">CommonParameters</span></span>
<span data-ttu-id="b2147-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2147-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2147-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2147-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2147-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b2147-136">INPUTS</span></span>

### <span data-ttu-id="b2147-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b2147-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>
<span data-ttu-id="b2147-138">Parametri: ApplicationInsightsComponent (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b2147-138">Parameters: ApplicationInsightsComponent (ByValue)</span></span>

### <span data-ttu-id="b2147-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b2147-139">System.String</span></span>

## <span data-ttu-id="b2147-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b2147-140">OUTPUTS</span></span>

### <span data-ttu-id="b2147-141">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="b2147-141">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="b2147-142">Note</span><span class="sxs-lookup"><span data-stu-id="b2147-142">NOTES</span></span>

## <span data-ttu-id="b2147-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b2147-143">RELATED LINKS</span></span>
