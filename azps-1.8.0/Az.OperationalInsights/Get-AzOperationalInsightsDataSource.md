---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: f291eedade1a1a243f22dc618ffcc538a9158de6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677820"
---
# <span data-ttu-id="94f57-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="94f57-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="94f57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94f57-102">SYNOPSIS</span></span>
<span data-ttu-id="94f57-103">Ottenere le origini dati in area di lavoro di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="94f57-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="94f57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94f57-104">SYNTAX</span></span>

### <span data-ttu-id="94f57-105">ByWorkspaceNameByKind (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94f57-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94f57-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="94f57-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94f57-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="94f57-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94f57-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="94f57-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94f57-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94f57-109">DESCRIPTION</span></span>
<span data-ttu-id="94f57-110">Il cmdlet **Get-AzOperationalInsightsDataSource** ottiene le origini dati.</span><span class="sxs-lookup"><span data-stu-id="94f57-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="94f57-111">Puoi specificare un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="94f57-111">You can specify a data source to get.</span></span>
<span data-ttu-id="94f57-112">È possibile filtrare i risultati in base al tipo di origine dati.</span><span class="sxs-lookup"><span data-stu-id="94f57-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="94f57-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94f57-113">EXAMPLES</span></span>

## <span data-ttu-id="94f57-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94f57-114">PARAMETERS</span></span>

### <span data-ttu-id="94f57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f57-115">-DefaultProfile</span></span>
<span data-ttu-id="94f57-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="94f57-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94f57-117">-Tipo</span><span class="sxs-lookup"><span data-stu-id="94f57-117">-Kind</span></span>
<span data-ttu-id="94f57-118">Specifica il tipo di origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="94f57-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="94f57-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="94f57-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="94f57-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="94f57-120">AzureActivityLog</span></span> 
- <span data-ttu-id="94f57-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="94f57-121">CustomLog</span></span> 
- <span data-ttu-id="94f57-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="94f57-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="94f57-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="94f57-123">LinuxSyslog</span></span> 
- <span data-ttu-id="94f57-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="94f57-124">WindowsEvent</span></span> 
- <span data-ttu-id="94f57-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="94f57-125">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f57-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="94f57-126">-Name</span></span>
<span data-ttu-id="94f57-127">Specifica il nome di un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="94f57-127">Specifies the name of a data source to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f57-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f57-128">-ResourceGroupName</span></span>
<span data-ttu-id="94f57-129">Specifica il nome di un gruppo di risorse che contiene origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="94f57-129">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f57-130">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="94f57-130">-Workspace</span></span>
<span data-ttu-id="94f57-131">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94f57-131">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94f57-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="94f57-132">-WorkspaceName</span></span>
<span data-ttu-id="94f57-133">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94f57-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f57-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f57-134">CommonParameters</span></span>
<span data-ttu-id="94f57-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f57-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f57-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f57-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f57-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94f57-137">INPUTS</span></span>

### <span data-ttu-id="94f57-138">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="94f57-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="94f57-139">System. String</span><span class="sxs-lookup"><span data-stu-id="94f57-139">System.String</span></span>

## <span data-ttu-id="94f57-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94f57-140">OUTPUTS</span></span>

### <span data-ttu-id="94f57-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="94f57-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="94f57-142">Note</span><span class="sxs-lookup"><span data-stu-id="94f57-142">NOTES</span></span>
* <span data-ttu-id="94f57-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="94f57-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="94f57-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94f57-144">RELATED LINKS</span></span>

[<span data-ttu-id="94f57-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="94f57-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="94f57-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="94f57-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


