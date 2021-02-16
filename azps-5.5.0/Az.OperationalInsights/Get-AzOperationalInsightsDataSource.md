---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179246"
---
# <span data-ttu-id="f4f79-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f4f79-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="f4f79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f79-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f79-103">Recuperare origini dati nell'area di lavoro Analisi log di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f79-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="f4f79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4f79-104">SYNTAX</span></span>

### <span data-ttu-id="f4f79-105">ByWorkspaceNameBy Testo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4f79-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f79-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="f4f79-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f79-107">ByWorkspaceObjectBy Scorte</span><span class="sxs-lookup"><span data-stu-id="f4f79-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f79-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="f4f79-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4f79-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4f79-109">DESCRIPTION</span></span>
<span data-ttu-id="f4f79-110">Il cmdlet **Get-AzOperationalInsightsDataSource ottiene** le origini dati.</span><span class="sxs-lookup"><span data-stu-id="f4f79-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="f4f79-111">È possibile specificare un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f4f79-111">You can specify a data source to get.</span></span>
<span data-ttu-id="f4f79-112">È possibile filtrare i risultati in base al tipo di origine dati.</span><span class="sxs-lookup"><span data-stu-id="f4f79-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="f4f79-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4f79-113">EXAMPLES</span></span>

## <span data-ttu-id="f4f79-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4f79-114">PARAMETERS</span></span>

### <span data-ttu-id="f4f79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f79-115">-DefaultProfile</span></span>
<span data-ttu-id="f4f79-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f4f79-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4f79-117">-Kind</span><span class="sxs-lookup"><span data-stu-id="f4f79-117">-Kind</span></span>
<span data-ttu-id="f4f79-118">Specifica il tipo di origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f4f79-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="f4f79-119">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="f4f79-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f4f79-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="f4f79-120">AzureActivityLog</span></span> 
- <span data-ttu-id="f4f79-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="f4f79-121">CustomLog</span></span> 
- <span data-ttu-id="f4f79-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="f4f79-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="f4f79-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="f4f79-123">LinuxSyslog</span></span> 
- <span data-ttu-id="f4f79-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="f4f79-124">WindowsEvent</span></span> 
- <span data-ttu-id="f4f79-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="f4f79-125">WindowsPerformanceCounter</span></span>

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

### <span data-ttu-id="f4f79-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f4f79-126">-Name</span></span>
<span data-ttu-id="f4f79-127">Specifica il nome di un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f4f79-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="f4f79-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f79-128">-ResourceGroupName</span></span>
<span data-ttu-id="f4f79-129">Specifica il nome di un gruppo di risorse che contiene le origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f4f79-129">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="f4f79-130">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="f4f79-130">-Workspace</span></span>
<span data-ttu-id="f4f79-131">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4f79-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f4f79-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f4f79-132">-WorkspaceName</span></span>
<span data-ttu-id="f4f79-133">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4f79-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f4f79-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f79-134">CommonParameters</span></span>
<span data-ttu-id="f4f79-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f79-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f79-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4f79-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f79-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4f79-137">INPUTS</span></span>

### <span data-ttu-id="f4f79-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f4f79-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f4f79-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f4f79-139">System.String</span></span>

## <span data-ttu-id="f4f79-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4f79-140">OUTPUTS</span></span>

### <span data-ttu-id="f4f79-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f4f79-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f4f79-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4f79-142">NOTES</span></span>
* <span data-ttu-id="f4f79-143">Parole chiave: azure, azurerm, arm, risorsa, gestione, responsabile, operativo, approfondimenti</span><span class="sxs-lookup"><span data-stu-id="f4f79-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f4f79-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4f79-144">RELATED LINKS</span></span>

[<span data-ttu-id="f4f79-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f4f79-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="f4f79-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="f4f79-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


