---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/get-azurermapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Get-AzureRmApplicationInsightsApiKey.md
ms.openlocfilehash: 705ebfc151ef4f6bcd5029026ce08ee1da5bd676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518252"
---
# <span data-ttu-id="58de4-101">Get-AzureRmApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="58de4-101">Get-AzureRmApplicationInsightsApiKey</span></span>

## <span data-ttu-id="58de4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58de4-102">SYNOPSIS</span></span>
<span data-ttu-id="58de4-103">Ottenere le chiavi dell'API Application Insights per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="58de4-103">Get application insights api keys for an application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58de4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58de4-104">SYNTAX</span></span>

### <span data-ttu-id="58de4-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58de4-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58de4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58de4-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58de4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58de4-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58de4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58de4-108">DESCRIPTION</span></span>
<span data-ttu-id="58de4-109">Ottenere le chiavi dell'API Application Insights per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="58de4-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="58de4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58de4-110">EXAMPLES</span></span>

### <span data-ttu-id="58de4-111">Esempio 1 ottenere le chiavi API per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="58de4-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="58de4-112">Ottenere le chiavi dell'API Application Insights per la risorsa "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="58de4-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="58de4-113">Esempio 2 ottenere una specifica chiave API per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="58de4-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzureRmApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="58de4-114">Ottenere una chiave API di Insights specifica dell'applicazione ID è "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for Resource "test" nel gruppo di risorse "testGroup".</span><span class="sxs-lookup"><span data-stu-id="58de4-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="58de4-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58de4-115">PARAMETERS</span></span>

### <span data-ttu-id="58de4-116">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="58de4-116">-ApiKeyId</span></span>
<span data-ttu-id="58de4-117">ID chiave API dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="58de4-117">Application Insights Api Key Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58de4-118">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="58de4-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="58de4-119">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="58de4-119">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="58de4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58de4-120">-DefaultProfile</span></span>
<span data-ttu-id="58de4-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58de4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58de4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="58de4-122">-Name</span></span>
<span data-ttu-id="58de4-123">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="58de4-123">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="58de4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58de4-124">-ResourceGroupName</span></span>
<span data-ttu-id="58de4-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58de4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="58de4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58de4-126">-ResourceId</span></span>
<span data-ttu-id="58de4-127">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="58de4-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="58de4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58de4-128">CommonParameters</span></span>
<span data-ttu-id="58de4-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58de4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58de4-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58de4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58de4-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58de4-131">INPUTS</span></span>

### <span data-ttu-id="58de4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="58de4-132">System.String</span></span>

## <span data-ttu-id="58de4-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58de4-133">OUTPUTS</span></span>

### <span data-ttu-id="58de4-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="58de4-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="58de4-135">Note</span><span class="sxs-lookup"><span data-stu-id="58de4-135">NOTES</span></span>

## <span data-ttu-id="58de4-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58de4-136">RELATED LINKS</span></span>

