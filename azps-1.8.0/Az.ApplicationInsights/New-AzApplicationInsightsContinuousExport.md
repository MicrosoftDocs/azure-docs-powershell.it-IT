---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: f30d5da085658c979a52f166469e4e548afdaf7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852325"
---
# <span data-ttu-id="5aee3-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="5aee3-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="5aee3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5aee3-102">SYNOPSIS</span></span>
<span data-ttu-id="5aee3-103">Creare una nuova applicazione Insights Continuous Export Configuration per una risorsa Insights Application</span><span class="sxs-lookup"><span data-stu-id="5aee3-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="5aee3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5aee3-104">SYNTAX</span></span>

### <span data-ttu-id="5aee3-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5aee3-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5aee3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5aee3-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5aee3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5aee3-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aee3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5aee3-108">DESCRIPTION</span></span>
<span data-ttu-id="5aee3-109">Creare una nuova applicazione Insights Continuous Export Configuration per una risorsa Insights Application</span><span class="sxs-lookup"><span data-stu-id="5aee3-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="5aee3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5aee3-110">EXAMPLES</span></span>

### <span data-ttu-id="5aee3-111">Esempio 1 creare una nuova configurazione di esportazione continua per una risorsa Insights applicazione</span><span class="sxs-lookup"><span data-stu-id="5aee3-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> New-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentType "Request","Trace", "Custom Event" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
 -StorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="5aee3-112">Creare una nuova applicazione approfondimenti la configurazione di esportazione continua per esportare i tipi di documento "Request" e "Trace" in Storage contengono "testcontainer" nell'account di archiviazione "teststorageaccount" nel gruppo di risorse "testgroup".</span><span class="sxs-lookup"><span data-stu-id="5aee3-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="5aee3-113">Il token SAS deve essere valido e avere l'autorizzazione di scrittura per il contenitore, altrimenti la caratteristica di esportazione continua non funzionerà. Se il token SAS è scaduto, la caratteristica di esportazione continua smetterà di funzionare.</span><span class="sxs-lookup"><span data-stu-id="5aee3-113">The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="5aee3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5aee3-114">PARAMETERS</span></span>

### <span data-ttu-id="5aee3-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5aee3-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="5aee3-116">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="5aee3-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="5aee3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aee3-117">-DefaultProfile</span></span>
<span data-ttu-id="5aee3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5aee3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5aee3-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="5aee3-119">-DocumentType</span></span>
<span data-ttu-id="5aee3-120">Tipi di documento che devono essere esportati.</span><span class="sxs-lookup"><span data-stu-id="5aee3-120">Document types that need exported.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aee3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5aee3-121">-Name</span></span>
<span data-ttu-id="5aee3-122">Nome del componente.</span><span class="sxs-lookup"><span data-stu-id="5aee3-122">Component Name.</span></span>

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

### <span data-ttu-id="5aee3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aee3-123">-ResourceGroupName</span></span>
<span data-ttu-id="5aee3-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5aee3-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="5aee3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5aee3-125">-ResourceId</span></span>
<span data-ttu-id="5aee3-126">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="5aee3-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="5aee3-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5aee3-127">-StorageAccountId</span></span>
<span data-ttu-id="5aee3-128">ID account di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5aee3-128">Destination Storage Account Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aee3-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="5aee3-129">-StorageLocation</span></span>
<span data-ttu-id="5aee3-130">ID posizione di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5aee3-130">Destination Storage Location Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aee3-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="5aee3-131">-StorageSASUri</span></span>
<span data-ttu-id="5aee3-132">URI SAS di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5aee3-132">Destination Storage SAS Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aee3-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5aee3-133">-Confirm</span></span>
<span data-ttu-id="5aee3-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5aee3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aee3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aee3-135">-WhatIf</span></span>
<span data-ttu-id="5aee3-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5aee3-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5aee3-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5aee3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aee3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aee3-138">CommonParameters</span></span>
<span data-ttu-id="5aee3-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aee3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aee3-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aee3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aee3-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5aee3-141">INPUTS</span></span>

### <span data-ttu-id="5aee3-142">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5aee3-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="5aee3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5aee3-143">System.String</span></span>

## <span data-ttu-id="5aee3-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5aee3-144">OUTPUTS</span></span>

### <span data-ttu-id="5aee3-145">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aee3-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="5aee3-146">Note</span><span class="sxs-lookup"><span data-stu-id="5aee3-146">NOTES</span></span>

## <span data-ttu-id="5aee3-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5aee3-147">RELATED LINKS</span></span>
