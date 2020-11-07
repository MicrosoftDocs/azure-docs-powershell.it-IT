---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: c4f972971b52e6ff8e7bac4ebcb0850ef71846ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685122"
---
# <span data-ttu-id="8b15f-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="8b15f-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="8b15f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b15f-102">SYNOPSIS</span></span>
<span data-ttu-id="8b15f-103">Creare una chiave API Insights Application per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="8b15f-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="8b15f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b15f-104">SYNTAX</span></span>

### <span data-ttu-id="8b15f-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b15f-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b15f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b15f-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b15f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b15f-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b15f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b15f-108">DESCRIPTION</span></span>
<span data-ttu-id="8b15f-109">Creare un App Insights Keys API per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="8b15f-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="8b15f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b15f-110">EXAMPLES</span></span>

### <span data-ttu-id="8b15f-111">Esempio 1 creare una nuova chiave API per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="8b15f-111">Example 1 Create a new Api Key for an application insights resource</span></span>
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

<span data-ttu-id="8b15f-112">Creare una descrizione della chiave API per l'applicazione Insights come "testapiKey" con le autorizzazioni "ReadTelemetry", "WriteAnnotations" per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="8b15f-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="8b15f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b15f-113">PARAMETERS</span></span>

### <span data-ttu-id="8b15f-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8b15f-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="8b15f-115">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="8b15f-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="8b15f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b15f-116">-DefaultProfile</span></span>
<span data-ttu-id="8b15f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b15f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b15f-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b15f-118">-Description</span></span>
<span data-ttu-id="8b15f-119">Descrizione che consente di identificare questa chiave API.</span><span class="sxs-lookup"><span data-stu-id="8b15f-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="8b15f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b15f-120">-Name</span></span>
<span data-ttu-id="8b15f-121">Nome del componente.</span><span class="sxs-lookup"><span data-stu-id="8b15f-121">Component Name.</span></span>

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

### <span data-ttu-id="8b15f-122">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="8b15f-122">-Permissions</span></span>
<span data-ttu-id="8b15f-123">Autorizzazioni che la chiave API consente alle app di eseguire.</span><span class="sxs-lookup"><span data-stu-id="8b15f-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="8b15f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b15f-124">-ResourceGroupName</span></span>
<span data-ttu-id="8b15f-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b15f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8b15f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b15f-126">-ResourceId</span></span>
<span data-ttu-id="8b15f-127">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="8b15f-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="8b15f-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8b15f-128">-Confirm</span></span>
<span data-ttu-id="8b15f-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b15f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b15f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b15f-130">-WhatIf</span></span>
<span data-ttu-id="8b15f-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b15f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b15f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b15f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b15f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b15f-133">CommonParameters</span></span>
<span data-ttu-id="8b15f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b15f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b15f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b15f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b15f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b15f-136">INPUTS</span></span>

### <span data-ttu-id="8b15f-137">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="8b15f-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="8b15f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8b15f-138">System.String</span></span>

## <span data-ttu-id="8b15f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b15f-139">OUTPUTS</span></span>

### <span data-ttu-id="8b15f-140">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="8b15f-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="8b15f-141">Note</span><span class="sxs-lookup"><span data-stu-id="8b15f-141">NOTES</span></span>

## <span data-ttu-id="8b15f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b15f-142">RELATED LINKS</span></span>
