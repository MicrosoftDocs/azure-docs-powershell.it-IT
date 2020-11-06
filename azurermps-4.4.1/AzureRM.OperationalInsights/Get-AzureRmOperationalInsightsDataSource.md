---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 61846456cfbff2dcbdaffba8c73a9bada87f07dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520011"
---
# <span data-ttu-id="cab54-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="cab54-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="cab54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cab54-102">SYNOPSIS</span></span>
<span data-ttu-id="cab54-103">Ottenere le origini dati in area di lavoro di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="cab54-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cab54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cab54-104">SYNTAX</span></span>

### <span data-ttu-id="cab54-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cab54-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cab54-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="cab54-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cab54-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="cab54-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cab54-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="cab54-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cab54-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="cab54-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cab54-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cab54-110">DESCRIPTION</span></span>
<span data-ttu-id="cab54-111">Il cmdlet **Get-AzureRmOperationalInsightsDataSource** ottiene le origini dati.</span><span class="sxs-lookup"><span data-stu-id="cab54-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="cab54-112">Puoi specificare un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="cab54-112">You can specify a data source to get.</span></span>
<span data-ttu-id="cab54-113">È possibile filtrare i risultati in base al tipo di origine dati.</span><span class="sxs-lookup"><span data-stu-id="cab54-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="cab54-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cab54-114">EXAMPLES</span></span>

## <span data-ttu-id="cab54-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cab54-115">PARAMETERS</span></span>

### <span data-ttu-id="cab54-116">-Tipo</span><span class="sxs-lookup"><span data-stu-id="cab54-116">-Kind</span></span>
<span data-ttu-id="cab54-117">Specifica il tipo di origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="cab54-117">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="cab54-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cab54-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cab54-119">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="cab54-119">AzureActivityLog</span></span> 
- <span data-ttu-id="cab54-120">CustomLog</span><span class="sxs-lookup"><span data-stu-id="cab54-120">CustomLog</span></span> 
- <span data-ttu-id="cab54-121">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="cab54-121">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="cab54-122">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="cab54-122">LinuxSyslog</span></span> 
- <span data-ttu-id="cab54-123">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="cab54-123">WindowsEvent</span></span> 
- <span data-ttu-id="cab54-124">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="cab54-124">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

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
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab54-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="cab54-125">-Name</span></span>
<span data-ttu-id="cab54-126">Specifica il nome di un'origine dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="cab54-126">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="cab54-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab54-127">-ResourceGroupName</span></span>
<span data-ttu-id="cab54-128">Specifica il nome di un gruppo di risorse che contiene origini dati da ottenere.</span><span class="sxs-lookup"><span data-stu-id="cab54-128">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="cab54-129">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="cab54-129">-Workspace</span></span>
<span data-ttu-id="cab54-130">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cab54-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cab54-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cab54-131">-WorkspaceName</span></span>
<span data-ttu-id="cab54-132">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cab54-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cab54-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab54-133">-DefaultProfile</span></span>
<span data-ttu-id="cab54-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cab54-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cab54-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab54-135">CommonParameters</span></span>
<span data-ttu-id="cab54-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab54-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab54-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab54-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab54-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cab54-138">INPUTS</span></span>

### <span data-ttu-id="cab54-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cab54-139">PSWorkspace</span></span>
<span data-ttu-id="cab54-140">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="cab54-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="cab54-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cab54-141">PSWorkspace</span></span>
<span data-ttu-id="cab54-142">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="cab54-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="cab54-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cab54-143">OUTPUTS</span></span>

### <span data-ttu-id="cab54-144">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="cab54-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="cab54-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="cab54-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="cab54-146">Note</span><span class="sxs-lookup"><span data-stu-id="cab54-146">NOTES</span></span>
* <span data-ttu-id="cab54-147">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="cab54-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="cab54-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cab54-148">RELATED LINKS</span></span>

[<span data-ttu-id="cab54-149">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="cab54-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="cab54-150">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="cab54-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


