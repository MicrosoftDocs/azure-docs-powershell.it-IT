---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 5729daec656c7f99ac7f4c4c9440e090217c315d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516147"
---
# <span data-ttu-id="c0cc1-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="c0cc1-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="c0cc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="c0cc1-103">Aggiunge un'origine dati ai computer Linux.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0cc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0cc1-104">SYNTAX</span></span>

### <span data-ttu-id="c0cc1-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0cc1-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0cc1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c0cc1-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0cc1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0cc1-107">DESCRIPTION</span></span>
<span data-ttu-id="c0cc1-108">Il cmdlet **New-AzureRmOperationalInsightsLinuxSyslogDataSource** aggiunge un'origine dati syslog ai computer Linux collegati in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="c0cc1-109">Le informazioni operative di Azure possono raccogliere dati syslog.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="c0cc1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0cc1-110">EXAMPLES</span></span>

## <span data-ttu-id="c0cc1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0cc1-111">PARAMETERS</span></span>

### <span data-ttu-id="c0cc1-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="c0cc1-112">-CollectAlert</span></span>
<span data-ttu-id="c0cc1-113">Indica che gli approfondimenti operativi raccolgono i messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="c0cc1-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="c0cc1-114">-CollectCritical</span></span>
<span data-ttu-id="c0cc1-115">Indica che gli approfondimenti operativi raccolgono messaggi critici.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="c0cc1-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="c0cc1-116">-CollectDebug</span></span>
<span data-ttu-id="c0cc1-117">Indica che gli approfondimenti operativi raccolgono i messaggi di debug.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="c0cc1-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="c0cc1-118">-CollectEmergency</span></span>
<span data-ttu-id="c0cc1-119">Indica che gli approfondimenti operativi raccolgono messaggi di emergenza.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="c0cc1-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="c0cc1-120">-CollectError</span></span>
<span data-ttu-id="c0cc1-121">Indica che gli approfondimenti operativi raccolgono i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="c0cc1-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="c0cc1-122">-CollectInformational</span></span>
<span data-ttu-id="c0cc1-123">Indica che gli approfondimenti operativi raccolgono i messaggi informativi.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="c0cc1-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="c0cc1-124">-CollectNotice</span></span>
<span data-ttu-id="c0cc1-125">Indica che gli approfondimenti operativi raccolgono i messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="c0cc1-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="c0cc1-126">-CollectWarning</span></span>
<span data-ttu-id="c0cc1-127">Indica che il syslog include messaggi di avviso.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="c0cc1-128">-Struttura</span><span class="sxs-lookup"><span data-stu-id="c0cc1-128">-Facility</span></span>
<span data-ttu-id="c0cc1-129">Specifica un codice di struttura.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-129">Specifies a facility code.</span></span>

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

### <span data-ttu-id="c0cc1-130">-Force</span><span class="sxs-lookup"><span data-stu-id="c0cc1-130">-Force</span></span>
<span data-ttu-id="c0cc1-131">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0cc1-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0cc1-132">-Name</span></span>
<span data-ttu-id="c0cc1-133">Specifica un nome per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-133">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="c0cc1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0cc1-134">-ResourceGroupName</span></span>
<span data-ttu-id="c0cc1-135">Specifica il nome di un gruppo di risorse che contiene computer Linux.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-135">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="c0cc1-136">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="c0cc1-136">-Workspace</span></span>
<span data-ttu-id="c0cc1-137">Specifica un'area di lavoro in cui funziona questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-137">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c0cc1-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0cc1-138">-WorkspaceName</span></span>
<span data-ttu-id="c0cc1-139">Specifica il nome di un'area di lavoro in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-139">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c0cc1-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c0cc1-140">-Confirm</span></span>
<span data-ttu-id="c0cc1-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0cc1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0cc1-142">-WhatIf</span></span>
<span data-ttu-id="c0cc1-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0cc1-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0cc1-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0cc1-145">-DefaultProfile</span></span>
<span data-ttu-id="c0cc1-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0cc1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0cc1-147">CommonParameters</span></span>
<span data-ttu-id="c0cc1-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0cc1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0cc1-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0cc1-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0cc1-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0cc1-150">INPUTS</span></span>

### <span data-ttu-id="c0cc1-151">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0cc1-151">PSWorkspace</span></span>
<span data-ttu-id="c0cc1-152">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c0cc1-152">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="c0cc1-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0cc1-153">OUTPUTS</span></span>

### <span data-ttu-id="c0cc1-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c0cc1-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c0cc1-155">Note</span><span class="sxs-lookup"><span data-stu-id="c0cc1-155">NOTES</span></span>

## <span data-ttu-id="c0cc1-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0cc1-156">RELATED LINKS</span></span>

[<span data-ttu-id="c0cc1-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="c0cc1-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="c0cc1-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="c0cc1-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)


