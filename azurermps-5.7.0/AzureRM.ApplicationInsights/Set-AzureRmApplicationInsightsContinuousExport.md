---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 7b426f7f6b494c92d86a41217000b2d2335c7d91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520482"
---
# <span data-ttu-id="df19e-101">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="df19e-101">Set-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="df19e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df19e-102">SYNOPSIS</span></span>
<span data-ttu-id="df19e-103">Aggiornare una configurazione di esportazione continua in una risorsa applciation Insights</span><span class="sxs-lookup"><span data-stu-id="df19e-103">Update a continuous export configuration in an applciation insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df19e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df19e-104">SYNTAX</span></span>

### <span data-ttu-id="df19e-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="df19e-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df19e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df19e-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df19e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df19e-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df19e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df19e-108">DESCRIPTION</span></span>
<span data-ttu-id="df19e-109">Aggiornare una configurazione di esportazione continua in una risorsa applciation Insights</span><span class="sxs-lookup"><span data-stu-id="df19e-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="df19e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df19e-110">EXAMPLES</span></span>

### <span data-ttu-id="df19e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="df19e-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -DestinationStorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -DestinationStorageLocationId sourcecentralus
 -DestinationStorageSASUri $sasuri

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

<span data-ttu-id="df19e-112">Aggiornare la configurazione di esportazione continua "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" della risorsa "test" nel gruppo di risorse "testgroup" per esportare i documenti "Request" e "Trace" nel contenitore di archiviazione "testcontainer" in "teststorageaccount". Il token SAS deve essere valido e avere l'autorizzazione di scrittura per il contenitore, altrimenti la caratteristica di esportazione continua non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="df19e-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="df19e-113">Se il token SAS è scaduto, la caratteristica di esportazione continua smetterà di funzionare.</span><span class="sxs-lookup"><span data-stu-id="df19e-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="df19e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df19e-114">PARAMETERS</span></span>

### <span data-ttu-id="df19e-115">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="df19e-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="df19e-116">Oggetto componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="df19e-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="df19e-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="df19e-117">-Confirm</span></span>
<span data-ttu-id="df19e-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df19e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df19e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df19e-119">-DefaultProfile</span></span>
<span data-ttu-id="df19e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df19e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df19e-121">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="df19e-121">-DisableConfiguration</span></span>
<span data-ttu-id="df19e-122">Disabilitare o meno l'esportazione continua.</span><span class="sxs-lookup"><span data-stu-id="df19e-122">Disable continuous export or not.</span></span>

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

### <span data-ttu-id="df19e-123">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="df19e-123">-DocumentType</span></span>
<span data-ttu-id="df19e-124">Tipi di documento che devono essere esportati.</span><span class="sxs-lookup"><span data-stu-id="df19e-124">Document types that need exported.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df19e-125">-ExportId</span><span class="sxs-lookup"><span data-stu-id="df19e-125">-ExportId</span></span>
<span data-ttu-id="df19e-126">ID dell'esportazione continuo dell'applicazione Insights.</span><span class="sxs-lookup"><span data-stu-id="df19e-126">Application Insights Continuous Export Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df19e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="df19e-127">-Name</span></span>
<span data-ttu-id="df19e-128">Nome del componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="df19e-128">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="df19e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df19e-129">-ResourceGroupName</span></span>
<span data-ttu-id="df19e-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="df19e-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="df19e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df19e-131">-ResourceId</span></span>
<span data-ttu-id="df19e-132">ID risorsa componente approfondimenti applicazione.</span><span class="sxs-lookup"><span data-stu-id="df19e-132">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="df19e-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="df19e-133">-StorageAccountId</span></span>
<span data-ttu-id="df19e-134">ID account di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df19e-134">Destination Storage Account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df19e-135">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="df19e-135">-StorageLocation</span></span>
<span data-ttu-id="df19e-136">ID posizione di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df19e-136">Destination Storage Location Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df19e-137">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="df19e-137">-StorageSASUri</span></span>
<span data-ttu-id="df19e-138">URI SAS di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df19e-138">Destination Storage SAS uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df19e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df19e-139">-WhatIf</span></span>
<span data-ttu-id="df19e-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df19e-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df19e-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df19e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df19e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df19e-142">CommonParameters</span></span>
<span data-ttu-id="df19e-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df19e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df19e-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df19e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df19e-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df19e-145">INPUTS</span></span>

### <span data-ttu-id="df19e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="df19e-146">System.String</span></span>
<span data-ttu-id="df19e-147">System. String [] System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df19e-147">System.String[] System.Boolean</span></span>

## <span data-ttu-id="df19e-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df19e-148">OUTPUTS</span></span>

### <span data-ttu-id="df19e-149">Microsoft. Azure. Commands. ApplicationInsights. Models. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="df19e-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="df19e-150">Note</span><span class="sxs-lookup"><span data-stu-id="df19e-150">NOTES</span></span>

## <span data-ttu-id="df19e-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df19e-151">RELATED LINKS</span></span>

