---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 97994eb9898f5eca3e8f7f3015e2ce96845d5c24
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182271"
---
# <span data-ttu-id="d4496-101">New-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="d4496-101">New-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="d4496-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4496-102">SYNOPSIS</span></span>
<span data-ttu-id="d4496-103">Creare una nuova configurazione continua di Informazioni dettagliate sull'applicazione per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="d4496-103">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="d4496-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4496-104">SYNTAX</span></span>

### <span data-ttu-id="d4496-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4496-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4496-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4496-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4496-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4496-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsContinuousExport [-ResourceId] <String> -DocumentType <String[]>
 -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4496-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4496-108">DESCRIPTION</span></span>
<span data-ttu-id="d4496-109">Creare una nuova configurazione continua di Informazioni dettagliate sull'applicazione per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="d4496-109">Create a new application insights continuous export configuration for an application insights resource</span></span>

## <span data-ttu-id="d4496-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4496-110">EXAMPLES</span></span>

### <span data-ttu-id="d4496-111">Esempio 1: Creare una nuova configurazione di esportazione continua per una risorsa di Application Insights</span><span class="sxs-lookup"><span data-stu-id="d4496-111">Example 1 Create a new continuous export configuration for an application insights resource</span></span>
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

<span data-ttu-id="d4496-112">Creare una nuova configurazione continua di informazioni sull'applicazione per esportare i tipi di documento "Richiesta" e "Traccia" per l'archiviazione che contengono "testcontainer" nell'account di archiviazione "teststorageaccount" nel gruppo di risorse "testgroup".</span><span class="sxs-lookup"><span data-stu-id="d4496-112">Create a new application insights continuous export configuration to export "Request" and "Trace" document types to storage contain "testcontainer" in storage account "teststorageaccount" in resource group "testgroup".</span></span> <span data-ttu-id="d4496-113">Il token di firma di accesso condiviso deve essere valido e avere l'autorizzazione di scrittura per il contenitore, altrimenti la caratteristica di esportazione continua non funzionerà. Se il token di firma di accesso condiviso è scaduto, la caratteristica di esportazione continua smetterà di funzionare.</span><span class="sxs-lookup"><span data-stu-id="d4496-113">The SAS token have to be valid and have write permission to the container, otherwise continuous export feature won't work.If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="d4496-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4496-114">PARAMETERS</span></span>

### <span data-ttu-id="d4496-115">-ApplicationInsightsInsightsIn</span><span class="sxs-lookup"><span data-stu-id="d4496-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="d4496-116">Oggetto componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d4496-116">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="d4496-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4496-117">-DefaultProfile</span></span>
<span data-ttu-id="d4496-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4496-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4496-119">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="d4496-119">-DocumentType</span></span>
<span data-ttu-id="d4496-120">Tipi di documento che devono essere esportati.</span><span class="sxs-lookup"><span data-stu-id="d4496-120">Document types that need exported.</span></span>

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

### <span data-ttu-id="d4496-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d4496-121">-Name</span></span>
<span data-ttu-id="d4496-122">Nome componente.</span><span class="sxs-lookup"><span data-stu-id="d4496-122">Component Name.</span></span>

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

### <span data-ttu-id="d4496-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4496-123">-ResourceGroupName</span></span>
<span data-ttu-id="d4496-124">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4496-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="d4496-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4496-125">-ResourceId</span></span>
<span data-ttu-id="d4496-126">ID risorsa componente Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d4496-126">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="d4496-127">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d4496-127">-StorageAccountId</span></span>
<span data-ttu-id="d4496-128">ID account di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d4496-128">Destination Storage Account Id.</span></span>

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

### <span data-ttu-id="d4496-129">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="d4496-129">-StorageLocation</span></span>
<span data-ttu-id="d4496-130">ID posizione di archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d4496-130">Destination Storage Location Id.</span></span>

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

### <span data-ttu-id="d4496-131">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="d4496-131">-StorageSASUri</span></span>
<span data-ttu-id="d4496-132">Uri della firma di accesso condiviso per l'archiviazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d4496-132">Destination Storage SAS Uri.</span></span>

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

### <span data-ttu-id="d4496-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4496-133">-Confirm</span></span>
<span data-ttu-id="d4496-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4496-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4496-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4496-135">-WhatIf</span></span>
<span data-ttu-id="d4496-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4496-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4496-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4496-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4496-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4496-138">CommonParameters</span></span>
<span data-ttu-id="d4496-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4496-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4496-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4496-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4496-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4496-141">INPUTS</span></span>

### <span data-ttu-id="d4496-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsights Insights</span><span class="sxs-lookup"><span data-stu-id="d4496-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="d4496-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d4496-143">System.String</span></span>

## <span data-ttu-id="d4496-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4496-144">OUTPUTS</span></span>

### <span data-ttu-id="d4496-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4496-145">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="d4496-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4496-146">NOTES</span></span>

## <span data-ttu-id="d4496-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4496-147">RELATED LINKS</span></span>
