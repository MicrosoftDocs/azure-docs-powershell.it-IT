---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032277"
---
# <span data-ttu-id="27cf5-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="27cf5-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="27cf5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="27cf5-103">Ottenere le origini dati in area di lavoro di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="27cf5-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="27cf5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27cf5-104">SYNTAX</span></span>

### <span data-ttu-id="27cf5-105">ByWorkspaceNameByKind (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27cf5-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27cf5-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="27cf5-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27cf5-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="27cf5-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27cf5-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="27cf5-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27cf5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27cf5-109">DESCRIPTION</span></span>
<span data-ttu-id="27cf5-110">Il cmdlet **Get-AzOperationalInsightsDataSource** ottiene le origini dati.</span><span class="sxs-lookup"><span data-stu-id="27cf5-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="27cf5-111">Puoi specificare un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="27cf5-111">You can specify a data source to get.</span></span>
<span data-ttu-id="27cf5-112">È possibile filtrare i risultati in base al tipo di origine dati.</span><span class="sxs-lookup"><span data-stu-id="27cf5-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="27cf5-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27cf5-113">EXAMPLES</span></span>

## <span data-ttu-id="27cf5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27cf5-114">PARAMETERS</span></span>

### <span data-ttu-id="27cf5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27cf5-115">-DefaultProfile</span></span>
<span data-ttu-id="27cf5-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="27cf5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27cf5-117">-Tipo</span><span class="sxs-lookup"><span data-stu-id="27cf5-117">-Kind</span></span>
<span data-ttu-id="27cf5-118">Specifica il tipo di origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="27cf5-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="27cf5-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="27cf5-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="27cf5-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="27cf5-120">AzureActivityLog</span></span> 
- <span data-ttu-id="27cf5-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="27cf5-121">CustomLog</span></span> 
- <span data-ttu-id="27cf5-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="27cf5-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="27cf5-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="27cf5-123">LinuxSyslog</span></span> 
- <span data-ttu-id="27cf5-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="27cf5-124">WindowsEvent</span></span> 
- <span data-ttu-id="27cf5-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="27cf5-125">WindowsPerformanceCounter</span></span>

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

### <span data-ttu-id="27cf5-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="27cf5-126">-Name</span></span>
<span data-ttu-id="27cf5-127">Specifica il nome di un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="27cf5-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="27cf5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27cf5-128">-ResourceGroupName</span></span>
<span data-ttu-id="27cf5-129">Specifica il nome di un gruppo di risorse che contiene origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="27cf5-129">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="27cf5-130">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="27cf5-130">-Workspace</span></span>
<span data-ttu-id="27cf5-131">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27cf5-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="27cf5-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="27cf5-132">-WorkspaceName</span></span>
<span data-ttu-id="27cf5-133">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27cf5-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="27cf5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27cf5-134">CommonParameters</span></span>
<span data-ttu-id="27cf5-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27cf5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27cf5-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27cf5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27cf5-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27cf5-137">INPUTS</span></span>

### <span data-ttu-id="27cf5-138">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="27cf5-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="27cf5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="27cf5-139">System.String</span></span>

## <span data-ttu-id="27cf5-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27cf5-140">OUTPUTS</span></span>

### <span data-ttu-id="27cf5-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="27cf5-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="27cf5-142">Note</span><span class="sxs-lookup"><span data-stu-id="27cf5-142">NOTES</span></span>
* <span data-ttu-id="27cf5-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="27cf5-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="27cf5-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27cf5-144">RELATED LINKS</span></span>

[<span data-ttu-id="27cf5-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="27cf5-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="27cf5-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="27cf5-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


