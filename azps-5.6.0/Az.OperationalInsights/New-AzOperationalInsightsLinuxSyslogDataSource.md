---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: ab11fcb47550603e23871730ed8779baa6cf7740
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989923"
---
# <span data-ttu-id="9fc79-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="9fc79-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="9fc79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fc79-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc79-103">Aggiunge un'origine dati ai computer Linux.</span><span class="sxs-lookup"><span data-stu-id="9fc79-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="9fc79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fc79-104">SYNTAX</span></span>

### <span data-ttu-id="9fc79-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9fc79-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fc79-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9fc79-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fc79-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9fc79-107">DESCRIPTION</span></span>
<span data-ttu-id="9fc79-108">Il cmdlet **New-AzOperationalInsightsLinuxSyslogDataSource** aggiunge un'origine dati SysLog ai computer Linux connessi in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9fc79-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="9fc79-109">Azure Operational Insights può raccogliere dati syslog.</span><span class="sxs-lookup"><span data-stu-id="9fc79-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="9fc79-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fc79-110">EXAMPLES</span></span>

### <span data-ttu-id="9fc79-111">Esempio 1: Creare origini dati SysLog</span><span class="sxs-lookup"><span data-stu-id="9fc79-111">Example 1: Create syslog data sources</span></span>
```
$FacilityNames       = @()
$FacilityNames      += 'auth'
$FacilityNames      += 'authpriv'
$FacilityNames      += 'cron'
$FacilityNames      += 'daemon'
$FacilityNames      += 'ftp'
$FacilityNames      += 'kern'
$FacilityNames      += 'mail'
$FacilityNames      += 'syslog'
$FacilityNames      += 'user'
$FacilityNames      += 'uucp'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($FacilityName in $FacilityNames) {
    $Count++
    $null = New-AzOperationalInsightsLinuxSyslogDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Linux-syslog-$($Count)" `
    -Facility $FacilityName `
    -CollectEmergency `
    -CollectAlert `
    -CollectCritical `
    -CollectError `
    -CollectWarning `
    -CollectNotice `
    -CollectDebug `
    -CollectInformational
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'LinuxSyslog'
```

## <span data-ttu-id="9fc79-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fc79-112">PARAMETERS</span></span>

### <span data-ttu-id="9fc79-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="9fc79-113">-CollectAlert</span></span>
<span data-ttu-id="9fc79-114">Indica che Dati operativi raccoglie messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="9fc79-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="9fc79-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="9fc79-115">-CollectCritical</span></span>
<span data-ttu-id="9fc79-116">Indica che Dati operativi raccoglie messaggi critici.</span><span class="sxs-lookup"><span data-stu-id="9fc79-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="9fc79-117">-CollectSetting</span><span class="sxs-lookup"><span data-stu-id="9fc79-117">-CollectDebug</span></span>
<span data-ttu-id="9fc79-118">Indica che Dati operativi raccoglie messaggi di debug.</span><span class="sxs-lookup"><span data-stu-id="9fc79-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="9fc79-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="9fc79-119">-CollectEmergency</span></span>
<span data-ttu-id="9fc79-120">Indica che Dati operativi raccoglie messaggi di emergenza.</span><span class="sxs-lookup"><span data-stu-id="9fc79-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="9fc79-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="9fc79-121">-CollectError</span></span>
<span data-ttu-id="9fc79-122">Indica che Dati operativi raccoglie messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="9fc79-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="9fc79-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="9fc79-123">-CollectInformational</span></span>
<span data-ttu-id="9fc79-124">Indica che Dati operativi raccoglie messaggi informativi.</span><span class="sxs-lookup"><span data-stu-id="9fc79-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="9fc79-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="9fc79-125">-CollectNotice</span></span>
<span data-ttu-id="9fc79-126">Indica che Dati operativi raccoglie messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="9fc79-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="9fc79-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="9fc79-127">-CollectWarning</span></span>
<span data-ttu-id="9fc79-128">Indica che il log di sistema include messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="9fc79-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="9fc79-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc79-129">-DefaultProfile</span></span>
<span data-ttu-id="9fc79-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9fc79-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fc79-131">-Struttura</span><span class="sxs-lookup"><span data-stu-id="9fc79-131">-Facility</span></span>
<span data-ttu-id="9fc79-132">Specifica un codice di struttura.</span><span class="sxs-lookup"><span data-stu-id="9fc79-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="9fc79-133">-Force</span><span class="sxs-lookup"><span data-stu-id="9fc79-133">-Force</span></span>
<span data-ttu-id="9fc79-134">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="9fc79-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9fc79-135">-Name</span><span class="sxs-lookup"><span data-stu-id="9fc79-135">-Name</span></span>
<span data-ttu-id="9fc79-136">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="9fc79-136">Specifies a name for the data source.</span></span> <span data-ttu-id="9fc79-137">Il nome non viene esposto nel portale di Azure e può essere usato qualsiasi stringa purché sia univoca.</span><span class="sxs-lookup"><span data-stu-id="9fc79-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="9fc79-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fc79-138">-ResourceGroupName</span></span>
<span data-ttu-id="9fc79-139">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="9fc79-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="9fc79-140">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="9fc79-140">-Workspace</span></span>
<span data-ttu-id="9fc79-141">Specifica un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fc79-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9fc79-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9fc79-142">-WorkspaceName</span></span>
<span data-ttu-id="9fc79-143">Specifica il nome di un'area di lavoro in cui viene eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fc79-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9fc79-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fc79-144">-Confirm</span></span>
<span data-ttu-id="9fc79-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fc79-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fc79-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fc79-146">-WhatIf</span></span>
<span data-ttu-id="9fc79-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fc79-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fc79-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fc79-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fc79-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc79-149">CommonParameters</span></span>
<span data-ttu-id="9fc79-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fc79-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc79-151">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fc79-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc79-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="9fc79-152">INPUTS</span></span>

### <span data-ttu-id="9fc79-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9fc79-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9fc79-154">System.String</span><span class="sxs-lookup"><span data-stu-id="9fc79-154">System.String</span></span>

## <span data-ttu-id="9fc79-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fc79-155">OUTPUTS</span></span>

### <span data-ttu-id="9fc79-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9fc79-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9fc79-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="9fc79-157">NOTES</span></span>

## <span data-ttu-id="9fc79-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fc79-158">RELATED LINKS</span></span>

[<span data-ttu-id="9fc79-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9fc79-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="9fc79-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="9fc79-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


