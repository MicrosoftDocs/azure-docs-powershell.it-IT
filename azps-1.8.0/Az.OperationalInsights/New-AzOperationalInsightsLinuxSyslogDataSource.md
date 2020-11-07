---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: a0268931d276c74560acd5cb04cac1d1e5778b81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677802"
---
# <span data-ttu-id="3e83b-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="3e83b-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="3e83b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e83b-102">SYNOPSIS</span></span>
<span data-ttu-id="3e83b-103">Aggiunge un'origine dati ai computer Linux.</span><span class="sxs-lookup"><span data-stu-id="3e83b-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="3e83b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e83b-104">SYNTAX</span></span>

### <span data-ttu-id="3e83b-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e83b-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e83b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3e83b-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e83b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e83b-107">DESCRIPTION</span></span>
<span data-ttu-id="3e83b-108">Il cmdlet **New-AzOperationalInsightsLinuxSyslogDataSource** aggiunge un'origine dati syslog ai computer Linux collegati in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3e83b-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="3e83b-109">Le informazioni operative di Azure possono raccogliere dati syslog.</span><span class="sxs-lookup"><span data-stu-id="3e83b-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="3e83b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e83b-110">EXAMPLES</span></span>

## <span data-ttu-id="3e83b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e83b-111">PARAMETERS</span></span>

### <span data-ttu-id="3e83b-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="3e83b-112">-CollectAlert</span></span>
<span data-ttu-id="3e83b-113">Indica che gli approfondimenti operativi raccolgono i messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="3e83b-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="3e83b-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="3e83b-114">-CollectCritical</span></span>
<span data-ttu-id="3e83b-115">Indica che gli approfondimenti operativi raccolgono messaggi critici.</span><span class="sxs-lookup"><span data-stu-id="3e83b-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="3e83b-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="3e83b-116">-CollectDebug</span></span>
<span data-ttu-id="3e83b-117">Indica che gli approfondimenti operativi raccolgono i messaggi di debug.</span><span class="sxs-lookup"><span data-stu-id="3e83b-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="3e83b-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="3e83b-118">-CollectEmergency</span></span>
<span data-ttu-id="3e83b-119">Indica che gli approfondimenti operativi raccolgono messaggi di emergenza.</span><span class="sxs-lookup"><span data-stu-id="3e83b-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="3e83b-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="3e83b-120">-CollectError</span></span>
<span data-ttu-id="3e83b-121">Indica che gli approfondimenti operativi raccolgono i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="3e83b-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="3e83b-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="3e83b-122">-CollectInformational</span></span>
<span data-ttu-id="3e83b-123">Indica che gli approfondimenti operativi raccolgono i messaggi informativi.</span><span class="sxs-lookup"><span data-stu-id="3e83b-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="3e83b-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="3e83b-124">-CollectNotice</span></span>
<span data-ttu-id="3e83b-125">Indica che gli approfondimenti operativi raccolgono i messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="3e83b-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="3e83b-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="3e83b-126">-CollectWarning</span></span>
<span data-ttu-id="3e83b-127">Indica che il syslog include messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="3e83b-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="3e83b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e83b-128">-DefaultProfile</span></span>
<span data-ttu-id="3e83b-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3e83b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e83b-130">-Struttura</span><span class="sxs-lookup"><span data-stu-id="3e83b-130">-Facility</span></span>
<span data-ttu-id="3e83b-131">Specifica un codice di struttura.</span><span class="sxs-lookup"><span data-stu-id="3e83b-131">Specifies a facility code.</span></span>

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

### <span data-ttu-id="3e83b-132">-Force</span><span class="sxs-lookup"><span data-stu-id="3e83b-132">-Force</span></span>
<span data-ttu-id="3e83b-133">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3e83b-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e83b-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e83b-134">-Name</span></span>
<span data-ttu-id="3e83b-135">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="3e83b-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="3e83b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e83b-136">-ResourceGroupName</span></span>
<span data-ttu-id="3e83b-137">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="3e83b-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="3e83b-138">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="3e83b-138">-Workspace</span></span>
<span data-ttu-id="3e83b-139">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e83b-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3e83b-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3e83b-140">-WorkspaceName</span></span>
<span data-ttu-id="3e83b-141">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e83b-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3e83b-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e83b-142">-Confirm</span></span>
<span data-ttu-id="3e83b-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e83b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e83b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e83b-144">-WhatIf</span></span>
<span data-ttu-id="3e83b-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e83b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e83b-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e83b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e83b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e83b-147">CommonParameters</span></span>
<span data-ttu-id="3e83b-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e83b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e83b-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e83b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e83b-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e83b-150">INPUTS</span></span>

### <span data-ttu-id="3e83b-151">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3e83b-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3e83b-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3e83b-152">System.String</span></span>

## <span data-ttu-id="3e83b-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e83b-153">OUTPUTS</span></span>

### <span data-ttu-id="3e83b-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3e83b-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3e83b-155">Note</span><span class="sxs-lookup"><span data-stu-id="3e83b-155">NOTES</span></span>

## <span data-ttu-id="3e83b-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e83b-156">RELATED LINKS</span></span>

[<span data-ttu-id="3e83b-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="3e83b-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="3e83b-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="3e83b-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


