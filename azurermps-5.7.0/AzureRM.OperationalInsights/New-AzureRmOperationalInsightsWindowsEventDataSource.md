---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: cebbcb0526c35fb803de783604db291612694baf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512439"
---
# <span data-ttu-id="cf83f-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="cf83f-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="cf83f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf83f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf83f-103">Raccoglie i registri eventi da computer che eseguono il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="cf83f-103">Collects event logs from computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf83f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf83f-104">SYNTAX</span></span>

### <span data-ttu-id="cf83f-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf83f-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf83f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cf83f-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf83f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf83f-107">DESCRIPTION</span></span>
<span data-ttu-id="cf83f-108">Il cmdlet **New-AzureRmOperationalInsightsWindowsEventDataSource** aggiunge un'origine dati che raccoglie i registri eventi di Windows da computer connessi che eseguono il sistema operativo Windows in Approfondimenti operativi di Azure.</span><span class="sxs-lookup"><span data-stu-id="cf83f-108">The **New-AzureRmOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="cf83f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf83f-109">EXAMPLES</span></span>

## <span data-ttu-id="cf83f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf83f-110">PARAMETERS</span></span>

### <span data-ttu-id="cf83f-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="cf83f-111">-CollectErrors</span></span>
<span data-ttu-id="cf83f-112">Indica che gli approfondimenti operativi raccolgono i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="cf83f-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="cf83f-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="cf83f-113">-CollectInformation</span></span>
<span data-ttu-id="cf83f-114">Indica che gli approfondimenti operativi raccolgono i messaggi informativi.</span><span class="sxs-lookup"><span data-stu-id="cf83f-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="cf83f-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="cf83f-115">-CollectWarnings</span></span>
<span data-ttu-id="cf83f-116">Indica che gli approfondimenti operativi raccolgono i messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="cf83f-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="cf83f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf83f-117">-DefaultProfile</span></span>
<span data-ttu-id="cf83f-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cf83f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf83f-119">-EventLogname</span><span class="sxs-lookup"><span data-stu-id="cf83f-119">-EventLogName</span></span>
<span data-ttu-id="cf83f-120">Specifica il nome del log eventi.</span><span class="sxs-lookup"><span data-stu-id="cf83f-120">Specifies the name of the event log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf83f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cf83f-121">-Force</span></span>
<span data-ttu-id="cf83f-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cf83f-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cf83f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf83f-123">-Name</span></span>
<span data-ttu-id="cf83f-124">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="cf83f-124">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf83f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf83f-125">-ResourceGroupName</span></span>
<span data-ttu-id="cf83f-126">Specifica il nome di un gruppo di risorse che contiene computer.</span><span class="sxs-lookup"><span data-stu-id="cf83f-126">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf83f-127">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="cf83f-127">-Workspace</span></span>
<span data-ttu-id="cf83f-128">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf83f-128">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf83f-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cf83f-129">-WorkspaceName</span></span>
<span data-ttu-id="cf83f-130">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf83f-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf83f-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf83f-131">-Confirm</span></span>
<span data-ttu-id="cf83f-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf83f-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf83f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf83f-133">-WhatIf</span></span>
<span data-ttu-id="cf83f-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf83f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf83f-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf83f-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf83f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf83f-136">CommonParameters</span></span>
<span data-ttu-id="cf83f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf83f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf83f-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf83f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf83f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf83f-139">INPUTS</span></span>

### <span data-ttu-id="cf83f-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cf83f-140">PSWorkspace</span></span>
<span data-ttu-id="cf83f-141">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="cf83f-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="cf83f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf83f-142">OUTPUTS</span></span>

### <span data-ttu-id="cf83f-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="cf83f-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="cf83f-144">Note</span><span class="sxs-lookup"><span data-stu-id="cf83f-144">NOTES</span></span>

## <span data-ttu-id="cf83f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf83f-145">RELATED LINKS</span></span>

