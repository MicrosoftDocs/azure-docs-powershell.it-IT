---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022104"
---
# <span data-ttu-id="b4fd7-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="b4fd7-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="b4fd7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="b4fd7-103">Creare una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="b4fd7-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="b4fd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4fd7-104">SYNTAX</span></span>

### <span data-ttu-id="b4fd7-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b4fd7-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4fd7-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4fd7-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4fd7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4fd7-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4fd7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4fd7-108">DESCRIPTION</span></span>
<span data-ttu-id="b4fd7-109">Creare un App Insights Keys API per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="b4fd7-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="b4fd7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4fd7-110">EXAMPLES</span></span>

### <span data-ttu-id="b4fd7-111">Esempio 1 creare una nuova chiave API per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="b4fd7-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="b4fd7-112">Creare una descrizione della chiave API per l'applicazione Insights come "testapiKey" con le autorizzazioni "ReadTelemetry", "WriteAnnotations" per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="b4fd7-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="b4fd7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4fd7-113">PARAMETERS</span></span>

### <span data-ttu-id="b4fd7-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b4fd7-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="b4fd7-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="b4fd7-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="b4fd7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4fd7-116">-DefaultProfile</span></span>
<span data-ttu-id="b4fd7-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4fd7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4fd7-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4fd7-118">-Description</span></span>
<span data-ttu-id="b4fd7-119">Descrizione che consente di identificare questa chiave API.</span><span class="sxs-lookup"><span data-stu-id="b4fd7-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="b4fd7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b4fd7-120">-Name</span></span>
<span data-ttu-id="b4fd7-121">Nome del componente.</span><span class="sxs-lookup"><span data-stu-id="b4fd7-121">Component Name.</span></span>

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

### <span data-ttu-id="b4fd7-122">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="b4fd7-122">-Permissions</span></span>
<span data-ttu-id="b4fd7-123">Autorizzazioni che la chiave API consente alle app di eseguire.</span><span class="sxs-lookup"><span data-stu-id="b4fd7-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="b4fd7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4fd7-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4fd7-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4fd7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b4fd7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4fd7-126">-ResourceId</span></span>
<span data-ttu-id="b4fd7-127">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="b4fd7-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="b4fd7-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b4fd7-128">-Confirm</span></span>
<span data-ttu-id="b4fd7-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4fd7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4fd7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4fd7-130">-WhatIf</span></span>
<span data-ttu-id="b4fd7-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4fd7-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4fd7-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4fd7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4fd7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4fd7-133">CommonParameters</span></span>
<span data-ttu-id="b4fd7-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4fd7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4fd7-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4fd7-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4fd7-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4fd7-136">INPUTS</span></span>

### <span data-ttu-id="b4fd7-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="b4fd7-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="b4fd7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b4fd7-138">System.String</span></span>

## <span data-ttu-id="b4fd7-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4fd7-139">OUTPUTS</span></span>

### <span data-ttu-id="b4fd7-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="b4fd7-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="b4fd7-141">Note</span><span class="sxs-lookup"><span data-stu-id="b4fd7-141">NOTES</span></span>

## <span data-ttu-id="b4fd7-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4fd7-142">RELATED LINKS</span></span>
