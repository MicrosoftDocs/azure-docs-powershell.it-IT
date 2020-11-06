---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 1e9114b9f6b62f6900c975b39e5f8c67b4d9051a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513128"
---
# <span data-ttu-id="1900d-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="1900d-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="1900d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1900d-102">SYNOPSIS</span></span>
<span data-ttu-id="1900d-103">Aggiunge contatori delle prestazioni a tutti i computer Linux in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1900d-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1900d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1900d-104">SYNTAX</span></span>

### <span data-ttu-id="1900d-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1900d-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1900d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1900d-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1900d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1900d-107">DESCRIPTION</span></span>
<span data-ttu-id="1900d-108">Il cmdlet **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** aggiunge contatori delle prestazioni da cui Azure Operation Insights raccoglie i dati in tutti i computer Linux in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1900d-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="1900d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1900d-109">EXAMPLES</span></span>

## <span data-ttu-id="1900d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1900d-110">PARAMETERS</span></span>

### <span data-ttu-id="1900d-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="1900d-111">-CounterNames</span></span>
<span data-ttu-id="1900d-112">Specifica una matrice di nomi di contatori.</span><span class="sxs-lookup"><span data-stu-id="1900d-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1900d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1900d-113">-Force</span></span>
<span data-ttu-id="1900d-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1900d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1900d-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1900d-115">-InstanceName</span></span>
<span data-ttu-id="1900d-116">Specifica un nome di istanza.</span><span class="sxs-lookup"><span data-stu-id="1900d-116">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1900d-117">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="1900d-117">-IntervalSeconds</span></span>
<span data-ttu-id="1900d-118">Specifica l'intervallo di raccolta.</span><span class="sxs-lookup"><span data-stu-id="1900d-118">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1900d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1900d-119">-Name</span></span>
<span data-ttu-id="1900d-120">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="1900d-120">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1900d-121">-NomeOggetto</span><span class="sxs-lookup"><span data-stu-id="1900d-121">-ObjectName</span></span>
<span data-ttu-id="1900d-122">Specifica il nome di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="1900d-122">Specifies the name of an object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1900d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1900d-123">-ResourceGroupName</span></span>
<span data-ttu-id="1900d-124">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="1900d-124">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1900d-125">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="1900d-125">-Workspace</span></span>
<span data-ttu-id="1900d-126">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1900d-126">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1900d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1900d-127">-WorkspaceName</span></span>
<span data-ttu-id="1900d-128">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1900d-128">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1900d-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1900d-129">-Confirm</span></span>
<span data-ttu-id="1900d-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1900d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1900d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1900d-131">-WhatIf</span></span>
<span data-ttu-id="1900d-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1900d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1900d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1900d-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1900d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1900d-134">-DefaultProfile</span></span>
<span data-ttu-id="1900d-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1900d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1900d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1900d-136">CommonParameters</span></span>
<span data-ttu-id="1900d-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1900d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1900d-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1900d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1900d-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1900d-139">INPUTS</span></span>

### <span data-ttu-id="1900d-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1900d-140">PSWorkspace</span></span>
<span data-ttu-id="1900d-141">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1900d-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="1900d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1900d-142">OUTPUTS</span></span>

### <span data-ttu-id="1900d-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1900d-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1900d-144">Note</span><span class="sxs-lookup"><span data-stu-id="1900d-144">NOTES</span></span>

## <span data-ttu-id="1900d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1900d-145">RELATED LINKS</span></span>

[<span data-ttu-id="1900d-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="1900d-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="1900d-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="1900d-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


