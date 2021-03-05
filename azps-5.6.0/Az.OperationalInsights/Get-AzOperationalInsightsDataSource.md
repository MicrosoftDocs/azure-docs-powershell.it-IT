---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: c3ca23ae1cbe29c7c2867ec9ac48bea612dd4fc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976509"
---
# <span data-ttu-id="bc705-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="bc705-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="bc705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc705-102">SYNOPSIS</span></span>
<span data-ttu-id="bc705-103">Recuperare origini dati nell'area di lavoro Analisi log di Azure.</span><span class="sxs-lookup"><span data-stu-id="bc705-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="bc705-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc705-104">SYNTAX</span></span>

### <span data-ttu-id="bc705-105">ByWorkspaceNameByTip (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bc705-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc705-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="bc705-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc705-107">ByWorkspaceObjectByByObject</span><span class="sxs-lookup"><span data-stu-id="bc705-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc705-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="bc705-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc705-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bc705-109">DESCRIPTION</span></span>
<span data-ttu-id="bc705-110">Il cmdlet **Get-AzOperationalInsightsDataSource ottiene** le origini dati.</span><span class="sxs-lookup"><span data-stu-id="bc705-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="bc705-111">È possibile specificare un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bc705-111">You can specify a data source to get.</span></span>
<span data-ttu-id="bc705-112">È possibile filtrare i risultati in base al tipo di origine dati.</span><span class="sxs-lookup"><span data-stu-id="bc705-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="bc705-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc705-113">EXAMPLES</span></span>

## <span data-ttu-id="bc705-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc705-114">PARAMETERS</span></span>

### <span data-ttu-id="bc705-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc705-115">-DefaultProfile</span></span>
<span data-ttu-id="bc705-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bc705-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc705-117">-Kind</span><span class="sxs-lookup"><span data-stu-id="bc705-117">-Kind</span></span>
<span data-ttu-id="bc705-118">Specifica il tipo di origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bc705-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="bc705-119">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="bc705-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc705-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="bc705-120">AzureActivityLog</span></span> 
- <span data-ttu-id="bc705-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="bc705-121">CustomLog</span></span> 
- <span data-ttu-id="bc705-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="bc705-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="bc705-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="bc705-123">LinuxSyslog</span></span> 
- <span data-ttu-id="bc705-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="bc705-124">WindowsEvent</span></span> 
- <span data-ttu-id="bc705-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="bc705-125">WindowsPerformanceCounter</span></span>

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

### <span data-ttu-id="bc705-126">-Name</span><span class="sxs-lookup"><span data-stu-id="bc705-126">-Name</span></span>
<span data-ttu-id="bc705-127">Specifica il nome di un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bc705-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="bc705-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc705-128">-ResourceGroupName</span></span>
<span data-ttu-id="bc705-129">Specifica il nome di un gruppo di risorse che contiene le origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bc705-129">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="bc705-130">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="bc705-130">-Workspace</span></span>
<span data-ttu-id="bc705-131">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc705-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bc705-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bc705-132">-WorkspaceName</span></span>
<span data-ttu-id="bc705-133">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc705-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bc705-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc705-134">CommonParameters</span></span>
<span data-ttu-id="bc705-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc705-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc705-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc705-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc705-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="bc705-137">INPUTS</span></span>

### <span data-ttu-id="bc705-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bc705-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="bc705-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bc705-139">System.String</span></span>

## <span data-ttu-id="bc705-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc705-140">OUTPUTS</span></span>

### <span data-ttu-id="bc705-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bc705-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bc705-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="bc705-142">NOTES</span></span>
* <span data-ttu-id="bc705-143">Parole chiave: azure, azurerm, arm, risorsa, gestione, responsabile, operativo, approfondimenti</span><span class="sxs-lookup"><span data-stu-id="bc705-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="bc705-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc705-144">RELATED LINKS</span></span>

[<span data-ttu-id="bc705-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="bc705-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="bc705-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="bc705-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


