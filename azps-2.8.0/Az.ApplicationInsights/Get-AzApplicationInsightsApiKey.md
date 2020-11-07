---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: bf5051f22d06e9e248501ecfb602bd47d3faaf39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675864"
---
# <span data-ttu-id="ac336-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="ac336-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="ac336-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac336-102">SYNOPSIS</span></span>
<span data-ttu-id="ac336-103">Ottenere le chiavi dell'API Application Insights per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="ac336-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="ac336-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac336-104">SYNTAX</span></span>

### <span data-ttu-id="ac336-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac336-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac336-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac336-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac336-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac336-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac336-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac336-108">DESCRIPTION</span></span>
<span data-ttu-id="ac336-109">Ottenere le chiavi dell'API Application Insights per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="ac336-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="ac336-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac336-110">EXAMPLES</span></span>

### <span data-ttu-id="ac336-111">Esempio 1 ottenere le chiavi API per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="ac336-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="ac336-112">Ottenere le chiavi dell'API Application Insights per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="ac336-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="ac336-113">Esempio 2 ottenere una specifica chiave API per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="ac336-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="ac336-114">Ottenere una chiave API di Insights specifica dell'applicazione ID è "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for Resource "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="ac336-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="ac336-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac336-115">PARAMETERS</span></span>

### <span data-ttu-id="ac336-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="ac336-116">-ApiKeyId</span></span>
<span data-ttu-id="ac336-117">ID chiave API dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="ac336-117">Application Insights Api Key Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac336-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ac336-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="ac336-119">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="ac336-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="ac336-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac336-120">-DefaultProfile</span></span>
<span data-ttu-id="ac336-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac336-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac336-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac336-122">-Name</span></span>
<span data-ttu-id="ac336-123">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="ac336-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="ac336-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac336-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac336-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac336-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ac336-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac336-126">-ResourceId</span></span>
<span data-ttu-id="ac336-127">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="ac336-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="ac336-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac336-128">CommonParameters</span></span>
<span data-ttu-id="ac336-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac336-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac336-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac336-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac336-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac336-131">INPUTS</span></span>

### <span data-ttu-id="ac336-132">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ac336-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="ac336-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ac336-133">System.String</span></span>

## <span data-ttu-id="ac336-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac336-134">OUTPUTS</span></span>

### <span data-ttu-id="ac336-135">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="ac336-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="ac336-136">Note</span><span class="sxs-lookup"><span data-stu-id="ac336-136">NOTES</span></span>

## <span data-ttu-id="ac336-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac336-137">RELATED LINKS</span></span>
