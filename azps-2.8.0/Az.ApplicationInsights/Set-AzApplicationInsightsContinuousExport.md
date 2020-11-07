---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/set-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Set-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 3927997ddca6c58c4ac97a0234291cac08777c6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675849"
---
# <span data-ttu-id="0efe7-101">Set-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="0efe7-101">Set-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="0efe7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0efe7-102">SYNOPSIS</span></span>
<span data-ttu-id="0efe7-103">Aggiornare una configurazione di esportazione continua in una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="0efe7-103">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="0efe7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0efe7-104">SYNTAX</span></span>

### <span data-ttu-id="0efe7-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0efe7-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0efe7-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0efe7-106">ComponentObjectParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0efe7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0efe7-107">ResourceIdParameterSet</span></span>
```
Set-AzApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String> [-DisableConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0efe7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0efe7-108">DESCRIPTION</span></span>
<span data-ttu-id="0efe7-109">Aggiornare una configurazione di esportazione continua in una risorsa approfondimenti applicazione</span><span class="sxs-lookup"><span data-stu-id="0efe7-109">Update a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="0efe7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0efe7-110">EXAMPLES</span></span>

### <span data-ttu-id="0efe7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0efe7-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -StorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -StorageLocation sourcecentralus
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

<span data-ttu-id="0efe7-112">Aggiornare la configurazione di esportazione continua "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" della risorsa "test" nel gruppo di risorse "testgroup" per esportare i documenti "Request" e "Trace" nel contenitore di archiviazione "testcontainer" in "teststorageaccount". Il token SAS deve essere valido e avere l'autorizzazione di scrittura per il contenitore, altrimenti la caratteristica di esportazione continua non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="0efe7-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.</span></span> <span data-ttu-id="0efe7-113">Se il token SAS è scaduto, la caratteristica di esportazione continua smetterà di funzionare.</span><span class="sxs-lookup"><span data-stu-id="0efe7-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="0efe7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0efe7-114">PARAMETERS</span></span>

### <span data-ttu-id="0efe7-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0efe7-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0efe7-116">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="0efe7-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="0efe7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0efe7-117">-DefaultProfile</span></span>
<span data-ttu-id="0efe7-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0efe7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0efe7-119">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="0efe7-119">-DisableConfiguration</span></span>
<span data-ttu-id="0efe7-120">Disabilitare o meno l'esportazione continua.</span><span class="sxs-lookup"><span data-stu-id="0efe7-120">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="0efe7-121">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="0efe7-121">-DocumentType</span></span>
<span data-ttu-id="0efe7-122">Tipi di documento che devono essere esportati.</span><span class="sxs-lookup"><span data-stu-id="0efe7-122">Document types that need exported.</span></span>

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

### <span data-ttu-id="0efe7-123">-ExportId</span><span class="sxs-lookup"><span data-stu-id="0efe7-123">-ExportId</span></span>
<span data-ttu-id="0efe7-124">ID dell'esportazione continuo dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="0efe7-124">Application Insights Continuous Export Id.</span></span>

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

### <span data-ttu-id="0efe7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="0efe7-125">-Name</span></span>
<span data-ttu-id="0efe7-126">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="0efe7-126">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="0efe7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0efe7-127">-ResourceGroupName</span></span>
<span data-ttu-id="0efe7-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0efe7-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="0efe7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0efe7-129">-ResourceId</span></span>
<span data-ttu-id="0efe7-130">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="0efe7-130">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0efe7-131">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0efe7-131">-StorageAccountId</span></span>
<span data-ttu-id="0efe7-132">ID account di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0efe7-132">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="0efe7-133">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="0efe7-133">-StorageLocation</span></span>
<span data-ttu-id="0efe7-134">ID posizione di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0efe7-134">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="0efe7-135">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="0efe7-135">-StorageSASUri</span></span>
<span data-ttu-id="0efe7-136">URI SAS di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0efe7-136">Destination Storage SAS uri.</span></span>

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

### <span data-ttu-id="0efe7-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0efe7-137">-Confirm</span></span>
<span data-ttu-id="0efe7-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0efe7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0efe7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0efe7-139">-WhatIf</span></span>
<span data-ttu-id="0efe7-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0efe7-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0efe7-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0efe7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0efe7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efe7-142">CommonParameters</span></span>
<span data-ttu-id="0efe7-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0efe7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efe7-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0efe7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efe7-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0efe7-145">INPUTS</span></span>

### <span data-ttu-id="0efe7-146">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0efe7-146">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="0efe7-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0efe7-147">System.String</span></span>

## <span data-ttu-id="0efe7-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0efe7-148">OUTPUTS</span></span>

### <span data-ttu-id="0efe7-149">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="0efe7-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="0efe7-150">Note</span><span class="sxs-lookup"><span data-stu-id="0efe7-150">NOTES</span></span>

## <span data-ttu-id="0efe7-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0efe7-151">RELATED LINKS</span></span>