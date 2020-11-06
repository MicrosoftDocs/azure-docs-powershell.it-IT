---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5d13fb4c432a0b40fdfd90a5eea55ea44a8b6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511631"
---
# <span data-ttu-id="0cc26-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0cc26-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="0cc26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0cc26-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc26-103">Ottenere le origini dati in area di lavoro di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="0cc26-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cc26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0cc26-104">SYNTAX</span></span>

### <span data-ttu-id="0cc26-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0cc26-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cc26-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="0cc26-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cc26-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="0cc26-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cc26-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="0cc26-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0cc26-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="0cc26-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cc26-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0cc26-110">DESCRIPTION</span></span>
<span data-ttu-id="0cc26-111">Il cmdlet **Get-AzureRmOperationalInsightsDataSource** ottiene le origini dati.</span><span class="sxs-lookup"><span data-stu-id="0cc26-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="0cc26-112">Puoi specificare un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0cc26-112">You can specify a data source to get.</span></span>
<span data-ttu-id="0cc26-113">È possibile filtrare i risultati in base al tipo di origine dati.</span><span class="sxs-lookup"><span data-stu-id="0cc26-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="0cc26-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0cc26-114">EXAMPLES</span></span>

## <span data-ttu-id="0cc26-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0cc26-115">PARAMETERS</span></span>

### <span data-ttu-id="0cc26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cc26-116">-DefaultProfile</span></span>
<span data-ttu-id="0cc26-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0cc26-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc26-118">-Tipo</span><span class="sxs-lookup"><span data-stu-id="0cc26-118">-Kind</span></span>
<span data-ttu-id="0cc26-119">Specifica il tipo di origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0cc26-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="0cc26-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0cc26-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0cc26-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="0cc26-121">AzureActivityLog</span></span> 
- <span data-ttu-id="0cc26-122">CustomLog</span><span class="sxs-lookup"><span data-stu-id="0cc26-122">CustomLog</span></span> 
- <span data-ttu-id="0cc26-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="0cc26-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="0cc26-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="0cc26-124">LinuxSyslog</span></span> 
- <span data-ttu-id="0cc26-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="0cc26-125">WindowsEvent</span></span> 
- <span data-ttu-id="0cc26-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="0cc26-126">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc26-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="0cc26-127">-Name</span></span>
<span data-ttu-id="0cc26-128">Specifica il nome di un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0cc26-128">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="0cc26-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cc26-129">-ResourceGroupName</span></span>
<span data-ttu-id="0cc26-130">Specifica il nome di un gruppo di risorse che contiene origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0cc26-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cc26-131">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="0cc26-131">-Workspace</span></span>
<span data-ttu-id="0cc26-132">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cc26-132">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0cc26-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0cc26-133">-WorkspaceName</span></span>
<span data-ttu-id="0cc26-134">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cc26-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cc26-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc26-135">CommonParameters</span></span>
<span data-ttu-id="0cc26-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cc26-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc26-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cc26-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc26-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0cc26-138">INPUTS</span></span>

### <span data-ttu-id="0cc26-139">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0cc26-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="0cc26-140">Parametri: area di lavoro (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0cc26-140">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="0cc26-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0cc26-141">System.String</span></span>

## <span data-ttu-id="0cc26-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0cc26-142">OUTPUTS</span></span>

### <span data-ttu-id="0cc26-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0cc26-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0cc26-144">Note</span><span class="sxs-lookup"><span data-stu-id="0cc26-144">NOTES</span></span>
* <span data-ttu-id="0cc26-145">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="0cc26-145">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="0cc26-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0cc26-146">RELATED LINKS</span></span>

[<span data-ttu-id="0cc26-147">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0cc26-147">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="0cc26-148">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0cc26-148">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


